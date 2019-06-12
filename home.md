<!-- TITLE: Home -->
<!-- SUBTITLE: Welcome to Patras 5G Wiki -->

# Patras 5G wiki

The 5G-VINNI facility in Patras/Greece is an exemplary Open Source 5G-IoT facility. This means that most of the installed components will be offered as Open Source but there will be also dedicated components and services to support 5G-IoT scenarios. Numerous partners will deploy their technologies in the Patras/Greece facility, thus creating a unique 5G playground for KPI validation and support on future verticals.

The 5G-VINNI facility in Greece will be part of the Patras Platform for Experimentation lab (http://nam.ece.upatras.gr/ppe/). City of Patras has been recently selected by the Greek Ministry of Digital Policy, Telecommunications and Media, as one of the first two 5G pilot cities in Greece. Under this plan, 5G infrastructure will be deployed across the city to facilitate 5G trials and validate the effectiveness of the proposed architecture.

In Greece facility site the following tasks will be performed:

* Providing 5G standard-conformant components and Core Network infrastructure as extension of the FhG Open5GCore toolkit
* Provide ICOM’s mmWave backhaul to link the access to the core network, and Fixed Wireless Access to provide broadband services to the facility
* Integration of FhG Open5GCore with Limemicro SDR platform and the SRS UE and g/eNB
* Enabling the E2E deployment of multiple customized-slices over the whole network – access, transport and core. This will further include the slicing of the IoT devices at the edge of the network.
* Supporting MEC orchestration and mobility management features for the support of interactive mobile streaming edge services.

 Summary of capabilities

* Service Orchestration (via OSM NBI services)
* NFV MANO (OSM) and NFVI (OpenStack)+DPDK
* Slicing (Orchestration via OSM extensions, use of dedicated CN instances)
* 5G RAN open source radio (Lime, SRS)-700-800MHz, 3.5.-3.8GHz
* 5G Core (FhG Open5GCore)
* SDN (ODL)
* NB-IoT, LTE-M (FhG NB-IOT core)
* UEs based on Limemicro’s SDR and SRS software
* mmWave backhaul (Intracom)
* MEC support
* GEANT connectivity

## KPIs and Use Cases 
The Patras 5G testbed will focus on the validation of a series of KPIs, related to developed/deployed features and the selected use cases. On the generic NFV/MEC front and with respect to the available MANO features, validation will focus on the Latency, Energy, Throughput, Service Deployment Time KPIs. Related to the employed use cases, activities will also focus on Reliability (Service Continuity), Latency (Interactivity), Energy Efficiency and Throughput KPIs. Additional, qualitative/quantitative assessment activities will focus on validating resource and traffic isolation.

The set of use cases which will challenge the 5G-VINNI KPIs and will be targeted by the test plans are as follows:

*     Information society on the road (eMBB)
*     Collaborative gaming AR/VR (URLLC and eMBB)
*     Ultra-high fidelity media AR/VR (URLLS and eMBB)
*     Intelligent navigation (URLLC and eMBB)


##  Architecture and Components of the Facility Site 

### Access Network, MEC devices and UE

In Patras/Greece facility there will be 3 Outdoor base stations together with MEC devices at the Patras campus and at the City of Patras placed at properly selected places to facilitate the execution of test plans together with around 6 UEs. UoP together with ICOM will implement and integrate any standardized APIs and services to provide MEC functionality, including the virtualization of edge IoT devices, i.e., IoT Slicing, as a VIM component.

LimeMicro’s hardware will be used for both handset and base station. LimeMicro specialises in field programmable RF (FPRF) transceivers and open source LimeSDR, LimeNET platforms for the next generation of wireless broadband systems.  These products offer an unprecedented level of configurability and will be used in the Patras/Greece to create wireless communication networking equipment using commodity hardware, i.e., x86- based machines that can be programmable and reconfigured to run on any wireless communications frequency and mobile standards from 2G to 5G networks of the future.

SRS will integrate its software suite into the LimeMicro SDR hardware platform as well as interworking with the Fraunhofer open5Gcore will be assured.  SRS will provide a set of selected 5G NR features for srsLTE that will be available for KPI validation within the project. SRS will extend their code base for both UE and (g/e)NB to support the 5G NR scalable numerology for configurable subcarrier spacings, integrate the new channel coding, and higher order modulation types supported by 5G. This work will serve as a proof-of-concept and feasibility study of a SDR-based 5G NR implementation. We are intending to adopt the non-standalone (NSA) mode for 5G NR in which a NR gNB will provide user-plane traffic services for a NR-capable UE to a master 4G eNB.

### Backhaul

ICOM will provide to the Greek facility state-of-the-art mmWave backhaul and Fixed Wireless Access (FWA) solutions. The UltraLink™-GX80 all-outdoor mmWave PtP Ethernet radio at 70/80 GHz (E-Band), that provides a 10 Gbps backhaul capacity, will be used to interconnect the g/eNBs with the core network and the data centre at the UoP premises.

Further, ICOM’s FWA solutions will be used to provide broadband access to public organisations’ sites (e.g. University Campus, City Hall, etc.) in the city. The WiBAS™ OSDR PtMP all-outdoor radio, as it has been enhanced to provide >1.5 Gbps aggregate sector capacity and < 1 ms latency  through the phase 1 project SPEED-5G, will be used.

Within the project ICOM will add support for SDN-based network slicing to the wireless backhaul and FWA network segments..

### Cloud/MANO services

Currently, the Patras/Greece facility is equipped with a cloud platform offered by the University of Patras, able to host core network components, as well as NFV and MEC deployments. The cloud platform offers a total computing power of 212 CPUs and 768 Gigabytes of RAM and 30 TB of storage. Two servers with 4x10GbE NICs DPDK enabled will be also available.

On top of our cloud hardware, a rich set of state-of-the-art SW tools is already available, which comprises our platform for experimentation called Cloudville. These include OpenStack as the cloud operating system, while OSM (but also OpenBaton via FhG) will be available to allow NSD/VNF deployments.  Prometheus alongside with Grafana are installed for monitoring purposes. At the same time, Elastic search and Kibana are installed and being used to collect and visualize data extracted from IoT devices and sensors.

### Core 5G /IoT services

In Cloudville, apart from Service Slice life-cycle management services and OSM, the FhHG Open5G Core will be installed. The Fraunhofer Open5GCore implementation is a 5G oriented implementation of the core network (currently 3GPP Release 14 and 15, Release 16 planned in two years). The Open5GCore enables the connectivity service as requested within the 5G networks. To support NB-IoT, the Patras/Greece facility will host the Open5GCore NB-IoT extension, which is the first implementation of the essential 3GPP NB-IoT features (Release 13 ‑ TS 23.682) enabling the demonstration of low energy IoT communication. It addresses the current stringent needs of the 5G use cases to provide low power, low cost efficient communication for a massive number of devices. On the NBIoT, LTE-M radio side there will be both commercial licenced as well as open source solution available.

### MEC

The Patras/Greece facility will provide support for Mobile/Multi-access Edge Computing on two fronts:

(i) IoT Slicing: A Virtualized Infrastructure Management (VIM) (sub-)component will be designed, implemented and integrated within the overall MANO architecture, to enable the virtualization of the available edge IoT resources (sensors/actuators) for access within individual network slices.

(ii) Mobile streaming applications support: The facility will support MANO mechanisms for the realization of high throughput, low latency, mobile types of applications (e.g., gaming, AR/VR) and corresponding test cases. Such mechanisms will include DNS and traffic flow management (on Mp1 ETSI MEC interface) for baseline service orchestration, as well as mobility support mechanisms i.e., mobility management events such as application context transfer, user redirection network/application level), and a subset of the Location Service (ETSI GS MEC 013) for triggering mobility management events.


