<!-- TITLE: Patras 5G KPIs -->
<!-- SUBTITLE: A quick summary of Patras 5G KPIs -->

# Patras 5G KPIs

The Patras 5G testbed focuses on the validation of a series of KPIs, related to developed/deployed features and the selected use cases. 
*major parts are based on 5G PPP phase II KPIs definitions*





Huawei CPE

| Amarisoft 5G    | Mode: | NSA/TDD      | UE:        | Samsung A90 | Commands:  | iperf3 -s -i 1 -u          | iperf3 -c 192.168.3.2  -i 1 -u -b 300M -t 100 |
|-----------------|-------|--------------|------------|-------------|------------|----------------------------|-----------------------------------------------|
| Bandwidth (MHz) | MIMO  | Downlink UDP | Uplink UDP | Down TCP    | Uplink TCP | speedtest GRNET multi down | GRNET multi UP                                |
| 50              | 2x2   | 272          | 18,5       | 50,6        | 18,7       | 232                        | 29,4                                          |
| 50              | 1x1   | 185          | 8,7        | 48,7        | 13         | 167                        | 4,4                                           |
| 40              | 2x2   | 215          | 20,4       | 51,2        | 24,9       | 202                        | 24,4                                          |
    



SAMSUNG A90

| Amarisoft 5G    | Mode: | NSA/TDD      | UE:        | Samsung A90 | Commands:  | iperf3 -s -i 1 -u          | iperf3 -c 192.168.3.2  -i 1 -u -b 300M -t 100 |
|-----------------|-------|--------------|------------|-------------|------------|----------------------------|-----------------------------------------------|
| Bandwidth (MHz) | MIMO  | Downlink UDP | Uplink UDP | Down TCP    | Uplink TCP | speedtest GRNET multi down | GRNET multi UP                                |
| 50              | 2x2   | 291          | 32,6       | 162         | 22,1       | 212                        | 29,8                                          |
| 50              | 1x1   | 184          | 17,3       | 180         | 16,8       | 170                        | 18,6                                          |
| 40              | 2x2   | 213          | 23,4       | 146         | 25,1       | 202                        | 25,7                                          |



## Service Delpoyment Time




On the generic NFV/MEC front and with respect to the available MANO features, validation will focus on the Latency, Energy, Throughput, Service Deployment Time KPIs. Related to the employed use cases, activities will also focus on Reliability (Service Continuity), Latency (Interactivity), Energy Efficiency and Throughput KPIs. Additional, qualitative/quantitative assessment activities will focus on validating resource and traffic isolation.

The set of use cases which will challenge the 5G-VINNI KPIs and will be targeted by the test plans are as follows:

* Information society on the road (eMBB)
* Collaborative gaming AR/VR (URLLC and eMBB)
* Ultra-high fidelity media AR/VR (URLLS and eMBB)
* Intelligent navigation (URLLC and eMBB)
