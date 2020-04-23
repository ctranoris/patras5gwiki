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



