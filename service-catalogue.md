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

![Service Catalog Osm](/uploads/images/service-catalog-osm.png "Service Catalog Osm")

## Definition and on-boarding of VNF, NSD descriptors to the different service catalogues
Two roles will be able to upload VFN and NS descriptors and define slices to be onboarded in the facility site, the customer (CSC) and the provider (CSP).  CSC as well as the CSP will use the facility portal to maintain and on-board different artifacts. The facility site portal mainly:
•	holds information about User data and roles retrieved from other repositories like OSM Keystone 
•	holds information about VNF, NSD, Slices.
•	Utilizes the OSM repository/catalogues via the OSM SOL005 NBI API.
•	Categorizes artifacts
The facility site portal implements the RESTful protocols specification for the Os-Ma-nfvo Reference Point. The portal will utilize:  
3.2.1.1	NS and VNF Package Management
REST wrapper for the NS and VNF package service via resource Descriptors. Provides methods for onboarding, updating and downloading NS and VNF packages.
## VNF Descriptor Management 
REST wrapper for VNFD descriptor management provides methods for onboarding, updating, querying, and deleting a VNF descriptor through the Individual resource Descriptors and Content.
## 	VNF Lifecycle Management
REST wrapper for the VNF lifecycle management service. Provides methods for querying a VNF and retrieving VNF records via resource Descriptors.
## 	Network Service Descriptor Management
REST wrapper for the NSD service (via resource Descriptors). Provides methods for onboarding, updating, querying, and deleting a network service descriptor.
## 	Network Service Lifecycle Management
REST wrapper for network service lifecycle management. Provides methods for instantiating, updating, finding, and terminating a network service (NFV-NS). Also provides methods for creating, updating, listing, and deleting or VNF forwarding graph (VNFFG). This will be implemented via the NS Lifecycle Management interface. 
## 	Network Slice Template Lifecycle Management
REST wrapper for network slice template lifecycle management. Provides methods for instantiating, updating, finding, and terminating a NST. 
## 	Hosting of third party VNFs and Images management
3rd party VNFs can by on-boarded through the portal. However, VNF Images are uploaded to the facility site only from the Network Operator that has also access to the VIM. The customer must request the upload of VNF Images and also provide any licensing details.
## 	VNF, NSD validation
The facility site portal makes a validation in terms of packaging compliance and modeling. The facility site portal currently supports descriptors following the ETSI proposed YANG models (e.g. SOL001, SOL004, SOL006).
## 	VNF upgrade/migration/suspension issues and dependencies with NSDs
Deployed NSDs depend on specific on-boarded VNFs. Currently it is not possible to upgrade these VNFs due to dependencies.



