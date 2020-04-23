<!-- TITLE: Experimentation Process -->
<!-- SUBTITLE: Patras5G Experimentation Process -->

# Experimentation Process

## Patras5G Access

Patras5G facility adopts the Network Slice as a Service (NSaaS) delivery model, whereby the Patras5G facility provisions tailored network slices to verticals upon request. Each vertical uses the slice that has been provided to meet their requirements for trialling activities, setting up different use cases and assessing their KPIs under different network conditions.
Patras5G facility incorporates into its architecture the guidelines from telecom industry organisations and the normative specifications from standards bodies to ensure interoperability and reproducibility. The Patras5G facility is based on Openslice (http://openslice.io)  which allows NSaaS delivery model is shown in next Figure, where the Patras5G portal and service catalogue expose TM Forum Open APIs towards verticals to allow them to directly trigger necessary operations for service ordering. The Patras5G Service Catalogue derives content from Patras5G Facility Service Catalogue offerings. The vertical's service order is then passed to the Service Orchestrator (SO) in Patras5G facility. The SO then instantiates the network slice by subsequent calls to the respective network function orchestrator (NFVO). The NFVO implements the northbound interface using ETSI SOL 005. This normative specification defines the protocol and data model for the interface capabilities in the form of RESTful APIs which have become de-facto solutions for most of the industrial and open-source NFVOs.


![Onboarding Process Service Access](/uploads/onboarding/onboarding-process-service-access.png "Onboarding Process Service Access")

### Service Exposure Level of Patras5G

The Patras5G exposes  Levels under different circumstances and requirements. This depends on the customer use cases and needs.

#### Level 1 Access

**Exposed entity and access:** 5G-VINNI Portal (WEB UI and REST API) https://patras5g.eu , VPN access to deployed NS

**Description:** Service Catalog exposure (TMForum), Service Ordering Support(TMForum), scheduled orchestration, and VPN access to deployed NS. Access to monitoring data of various points


#### Level 2 Access

**Exposed entity and access:**  5G-VINNI Portal (WEB UI and REST API) https://patras5g.eu NFVO onboarding. Will be available at the level of 5G-RAN, 5G-CORE and Transport Controllers 

**Description:** Upload/manage 3rd party VNFs/NSDs to facility NFVO (via web UI and REST API). scheduled NSD orchestration,  Depending on the capabilities and if the underlying technologies allow this


#### Level 3 Access

**Exposed entity and access:**  Access to facility OSM (web and NBI SOL005)

**Description:** This will be available in special cases where the portal access is not enough. In most cases a separate tenant will be created ( OSM SIX )


#### Level 4 Access

**Exposed entity and access:**  Access to facility NFVI

**Description:** Use of Openstack (Rocky) APIs and HORIZON UI. Tenant will not have administrative privileges. Allowed to install VMs on subnets accessible by the 5G core. In certain cases will be allowed to view VNFs deployed by the OSM tenant project


See also (https://wiki.patras5g.eu/support-and-lcm) about the Exposure Level definition .

## Patras5G Experimentation Process

### ONBOARDING

Onboarding a vertical on Patras5G facility is challenging as it involves various iterative and parallel steps. The problem is compounded by the introduction of experimentation aspects as it involves monitoring and testing of KPIs when the network slice is in operation. It is therefore of utmost importance that the different stakeholders of 5G system co-design and co-develop different parts of the onboarding process for a successful service operation and KPI testing.
Figure 5 displays the 5G-VINNI vertical onboarding process. The process consists of several phases which are discussed in detail in subsequent sections.
i) The co-design period which involves stakeholders such as vertical customers, 5G-VINNI facility providers and CFS/RFS developers to understand the vertical needs and how to enable them.
ii) The iterative co-development period which involves the vertical customer and the 5G facility provider to jointly develop the final service to be ordered including the development of any VNFs, test scripts and monitoring services. Testing as a Service (TaaS) and Monitoring as a Service (MaaS) can be integrated during the preparation of the VNFs and development of service templates. This is subject to availability of TaaS and/or MaaS in the 5G-VINNI facility site.
iii) The operational and KPI testing KPI period: In this phase the vertical customer can make repeatable and scheduled service orders of the developed service blueprint via the portal and perform KPI testing, monitoring and assessment.

