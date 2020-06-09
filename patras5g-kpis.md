<!-- TITLE: Patras 5G KPIs -->
<!-- SUBTITLE: A quick summary of Patras 5G KPIs -->

# Patras 5G KPIs

The Patras 5G testbed focuses on the validation of a series of KPIs, related to developed/deployed features and the selected use cases. 
*major parts are based on 5G PPP phase II KPIs definitions/3GPP/NGMN/ITU as described*


## Peak throughput for Single Network Slice Instance

| Related Definition    | Description | Definition |
|-----------------|-------|-------|
|190802_NGMN-PreCommTrials_Framework_definition_v3.0  | 5G is expected to provide significant improvement in the context of peak data rates (on both UL and DL). 5G data rate requirements are in the order of 100 Mbps to 1 Gbps for user experienced data rate, with peaks of 10 Gbps data rate. This leads to an improvement needed (compared to LTE Rel’12) to meet NGMN requirements in the order of > 10x. The purpose of this test is to verify peak DL and UL UE data rate provided by 5G system. | Peak user throughput is the maximum DL/UL data rate achievable for a single user located at the best location within a cell.|

### Test environment

####Test Configuration: 

Conf. 1 (eMBB service)

| BS            | Mode    | UE                                           | Commands                                       | 
|---------------|---------|----------------------------------------------|-------------------------------------------------|
| Amarisoft 5G, | NSA/TDD | **Huawei CPE** (Samsung A90 connected via Wifi), | iperf3 -s -i 1 -u                               |
|               |         |                                              | iperf3 -c   192.168.3.2  -i 1 -u -b 300M -t 100 |                                           |                        |   |   |   |



| Bandwidth (MHz) | MIMO  | Downlink UDP | Uplink UDP | Down TCP    | Uplink TCP | speedtest GRNET multi down | GRNET multi UP                                |
|-----------------|-------|--------------|------------|-------------|------------|----------------------------|-----------------------------------------------|
| 50              | 2x2   | 272          | 18,5       | 50,6        | 18,7       | 232                        | 29,4                                          |
| 50              | 1x1   | 185          | 8,7        | 48,7        | 13         | 167                        | 4,4                                           |
| 40              | 2x2   | 215          | 20,4       | 51,2        | 24,9       | 202                        | 24,4                                          |
    

Test Configuration: 
Conf. 1 (eMBB service)


| BS            | Mode    | UE                                           | Commands                                       | 
|---------------|---------|----------------------------------------------|-------------------------------------------------|
| Amarisoft 5G, | NSA/TDD | **Samsung A90** | iperf3 -s -i 1 -u                               |
|               |         |                                              | iperf3 -c   192.168.3.2  -i 1 -u -b 300M -t 100 |                                           |                        |   |   |   |



| Bandwidth (MHz) | MIMO  | Downlink UDP | Uplink UDP | Down TCP    | Uplink TCP | speedtest GRNET multi down | GRNET multi UP                                |
|-----------------|-------|--------------|------------|-------------|------------|----------------------------|-----------------------------------------------|
| 50              | 2x2   | 291          | 32,6       | 162         | 22,1       | 212                        | 29,8                                          |
| 50              | 1x1   | 184          | 17,3       | 180         | 16,8       | 170                        | 18,6                                          |
| 40              | 2x2   | 213          | 23,4       | 146         | 25,1       | 202                        | 25,7                                          |



## Service Deployment Time




On the generic NFV/MEC front and with respect to the available MANO features, validation will focus on the Latency, Energy, Throughput, Service Deployment Time KPIs. Related to the employed use cases, activities will also focus on Reliability (Service Continuity), Latency (Interactivity), Energy Efficiency and Throughput KPIs. Additional, qualitative/quantitative assessment activities will focus on validating resource and traffic isolation.

The set of use cases which will challenge the 5G-VINNI KPIs and will be targeted by the test plans are as follows:

* Information society on the road (eMBB)
* Collaborative gaming AR/VR (URLLC and eMBB)
* Ultra-high fidelity media AR/VR (URLLS and eMBB)
* Intelligent navigation (URLLC and eMBB)
