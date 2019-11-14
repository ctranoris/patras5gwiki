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

Check this [video](https://www.youtube.com/watch?v=rASfEuHzhW0) for a quick presentation

## KPIs and Use Cases 
The Patras 5G testbed will focus on the validation of a series of KPIs, related to developed/deployed features and the selected use cases. On the generic NFV/MEC front and with respect to the available MANO features, validation will focus on the Latency, Energy, Throughput, Service Deployment Time KPIs. Related to the employed use cases, activities will also focus on Reliability (Service Continuity), Latency (Interactivity), Energy Efficiency and Throughput KPIs. Additional, qualitative/quantitative assessment activities will focus on validating resource and traffic isolation.

The set of use cases which will challenge the 5G-VINNI KPIs and will be targeted by the test plans are as follows:

* Information society on the road (eMBB)
* Collaborative gaming AR/VR (URLLC and eMBB)
* Ultra-high fidelity media AR/VR (URLLS and eMBB)
* Intelligent navigation (URLLC and eMBB)


##  Architecture and Components of the Facility Site 

Read more:
[Architecture and Components of the Patras/Greece Facility Site](architecture-and-components-)


## Service Catalogue and LCM of Network Slice Services

[Service Catalogue](service-catalogue)
[Support and LCM of Network Slice Services](support-and-lcm)
[Customer Facing Services](customer-facing-services)

[Demo VIdeo for onboarding and deployment of VNFs/NSDs](https://www.youtube.com/watch?v=3-fRuVfe2a4)


## The Patras5G coverage area
the following are the preliminary coverage plans of the facility

![Patras Areaplansslide 1](/uploads/images/patras-areaplansslide-1.png "Patras Areaplansslide 1")
![Patras Areaplansslide 2](/uploads/images/patras-areaplansslide-2.png "Patras Areaplansslide 2")
![Patras Areaplansslide 3](/uploads/images/patras-areaplansslide-3.png "Patras Areaplansslide 3")




## The wider area of Patras city and Western Region

In Patras/Greece facility there will be Outdoor base stations to provide 5G and IoT coverage at locations of interest (where ICT19 vertical pilots will be enabled) both in the Patras campus and in the wider areas (see following two figures).

Next figure presents the campus area of the Patras main facility, which includes the largest hospital of western Greece as well as the Patras Science Park and Innohub that host many companies, organizations and technology start-ups. Outdoor base stations will be deployed across the main campus road (bold straight line in the figure) that leads to the hospital as well as other departments. To this end, a wide range of vertical scenarios could be hosted ranging from eHealth to automotive.
![patras-innohub](/uploads/images/patras-innohub.png "patras-innohub")


Moreover, in the wider area of Patras city and Western Region (shown in the next figure) we depict key vertical industries and stakeholders that could be involved in potential vertical pilots. Some of these verticals that could be enabled are Sea ports, Smart agriculture and fish farming, smart city and critical infrastructures e.g. bridges and public buildings. These areas will be reached by either ICOM backhauling technology or Patras Optical MAN in order to be interconnected with the back end of the Patras facility and corresponding computational and communication resources.
![patras-area-map](/uploads/images/patras-area-map.png "patras-area-map")

-----
![Eu Flag](/uploads/images/eu-flag.png "Eu Flag")
5GinFIRE project has received funding from the European Horizon 2020 Programme for research, technological development and demonstration under grant agreement n° 732497