( Our process is based on the whitepaper https://doi.org/10.5281/zenodo.3695716  )

![Onboarding Process](/uploads/onboarding/onboarding-process.png "Onboarding Process")


### VERTICAL AND FACILITY CO-DESIGN PERIOD

During this initial period the involved stakeholders such as vertical customer, 5G-VINNI facility providers, CFS/RFS developers need to understand the vertical customer needs from the 5G facility in terms of:
* what needs to be extended and co-developed
* what and where can be measured and tested
* what is the plan for onboarding?
Since orchestration is a key part of automatically configuring, activating and deactivating services and network slices in a repeatable fashion, certain components must be developed either by the vertical or the 5G-VINNI facility.
To understand better the vertical customer, and to ease this process, the following phases are envisioned:

#### EARLY INSTALLATION OF THE VERTICAL USE CASE
This phase involves a sanity check of the vertical use case by instantiating key components required to execute the service. As this is an initial sanity check so the instantiation need not to be automated.

#### COMMON UNDERSTANDING
The advantage of the early installation of the vertical use case enables all the stakeholders to reach a common understanding with respect to:
*  vertical requirements from the 5G system and the capabilities of the 5G facility.
*  service onboarding as some parts of the vertical services might need to be developed for automated deployment by orchestrators. Here the verticals need to understand the target orchestrator and the supported NFV models (YANG, TOSCA).
*  what can be parameterized. This involves verticals to clearly identify if there are any exposed parameters from the vertical services that can be parameterized and reconfigured during orchestration.
*  the procedure and tools for automated test, measurement and validation. This also involves shepherding the vertical in order


Upon reaching a common understanding, the vertical and the 5G facility can proceed with a co-development period. We identify here two main processes:
i) the Network Service Design process which is related to resource facing services (RFS)
ii) the Service Design process which is related to customer facing services (CFS)

### CO-DEVELOPMENT PERIOD– SERVICE DESIGN PROCESS (CFS)

During this phase the 5G facility develops the service blueprint (SB) together with the vertical customer. The SB is pre-launch/pre-ordered via the Service Orchestrator which also involves validation of the Taas and MaaS to be correctly orchestrated. The process is iterative and interacts with the Network Service Design process.

#### DESIGN THE SERVICE BLUEPRINT
During this process, the Vertical and the 5G facility can define the attributes of the 5G-VINNI-SB. This step might need some research on defining the proper parameter values in which the stakeholders need to be pragmatic on how these requirements are “translated” towards the SO and NFVO. In later stages, the 5G-VINNI-SB will be used to automatically trigger the complete orchestration of the network slice instance. Proper definition of the 5G-VINNI-SB requires some work initially but this will benefit the vertical customer to consequently reproduce the service instantiation via the service catalogues at later stages with potential minor updates to the 5G-VINNI-SB.

#### TEST CASE DESIGN
The 5G-VINNI-SB will have the option to include testing as a service (TaaS). For example, by including relevant test scripts for TaaS. The test scripts will represent specific Test Cases (TCs) that are targeted at stressing specific aspects or KPIs of the Service. It is important to understand that there are two types of TCs: 1) TCs for validating fundamental network KPIs like throughput, delay, and 2) TCs for validating the service of the vertical customer that might include the vertical’s application. While the former can be offered as part of the service design with minimal configuration, the latter might require significant work.
Training on TCs design methodologies will be offered by 5G-VINNI facility as part of the available documentation. It is of fundamental importance that in order to achieve consistent and repeatable results, all actors in the value chain, including the vertical customer, is capable of designing solid TCs. Ongoing consulting support will be provided in the design phase, where most of the work will consists in creating specifications rather than scripts. Only afterward, the scripts can be reliably developed.

