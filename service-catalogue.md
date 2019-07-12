<!-- TITLE: Service Catalogue -->
<!-- SUBTITLE: Service Catalogue -->

# Service Catalogue

The Service Catalogue is a feature that will be exposed by the facility site portal and will contain various service offerings of the facility site. These service offerings will be delivered under the Network Slice as a Service (NSaaS) model. This model relies on the deployment of NSIs and their delivery towards 5G-VINNI customers, allowing them to build on top their own services and carry out experimentation activities on them.

The Service Catalogue is maintained by the facility site (CSP) via the facility site portal user interface, where the facility site can define its service offerings through 5G-VINNI Service Blueprints (VINNI-SBs). 
5G-VINNI Customers can define requirements through service descriptors, which contain specific attributes of a Service Blueprint for the specific customer.
The Service Catalogue will also expose an API based on TM Forums OpenAPIs [OpenAPI]: 
–	TMF633 Service Catalogue Management API 
–	TMF641 Service Ordering
Since the facility uses OSM, the Service Catalogue utilizes the SOL005 NBI API of OSM to expose Network Service Descriptors (NDSs) as well as Network Slices Templates (NSTs). The Service Catalogue performs transformations from the ETSI defined models as used by OSM for describing VNF, NS descriptors (SOL001, SOL004, SOL006) and the slicing templates defined by OSM to the TM Forum OpenAPIs models. 




