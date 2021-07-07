<!-- TITLE: Home -->
<!-- SUBTITLE: Welcome to Patras 5G Wiki -->


<img src="/uploads/patras-5-g-logo.png" width="320">
# Patras 5G wiki

**The Patras 5G facility is an "isolated" Non-public Network for 5G and IoT applications.**

Most of the installed components are offered as Open Source but there are also dedicated components and services to support 5G and IoT scenarios. Numerous partners have deployed their technologies in the Patras 5G /Greece facility, thus creating a unique 5G playground for KPI validation and support on future verticals. For more information please check http://wiki.patras5g.eu/ )

In Greece facility site the following tasks are performed:

* Providing 5G standard-conformant components and Core Network infrastructure as extension of the FhG Open5GCore toolkit
* Provide Intracom Telecom mmWave backhaul to link the access to the core network, and Fixed Wireless Access to provide broadband services to the facility
* Integration of FhG Open5GCore with Limemicro SDR platform and the SRS UE and g/eNB
* Enabling the E2E deployment of multiple customized-slices over the whole network – access, transport and core. This will further include the slicing of the IoT devices at the edge of the network.
* Supporting MEC orchestration and mobility management features for the support of interactive mobile streaming edge services.

## Demo videos


5G end-to-end experimentation: From Service Order to Network Monitoring Service https://www.youtube.com/watch?v=X662lml0p8w
5G-VINNI Patras Facility [video](https://www.youtube.com/watch?v=rASfEuHzhW0) for a quick presentation


## Patras 5G facility infrastructure: Onboarding and access for Vertical Applications

<img src="/uploads/onboarding-overview.png" width="1024">

**Summary of capabilities**
With our OSS, NFV and experimentation enabled services, like Openslice and Open Source MANO, we enable E2E automated deployment of multiple customized-slices over the whole network – access, transport and core. This further includes the slicing of the IoT devices at the edge of the network. Patras 5G facility is equipped with a cloud platform, able to host core network components, as well as NFV and MEC deployments. The cloud platform offers a total computing power of 300 CPUs and 1TB of RAM and 50 TB of storage. 10GbE NICs DPDK enabled are also available. Patras 5G provides 5G standard-conformant components and Core Network infrastructure and Integration of 5G Core and 5G RAN with our Opensource based NFV platform.  We support various flavors and installations of the 5G System, that are both NSA and SA depending on the scenarios that the customer 
* 	5G Core and EPC solutions that are available and can be orchestrated in the facility:  FhG Open5GCore, AMARISOFT EPC, SRS EPC, NextEPC
* 	5G and 4G RAN: AMARISOFT 5G RAN (Classic boxes), 5G RAN open source radio (Lime, SRS)-700-800MHz, 3.5.-3.8GHz, 4G NB-IoT, LTE-M (FhG NB-IOT core) based on AMARISOFT, Various SDR equipment (ETTUS)
* 	UEs based on Limemicro’s SDR and SRS software, as well as commercial UEs: Mobile phones LG and Samsung, Huawei CPE, Various SDR equipment, a Drone for URLLC testing
* 	Monitoring is available through: Graphana, Prometheus,Netdata while OSM also configure with VNF telemetry support
* 	Patras 5G has mmWave backhaul to link the access to the core network, and Fixed Wireless Access to provide broadband services to the facility from various locations in the region of Patras and beyond. 
* 	GEANT connectivity is also available


Vertical applications can access the Patras 5G Service Catalogue through the Patras Facility site portal: https://patras5g.eu .  Vertical applications can self-manage and onboard their artifacts through our portal or access programmatically available services.
Various artifacts can be managed through the facility portal https://patras5g.eu via standardized TMForum OpenAPIs: Service Catalog,  Service Order and Service Inventory, Partner Management and Users, Service Orchestration, VNFs/NSDs catalogue, NFVO endpoints via OSM NBI, Service and NFV Deployment requests. 

![Openslice Logo Small](/uploads/images/openslice-logo-small.png "Openslice Logo Small")
The Patras Facility site portal is based on Openslice (http://openslice.io) a prototype open source, operations support system. Up is the main contributor of OpenSlice. It supports VNF/NSD onboarding to OpenSourceMANO (OSM) and NSD deployment management. It also supports TMFORUM OpenAPIs regarding Service Catalog Management, Ordering, Resource, etc. Openslice offers the following main functionalities:

* 	Service Catalog Management: A CSP will have the ability to manage the Service Catalog Items, their attributes , organize in categories and decide what to make available to Customers
* 	Services Specifications: A CSP will be able to manage Service Specifications
* 	Service Catalog Exposure: A CSP will be able to expose catalog to customers and related parties
* 	Service Catalog to Service Catalog: Openslice able to consume and provide Service Catalog items to other catalogs
* 	Service Order: The Communication Service Customer will be able to place a Service Order
* 	Service Inventory: The Communication Service and Provider will be able to view deployed Services status

Openslice thus support both APIs for programmable access to the infrastructure as well as a web portal for user friendly access.



## Experimentation Process

Read more:
[Experimentation process](experimentation-process)
[Telemetry/Monitoring](telemetry-monitoring)

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

<img src="/uploads/images/patras-areaplansslide-1.png" width="1024">
<img src="/uploads/images/patras-areaplansslide-2.png" width="1024">
<img src="/uploads/images/patras-areaplansslide-3.png" width="1024">


##  Patras5G University Campus coverage area
### Testing Area
The followign show a birds eye view of the campues with the location of the equipment and the testing area marked.
![Coverage 1](/uploads/images/coverage-1.png "Coverage 1")

### Measurement points
This image shows the various points around the campous were actual measurements were taken with mobile devices.
The measuremenets are then stored along with other data like coordinates and can be retrieved to be shown on live interactive maps. (Link: TBD)

![Coverage 2](/uploads/images/coverage-2.png "Coverage 2")


## The wider area of Patras city and Western Region

In Patras/Greece facility there will be Outdoor base stations to provide 5G and IoT coverage at locations of interest (where ICT19 vertical pilots will be enabled) both in the Patras campus and in the wider areas (see following two figures).

Next figure presents the campus area of the Patras main facility, which includes the largest hospital of western Greece as well as the Patras Science Park and Innohub that host many companies, organizations and technology start-ups. Outdoor base stations will be deployed across the main campus road (bold straight line in the figure) that leads to the hospital as well as other departments. To this end, a wide range of vertical scenarios could be hosted ranging from eHealth to automotive.
![patras-innohub](/uploads/images/patras-innohub.png "patras-innohub")


Moreover, in the wider area of Patras city and Western Region (shown in the next figure) we depict key vertical industries and stakeholders that could be involved in potential vertical pilots. Some of these verticals that could be enabled are Sea ports, Smart agriculture and fish farming, smart city and critical infrastructures e.g. bridges and public buildings. These areas will be reached by either Intracom Telecom backhauling technology or Patras Optical MAN in order to be interconnected with the back end of the Patras facility and corresponding computational and communication resources.
![patras-area-map](/uploads/images/patras-area-map.png "patras-area-map")


## Contact

See http://nam.ece.upatras.gr

-----
![Eu Flag](/uploads/images/eu-flag.png "Eu Flag")
Patras5G  has received funding from the European Horizon 2020 Programme for research, technological development and demonstration under grant agreement n° 732497