#### TEST AND VALIDATE SERVICE BLUEPRINT DEPLOYMENT/ ACTIVATION OF SB
At this point the 5G-VINNI-SB has been co-created with the vertical. The next step is to test and validate its proper operation via the SO. This involves pre-launching/pre-ordering the 5G-VINNI-SB via the portal to check that the 5G-VINNI-SB can be correctly orchestrated via the SO. In this step, the 5G-VINNI facility tries to instantiate, test and validate the defined 5G-VINNI-SB. This is also related to developments in Openslice itself as well as development in the SO part. During this step, the 5G-VINNI-SB attributes might be redefined based on the interaction with the 5G-VINNI facility.

#### LAUNCH SERVICE SPEC - ALPHA/BETA VERSIONS
Since the 5G-VINNI-SB is instantiated and validated successfully, the 5G-VINNI facility can start launching different versions of the 5G-VINNI-SB towards the SO and NFVO while involving TaaS and MaaS, checking and assessing their interoperability.

#### PRE-VALIDATION
In this step, a pre-validation period can start and required adjustment can be made to the service order. The vertical customer and 5G-VINNI facility can check that the KPIs can be extracted properly. Since the orchestration of 5G-VINNI-SB parts have been verified, the vertical customer and the 5G-VINNI facility can schedule and perform a pre-validation of the service and validate the proper deployment of the Network Service as discussed in section 2.3. At this stage it can be verified that the developed CFS can extract the proper KPIs. This process might also involve TaaS. By invoking TaaS during service deployment, the vertical customer and 5G facility will validate that the 5G-VINNI-SB and TaaS/MaaS work as expected.


### CO-DEVELOPMENT PERIOD - NETWORK SERVICE DESIGN PROCESS (RFS)
The Network Service design process is related with the NFV specifics of onboarding. This process is iterative and interacts with the Service Design process.

####  VNFD/NSD DEVELOPMENT
This step is optional, depending on whether or not the vertical customer need to on-board any additional VNFs during orchestration.
Prior to development of VNFs/NSDs, the developer must understand the specifics of the target 5G facility and plan for any specific requirements (e.g., hardware acceleration, Internet access for VNF). Creating VNF packages or Network Service descriptors is a tedious task and depends on the target NFV Orchestrator (e.g. OSM, Nokia CloudBand Network Director) and the standard followed. For the creation of VNFs the following should be considered:
* Preparing the Virtual Machine image
* Implement a VNF descriptor according to target orchestrator model
* Implement any configurations related to the VNF Manager and especially the Element Management System (EMS). EMS is responsible for the functional management of VNF, i.e. FCAPS (Fault, Configuration, Accounting, Performance and Security Management), which often involves VNF management using proprietary interfaces.
* VNF packaging
Similarly, for Network Service descriptors, the task includes:
1. Creating folder structure
2. Completing the NSD YAML file, with the Network Service metadata, constituent VNFDs and Virtual Link Descriptors
3. Packaging the Network Service

#### VNFD/NSD ONBOARDING
This is an iterative task performed by the VNF/NSD developers. Usually the developers get access to an orchestrator in order to develop and test their VNF/NSDs. The 5G facility might also give access to their own orchestrator.
The following options might be available to the vertical customer:
* Manual onboarding of VNFD/NSD performed by the 5G facility operator.
* Self-service onboarding/off boarding, deployment test and access (Exposure Level 1): Automated self-service onboarding can be done by Openslice NFV portal when offered by the 5G facility
* The 5G facility might offer a staging area (e.g. a private OSM to experiment) or offer the use of the production NFVO itself (Exposure Level 2 and 3)
* The 5G facility might offer VIM access (Exposure Level 4)
The vertical customer must upload any VM images to the 5G facility so that these can be stored in the image repository.

