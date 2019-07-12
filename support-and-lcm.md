<!-- TITLE: Support and LCM of Network Slice Services -->
<!-- SUBTITLE: Support and LCM of Network Slice Services -->

# Support and LCM of Network Slice Services
![Vinni Sb Structure](/uploads/images/vinni-sb-structure.png "Vinni Sb Structure")

CSP will expose a number of VINNI-SBs towards CSCs. These VINNI-SBs represents service offerings against which CSCs can issue service orders for the delivery of network slice services. The structure of any VINNI-SB is extensively discussed in [Deliverable 3.1](https://www.5g-vinni.eu/deliverables/) of 5G-VINNI project As shown in Figure, VINNI-SB consists of four main parts:
•	Service type: provides a high-level description of the slice service to be provided from this VINNI-SB. Any VINNI-SB must specify one of the following options: enhanced Mobile Broadband (eMBB), ultra-Reliable Low Latency Communication (uRLLC), massive IoT (mIoT) and customised. 
•	Service topology: specifies the functional nodes of the slices and their associated topology. Each of this functional node is referred to as a Service Component (SC), each being a unified abstraction of a given network functionality. SCs are technology-agnostic, modular, and can be easily chained to form different topologies, being these topologies flexibly extended (or even modified) with the attachment of 3rd party VNFs. The topology presented in a VINNI-SB and its possibilities of extension (or even modification) are highly dependent on the service type the VINNI-SB refers to. 
•	Service requirements: specifies the requirements of the slice service to be provided from the VINNI-SB. These requirements include i) performance requirements, ii) functional requirements and iii) network optimisation requirements. The requirements presented in a VINNI-SB are highly dependent on the service type the VINNI-SB refers to. 
Service exposure, monitoring and testing: specifies the service capability exposure made available to the CSC. This exposure is based on a four-level classification, with each higher level allowing the CSC to gain access to a lower abstraction management entity. Depending on the selected level, the CSC can consume management data (e.g. performance measurements, fault data) and trigger enabled management operations (e.g. LCM) at different abstraction layers, which is relevant for testing and monitoring activities conducted at run-time. 

