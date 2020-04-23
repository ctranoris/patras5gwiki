<!-- TITLE: Experimentation Process -->
<!-- SUBTITLE: Patras5G Experimentation Process -->

# Experimentation Process

## Patras5G Access

Patras5G facility adopts the Network Slice as a Service (NSaaS) delivery model, whereby the Patras5G facility provisions tailored network slices to verticals upon request. Each vertical uses the slice that has been provided to meet their requirements for trialling activities, setting up different use cases and assessing their KPIs under different network conditions.
Patras5G facility incorporates into its architecture the guidelines from telecom industry organisations and the normative specifications from standards bodies to ensure interoperability and reproducibility. The Patras5G facility is based on Openslice (http://openslice.io)  which allows NSaaS delivery model is shown in next Figure, where the Patras5G portal and service catalogue expose TM Forum Open APIs towards verticals to allow them to directly trigger necessary operations for service ordering. The Patras5G Service Catalogue derives content from Patras5G Facility Service Catalogue offerings. The vertical's service order is then passed to the Service Orchestrator (SO) in Patras5G facility. The SO then instantiates the network slice by subsequent calls to the respective network function orchestrator (NFVO). The NFVO implements the northbound interface using ETSI SOL 005. This normative specification defines the protocol and data model for the interface capabilities in the form of RESTful APIs which have become de-facto solutions for most of the industrial and open-source NFVOs.


![Onboarding Process Service Access](/uploads/onboarding/onboarding-process-service-access.png "Onboarding Process Service Access")

### Service Exposure Level of Patras5G

See next section about the Exposure Level definition.

The Patras5G exposes all Levels under different circumstances and requirements. This depends on the customer use cases and needs.

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


( Our process is based from the whitepaper https://doi.org/10.5281/zenodo.3695716  )

![Onboarding Process](/uploads/onboarding/onboarding-process.png "Onboarding Process")