### Points of Interest that could be enabled with 5G and IoT coverage for supporting verticals.

In Patras/Greece facility there will be Outdoor base stations to provide 5G and IoT coverage at locations of interest (where ICT19 vertical pilots will be enabled) both in the Patras campus and in the wider areas (see following two figures).

Next figure presents the campus area of the Patras main facility, which includes the largest hospital of western Greece as well as the Patras Science Park and Innohub that host many companies, organizations and technology start-ups. Outdoor base stations will be deployed across the main campus road (bold straight line in the figure) that leads to the hospital as well as other departments. To this end, a wide range of vertical scenarios could be hosted ranging from eHealth to automotive.


Moreover, in the wider area of Patras city and Western Region (shown in the next figure) we depict key vertical industries and stakeholders that could be involved in potential vertical pilots. Some of these verticals that could be enabled are Sea ports, Smart agriculture and fish farming, smart city and critical infrastructures e.g. bridges and public buildings. These areas will be reached by either ICOM backhauling technology or Patras Optical MAN in order to be interconnected with the back end of the Patras facility and corresponding computational and communication resources.


-----
![Eu Flag](/uploads/images/eu-flag.png "Eu Flag")
5GinFIRE project has received funding from the European Horizon 2020 Programme for research, technological development and demonstration under grant agreement n° 732497