#### VNFD/NSD VALIDATION
In this step, it is recommended to test the NSD orchestration only by the NFVO to identify any errors in which case the previous steps of developing, on-boarding, test orchestration might be repeated.
When the pre-validation and testing are performed and the VNFDs and NSDs can be repeatedly orchestrated and instantiated without errors, it is advised to on-board the VNFDs and NSDs to the production NFVO of the 5G facility via its tools and processes.
It needs to be highlighted that remote access through VPN is provided by the 5G-VINNI facility for accessing the instantiated VNFs and the running NSs.

#### VNFD/NSD MAAS AND TAAS
While this step is optional, the vertical customer should consider the involvement of monitoring and testing services during VNFD and NSD development. Such services can be consumed both as a human-driven or an automated interaction. It is necessary to understand that such services require actions from the vertical customer side in order to be properly consumed such as the VNF exposing its functionality to a monitoring system.
TaaS is a set of testing tools and automation frameworks that allow the vertical customer to either execute standard verification of the Network Service, or create and execute customized suites of tests that can be successfully integrated into the life cycle of the NSD. Such tests can also include the vertical customer’s application, since the TaaS system should be capable of onboarding specific drivers.
MaaS is targeted at having a constant overview of the health and performance of the system, and it consists of two main categories of services: Network Monitoring and Telemetry. The former is the traditional overview of the traffic flowing across the network, in particular emphasizing the visibility in specific critical points in the network. The latter is focused on providing the health and performance of the individual Network Service or VNFs/application components. The two categories are very different despite being offered under the same umbrella of MaaS.
TaaS consists of a set of testing tools that can be deployed, configured, and automated through a set of offered web services. A typical example of testing tools is traffic generators, that can emulate realistic traffic and protocols. The offered services allow the vertical customer to:
* onboard specific drivers for automating vertical applications and use cases
* create and execute individual test scripts for automating the tests or the experimentation
* create and execute test campaigns, i.e. batch of test scripts that can be executed on multiple target infrastructures
* visualize logs and results through the offered visualization systems
* allow the vertical to develop customized visualizations
In order to better understand how to consume a TaaS service, an example is depicted in Figure 6

#### PRE-VALIDATION KPI PERIOD VIA NFVO
After a vertical customer together with the 5G-VINNI facility have developed the VNFs and NSDs, the next step is to test these for proper instantiation via the 5G facility’s NFV orchestrator. Since, at this point in the process, the orchestration has been verified, the vertical customer and the 5G facility can schedule and perform a pre-validation of the Network Service.
This step might also involve TaaS. By invoking TaaS during VNF and Network Service deployment, the vertical customer and 5G-VINNI facility need to validate that the VNFs and TaaS/MaaS work as expected.
The above defined steps of the Network Service design process might be repeated multiple times since NFV orchestration is key to repeatability of Network Service deployments and testing.


### OPERATIONAL AND KPI TESTING PERIOD

During this period and since CFS and RFS are in place, an official Testing period can start according to the 5G-VINNI facility plan. This process is again iterative and if necessary, developers might revisit previous steps. The following steps are planned.

#### SERVICE BLUEPRINT SPECIFICATION LAUNCHED
The latest developed 5G-VINNI-SB is officially launched in the 5G facility catalogue and ready for service orders.

#### E2E SERVICE ORDER FULFILMENT
The Service Order takes place and the subsequent services are instantiated.

#### TESTING
In this phase the actual testing takes place, either through automated scripts or via user interactions. It is strongly suggested to use test automation in order to ensure consistency and repeatability of the results. Testing consulting services will be provided in order to facilitate the testing and experimentation operations. The results of the testing (or the MaaS aspects) will be stored in heterogeneous data stores. These data stores cannot be defined at the present moment and will be strongly dependent on the use cases and tools used.

#### ASSESSMENT
The monitoring data is available to the vertical customer for any assessment.

### OFFER THE SERVICE BLUEPRINT TO THE VERTICAL COMMUNITY
After the testing and validation period the defined 5G-VINNI-SB can be publicly offered to the vertical customer community for repeatable deployments.


