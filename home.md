![Architecture 2025 04 02](/uploads/images/architecture-2025-04-02.png "Architecture 2025 04 02")<!-- TITLE: Home -->
<!-- SUBTITLE: Welcome to Patras 5G Wiki -->


<img src="/uploads/patras-5-g-logo.png" width="320">


# Patras 5G wiki

**The Patras 5G facility is an "isolated" Non-public Network for 5G and IoT applications.**

* Patras5G facility adopts the Network Slice as a Service (NSaaS) delivery model, whereby the facility provisions tailored network slices to verticals upon request. Each vertical uses the slice that has been provided to meet their requirements for trialing activities, setting up different use cases and assessing their KPIs under different network conditions.
* Users and applications access is enabled by the open-source Operations Support System (OSS) Openslice, an ETSI SDG (https://osl.etsi.org ). Vertical applications can manage and on-board their artefacts through our user-friendly portal or programmatically access the available services. The Service Catalogue is easily accessible through our site portal (https://patras5g.eu).
* An APIs collection, which adheres to the TMForum OpenAPIs standard, provides comprehensive management of various artefacts. The APIs encompass Service Catalog, Service Order and Service Inventory, Partner Management and Users, Service Orchestration, VNFs/NSDs catalogue, and NFVO endpoints via OSM NBI, Service and NFV Deployment requests.
* The testbed provides telemetry and monitoring through Prometheus and NetData, which offers comprehensive metrics related to cloud infrastructure, VNFs, and RAN nodes as well as measurement sensors for energy consumption of compute nodes, switches, 5G gNBs, and CPEs, with all data securely gathered in a Prometheus server. Prometheus alongside Grafana is used for monitoring purposes. Elastic search and Kibana are used to collect and visualize data

In a nutshell:

* We offer for testing and experimentation a private 5G Network, working on licensed and unlicensed spectrum, with our own SIM cards.
* We provide 5G standard-conformant components and Core Network infrastructure 
* mmWave backhaul is installed to various locations in the city of Patras to link the access to the core network, and Fixed Wireless Access to provide broadband services to the facility
* Integration of various open source and commercial 5G Cores with  SDR platforms and UEs and g/eNB
* Enabling the E2E deployment of multiple customized-slices over the whole network – access, transport and core. This further includes the slicing of the IoT devices at the edge of the network.
* Supporting MEC orchestration and mobility management features for the support of interactive mobile streaming edge services.
* We have an Academic License from the Greek government on the licensed spectrum.

Most of the installed components are offered as Open Source but there are also dedicated components and services to support 5G and IoT scenarios. 
Numerous partners have deployed their technologies in the Patras 5G facility, thus creating a unique 5G playground for KPI validation and support on future verticals.

## Access to the facility:

**Physical access**
Users are offered with the required technical and scientific assistance to learn and use the infrastructure. Such a type of access is more applicable to users that cannot  easily access remotely for fine-tuning, and facilitate experiments requiring physical presence on site, such as for instance Bring-Your-Own-Equipment (BYOE). In such cases, users can install their prototype equipment at the Patras5G premises and combine it in their use cases with the equipment offered Patras5G. (Radios, 5GCore cloud, clusters, etc)

**Remote access** 
Users make service orders through our portal (https://patras5g.eu) for requesting a service. Then we offer various tools to access the requested resources (virtual machines, containers, etc)

## Demo videos


 <iframe width="640" height="360" src="https://www.youtube.com/embed/DkBKhYaHqPg?autoplay=1&mute=1">
</iframe> 
 <iframe width="640" height="360" src="https://www.youtube.com/embed/U3Mv7NCn40w?autoplay=1&mute=1">
</iframe> 


5G end-to-end experimentation: From Service Order to Network Monitoring Service https://www.youtube.com/watch?v=X662lml0p8w
5G-VINNI Patras Facility [video](https://www.youtube.com/watch?v=rASfEuHzhW0) for a quick presentation


## News

Check out our social media pages: https://www.linkedin.com/company/74512910/admin/



## Patras 5G facility infrastructure: Onboarding and access for Vertical Applications

<img src="/uploads/images/architecture-2025-04-02.png" width="1024">


**Summary of capabilities**
With our OSS, NFV and experimentation enabled services, like Openslice and Open Source MANO, we enable E2E automated deployment of multiple customized-slices over the whole network – access, transport and core. This further includes the slicing of the IoT devices at the edge of the network. 

Patras 5G facility is equipped with a cloud platform, able to host core network components, as well as NFV and MEC deployments. The cloud platform offers a total computing power of 1082 CPUs and 4,5 TB of RAM and 100 TB of storage.
3 Servers are AI enabled, each one equiped with 2xGPUs of NVIDIA PNY QUADRO A6000 48GB GDDR6 GPU Nvidia RTX interconnected via NVIDIA NVLINK Bridge
All servers are interconnected on 100GbE/400GbE Edgecore P4 Switches
and  10GbE/40GbE NVIDIA Cumulus switches with dual 10GbE NICs DPDK enabled. 

Kubernetes clusters are available on demand managed via GitOps: LF Sylva, OpenSourceMANO or Terraform, attached to the dataplane of the 5G System provided by Patras5G/PNET. Experimenters can order 5G connectivity as one of the network services, reserve resources, and configure the network based on user profiles for indoor and outdoor sites. Experimenters receive pre-provisioned sim cards for their external applications/devices to connect directly to the 5G network and interact with network applications deployed in dedicated k8s clusters. The cloud-hosted 5G core, deployed in a k8s cluster, relies on the open-source implementation of Open5GS/Free5GC and OpenAirInterface, enabling dynamic deployments.


Patras 5G provides 5G standard-conformant components and Core Network infrastructure and Integration of 5G Core and 5G RAN with our Opensource based NFV platform.  We support various flavors and installations of the 5G System, that are both NSA and SA depending on the scenarios that the customer wants to support.
* 	5G Core and EPC solutions that are available and can be orchestrated in the facility:  FhG Open5GCore, Open5GS in Kubernetes, free5GC in Kubernetes, OpenAirInterface in Kubernetes, AMARISOFT EPC, SRS EPC
* 	[Radio equipment](radio-equipment) 5G and 4G RAN[Available gNodeBs](radio-equipment/g-node-bs): AMARISOFT 5G RAN (Classic boxes), 5G RAN open source radio (Lime, SRS)-700-800MHz, 3.5.-3.8GHz, 4G NB-IoT, LTE-M (FhG NB-IOT core) based on AMARISOFT, Various SDR equipment (ETTUS)
* 	 [Available UEs](radio-equipment/u-es) based on Limemicro’s SDR and SRS software, as well as commercial UEs: Mobile phones LG and Samsung, Huawei CPE, Various SDR equipment, a Drone for URLLC testing
* 	Monitoring is available through: Graphana, Prometheus,Netdata while OSM also configure with VNF telemetry support
* 	Patras 5G has mmWave backhaul [Other Devices](radio-equipment/other-devices) to link the access to the core network, and Fixed Wireless Access to provide broadband services to the facility from various locations in the region of Patras and beyond. 
* 	GEANT connectivity is also available

## P-NET pre-commercial 5G extension

<img src="/uploads/images/pnet-extension.jpg" width="640">

The Patras5G testbed hosts a next generation networks pre-commercial site, based on ERICSSON 5G Rel-17 and beyond equipment. The site hosts several 5G radios indoors and outdoors located at the area of UoP, as well as a dedicated edge User Plane Function - UPF, while the 5G Core is co-located remotely in Athens containing all related functions (Access Mobility Function-AMF, Session Management Function-SMF, Network Exposure Function-NEF, etc) by a Greek operator NOVA which hosts a dedicated slice for PNET. This extension offers a unique opportunity to test 5G/6G cloud to edge scenarios, as well as various non-public-network deployments, using NOVA’s licensed spectrum.
Read more:
[P-NET pre-commercial 5G extension](pnet-extension)
## Interacting with the facility


### Web interface

Vertical applications can access the Patras 5G Service Catalogue through the Patras Facility site portal: https://patras5g.eu .  Vertical applications can self-manage and onboard their artifacts through our portal or access programmatically available services.


### APIs

Various artifacts can be managed through our APIs colleaction (see swagger) https://patras5g.eu/tmf-api/swagger-ui/ via standardized TMForum OpenAPIs: Service Catalog,  Service Order and Service Inventory, Partner Management and Users, Service Orchestration, VNFs/NSDs catalogue, NFVO endpoints via OSM NBI, Service and NFV Deployment requests. 

### Openslice

![Openslice Logo Small](/uploads/images/openslice-logo-small.png "Openslice Logo Small")
The Patras Facility site portal is based on Openslice (https://osl.etsi.org) a prototype open source, operations support system. Up is the main contributor of OpenSlice. It supports VNF/NSD onboarding to OpenSourceMANO (OSM) and NSD deployment management. It also supports TMFORUM OpenAPIs regarding Service Catalog Management, Ordering, Resource, etc. Openslice offers the following main functionalities:

* 	Service Catalog Management: A CSP will have the ability to manage the Service Catalog Items, their attributes , organize in categories and decide what to make available to Customers
* 	Services Specifications: A CSP will be able to manage Service Specifications
* 	Service Catalog Exposure: A CSP will be able to expose catalog to customers and related parties
* 	Service Catalog to Service Catalog: Openslice able to consume and provide Service Catalog items to other catalogs
* 	Service Order: The Communication Service Customer will be able to place a Service Order
* 	Service Inventory: The Communication Service and Provider will be able to view deployed Services status

Openslice thus support both APIs for programmable access to the infrastructure as well as a web portal for user friendly access.


## Benefits

* Equipment Vendors: can participate in testbed construction and operations, satisfy the requirement to show interoperability at the neutral “playgrounds,” especially before the formal standardization. Enable collaboration with the vendors and supplier community
* Network Operators: Agile development cycles and easy evaluation of technologies.
* Standardization Bodies: Evaluate and compare ideas
* Academia: Researchers rely on experimentation for technology development and performance evaluation.
* Innovators: The can use it as a  playgrounds with minimal cost
* Open-source Communities: Develop features and capabilities, test, evaluate and compare ideas and technologies from other vendors


## Experimentation Process

Read more:
[Experimentation process](experimentation-process)
[Telemetry/Monitoring](telemetry-monitoring)
[Energy Measurement](telemetry-monitoring/energy-measurement)

## KPIs and Use Cases 

Check in this page some KPIs: [Patras5G-KPIs](Patras5G-KPIs)

##  Architecture and Components of the Facility Site 

Read more:
[Architecture and Components of the Patras/Greece Facility Site](architecture-and-components-)
[Radio equipment](radio-equipment)
[Available gNodeBs](radio-equipment/g-node-bs)
[Available UEs](radio-equipment/u-es)
[Other Devices](radio-equipment/other-devices)



##  Patras 5G Autonomous Edge
Read more:
[Patras 5G Autonomous Edge](5g-autonomous-edge)


## Service Catalogue and LCM of Network Slice Services

[Service Catalogue](service-catalogue)
[Support and LCM of Network Slice Services](support-and-lcm)
[Customer Facing Services](customer-facing-services)

[Demo VIdeo for onboarding and deployment of VNFs/NSDs](https://www.youtube.com/watch?v=3-fRuVfe2a4)


## The Patras5G coverage area
the following are the preliminary coverage plans of the facility

<img src="/uploads/images/patras-areaplansslide-1.png" width="640"><img src="/uploads/images/patras-areaplansslide-2.png" width="640"><img src="/uploads/images/patras-areaplansslide-3.png" width="640">


##  Patras5G University Campus coverage area
### Testing Area
The followign show a birds eye view of the campues with the location of the equipment and the testing area marked.

<img src="/uploads/images/coverage-1.png" width="640">

### Measurement points
This image shows the various points around the campous were actual measurements were taken with mobile devices.
The measuremenets are then stored along with other data like coordinates and can be retrieved to be shown on live interactive maps. (Link: TBD)

<img src="/uploads/images/coverage-2.png" width="640">


## The wider area of Patras city and Western Region

In Patras/Greece facility there will be Outdoor base stations to provide 5G and IoT coverage at locations of interest (where ICT19 vertical pilots will be enabled) both in the Patras campus and in the wider areas (see following two figures).

Next figure presents the campus area of the Patras main facility, which includes the largest hospital of western Greece as well as the Patras Science Park and Innohub that host many companies, organizations and technology start-ups. Outdoor base stations will be deployed across the main campus road (bold straight line in the figure) that leads to the hospital as well as other departments. To this end, a wide range of vertical scenarios could be hosted ranging from eHealth to automotive.
<img src="/uploads/images/patras-innohub.png" width="640">


Moreover, in the wider area of Patras city and Western Region (shown in the next figure) we depict key vertical industries and stakeholders that could be involved in potential vertical pilots. Some of these verticals that could be enabled are Sea ports, Smart agriculture and fish farming, smart city and critical infrastructures e.g. bridges and public buildings. These areas will be reached by either Intracom Telecom backhauling technology or Patras Optical MAN in order to be interconnected with the back end of the Patras facility and corresponding computational and communication resources.
<img src="/uploads/images/patras-area-map.png" width="640">



## Our partners

![Partners](/uploads/images/partners.png "Partners")


## Participating research projects

![Projects](/uploads/images/projects.png "Projects")

## Contact
Send an email to <b>info at patras5g.eu</b>

or see http://nam.ece.upatras.gr

-----
![Eu Flag](/uploads/images/eu-flag.png "Eu Flag")
Patras5G  has received funding from the European Horizon 2020 Programme for research, technological development and demonstration under grant agreements:
* 5GinFIRE n° 732497
* 5G-VINNI  n° 815279 
* 5G-SOLUTIONS n° 856691
* 5G-VICTORI n° 857201
* 5GASP n° 101016448
* 5G-INDUCE n° 101016941
