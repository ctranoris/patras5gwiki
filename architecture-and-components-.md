<!-- TITLE: Architecture And Components -->
<!-- SUBTITLE: A quick summary of Architecture And Components -->

# Architecture And Components of Patras5G


![greeksitearch](/uploads/images/greece-site.png "greeksitearch")


### Cloud/MANO services

Currently, the Patras/Greece facility is equipped with a cloud platform offered by the University of Patras, able to host core network components, as well as NFV and MEC deployments. The cloud platform offers a total computing power of 1512 CPUs and 3520 Gigabytes of RAM and 30 TB of storage. Two servers with 4x10GbE NICs DPDK enabled will be also available.

On top of our cloud hardware, a rich set of state-of-the-art SW tools is already available, which comprises our platform for experimentation called Cloudville. These include OpenStack as the cloud operating system but also a Kubernetes cluster install over Openstack, while OSM (but also OpenBaton via FhG) will be available to allow NSD/VNF deployments.  Prometheus alongside with Grafana are installed for monitoring purposes. At the same time, Elastic search and Kibana are installed and being used to collect and visualize data extracted from IoT devices and sensors.



### Access Network, MEC devices and UE

In Patras/Greece facility there will be 3 Outdoor base stations together with MEC devices at the Patras campus and at the City of Patras placed at properly selected places to facilitate the execution of test plans together with around 6 UEs. UoP together with ICOM will implement and integrate any standardized APIs and services to provide MEC functionality, including the virtualization of edge IoT devices, i.e., IoT Slicing, as a VIM component.

LimeMicro’s hardware will be used for both handset and base station. LimeMicro specialises in field programmable RF (FPRF) transceivers and open source LimeSDR, LimeNET platforms for the next generation of wireless broadband systems.  These products offer an unprecedented level of configurability and will be used in the Patras/Greece to create wireless communication networking equipment using commodity hardware, i.e., x86- based machines that can be programmable and reconfigured to run on any wireless communications frequency and mobile standards from 2G to 5G networks of the future.

SRS will integrate its software suite into the LimeMicro SDR hardware platform as well as interworking with the Fraunhofer open5Gcore will be assured.  SRS will provide a set of selected 5G NR features for srsLTE that will be available for KPI validation within the project. SRS will extend their code base for both UE and (g/e)NB to support the 5G NR scalable numerology for configurable subcarrier spacings, integrate the new channel coding, and higher order modulation types supported by 5G. This work will serve as a proof-of-concept and feasibility study of a SDR-based 5G NR implementation. We are intending to adopt the non-standalone (NSA) mode for 5G NR in which a NR gNB will provide user-plane traffic services for a NR-capable UE to a master 4G eNB.

See more:

[Radio equipment](radio-equipment)
[Available gNodeBs](radio-equipment/g-node-bs)
[Available UEs](radio-equipment/u-es)
[Other Devices](radio-equipment/other-devices)


### Backhaul

ICOM  provides to the Greek facility state-of-the-art mmWave backhaul and Fixed Wireless Access (FWA) solutions. The UltraLink™-GX80 all-outdoor mmWave PtP Ethernet radio at 70/80 GHz (E-Band), that provides a 10 Gbps backhaul capacity, will be used to interconnect the g/eNBs with the core network and the data centre at the UoP premises.

Further, ICOM’s FWA solutions will be used to provide broadband access to public organisations’ sites (e.g. University Campus, City Hall, etc.) in the city. The WiBAS™ OSDR PtMP all-outdoor radio, as it has been enhanced to provide >1.5 Gbps aggregate sector capacity and < 1 ms latency  through the phase 1 project SPEED-5G, will be used.

Within the project ICOM will add support for SDN-based network slicing to the wireless backhaul and FWA network segments..

<img src="/uploads/radio-equipment/pilaradmhe-02.png" width="1024">

 ![Img 20200506 16392](/uploads/radio-equipment/img-20200506-16392.jpg "Img 20200506 16392")

### Core 5G /IoT services

In Cloudville, apart from Service Slice life-cycle management services and OSM, the FhHG Open5G Core will be installed. The Fraunhofer Open5GCore implementation is a 5G oriented implementation of the core network (currently 3GPP Release 14 and 15, Release 16 planned in two years). The Open5GCore enables the connectivity service as requested within the 5G networks. To support NB-IoT, the Patras/Greece facility will host the Open5GCore NB-IoT extension, which is the first implementation of the essential 3GPP NB-IoT features (Release 13 ‑ TS 23.682) enabling the demonstration of low energy IoT communication. It addresses the current stringent needs of the 5G use cases to provide low power, low cost efficient communication for a massive number of devices. On the NBIoT, LTE-M radio side there will be both commercial licenced as well as open source solution available.

### MEC

The Patras/Greece facility will provide support for Mobile/Multi-access Edge Computing on two fronts:

(i) IoT Slicing: A Virtualized Infrastructure Management (VIM) (sub-)component will be designed, implemented and integrated within the overall MANO architecture, to enable the virtualization of the available edge IoT resources (sensors/actuators) for access within individual network slices.

(ii) Mobile streaming applications support: The facility will support MANO mechanisms for the realization of high throughput, low latency, mobile types of applications (e.g., gaming, AR/VR) and corresponding test cases. Such mechanisms will include DNS and traffic flow management (on Mp1 ETSI MEC interface) for baseline service orchestration, as well as mobility support mechanisms i.e., mobility management events such as application context transfer, user redirection network/application level), and a subset of the Location Service (ETSI GS MEC 013) for triggering mobility management events.



