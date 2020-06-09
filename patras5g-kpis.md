<!-- TITLE: Patras 5G KPIs -->
<!-- SUBTITLE: A quick summary of Patras 5G KPIs -->

# Patras 5G KPIs

The Patras 5G testbed focuses on the validation of a series of KPIs, related to developed/deployed features and the selected use cases. 
*major parts are based on 5G PPP phase II KPIs definitions/3GPP/NGMN/ITU as described*


# Peak throughput for Single Network Slice Instance

| Related Standard/Definition    | Definition | Description |
|-----------------|-------|-------|
|190802_NGMN-PreCommTrials_Framework_definition_v3.0  | Peak user throughput is the maximum DL/UL data rate achievable for a single user located at the best location within a cell. | 5G is expected to provide significant improvement in the context of peak data rates (on both UL and DL). 5G data rate requirements are in the order of 100 Mbps to 1 Gbps for user experienced data rate, with peaks of 10 Gbps data rate. This leads to an improvement needed (compared to LTE Rel’12) to meet NGMN requirements in the order of > 10x. The purpose of this test is to verify peak DL and UL UE data rate provided by 5G system.|

## Test environment

###Test Configuration 1: 

Conf. 1 (eMBB service)
Location: Indoor
Distance: ~3m


| BS            | Mode    | UE                                           | Commands                                       | 
|---------------|---------|----------------------------------------------|-------------------------------------------------|
| Amarisoft 5G, | NSA/TDD | **Huawei CPE** (Samsung A90 connected via Wifi), | iperf3 -s -i 1 -u                               |
|               |         |                                              | iperf3 -c   192.168.3.2  -i 1 -u -b 300M -t 100 |                                           |                        |   |   |   |



| Bandwidth (MHz) | MIMO  | Downlink UDP | Uplink UDP | Down TCP    | Uplink TCP | speedtest GRNET multi down | GRNET multi UP                                |
|-----------------|-------|--------------|------------|-------------|------------|----------------------------|-----------------------------------------------|
| 50              | 2x2   | 272          | 18,5       | 50,6        | 18,7       | 232                        | 29,4                                          |
| 50              | 1x1   | 185          | 8,7        | 48,7        | 13         | 167                        | 4,4                                           |
| 40              | 2x2   | 215          | 20,4       | 51,2        | 24,9       | 202                        | 24,4                                          |
    

###Test Configuration 2: 
Conf. 1 (eMBB service)
Location: Indoor
Distance: ~3m

| BS            | Mode    | UE                                           | Commands                                       | 
|---------------|---------|----------------------------------------------|-------------------------------------------------|
| Amarisoft 5G, | NSA/TDD | **Samsung A90** | iperf3 -s -i 1 -u                               |
|               |         |                                              | iperf3 -c   192.168.3.2  -i 1 -u -b 300M -t 100 |                                           |                        |   |   |   |



| Bandwidth (MHz) | MIMO  | Downlink UDP | Uplink UDP | Down TCP    | Uplink TCP | speedtest GRNET multi down | GRNET multi UP                                |
|-----------------|-------|--------------|------------|-------------|------------|----------------------------|-----------------------------------------------|
| 50              | 2x2   | 291          | 32,6       | 162         | 22,1       | 212                        | 29,8                                          |
| 50              | 1x1   | 184          | 17,3       | 180         | 16,8       | 170                        | 18,6                                          |
| 40              | 2x2   | 213          | 23,4       | 146         | 25,1       | 202                        | 25,7                                          |


### Test procedure

The following test procedure define the peak UL/DL data rate test:

1. Coverage of the test area defined as Received RSRP > -60 dBm and SINR > 22dB as measured with measurement tool.
2. Identify a location(s) where combination of highest MIMO rank, modulation and coding rate can be attained with stability.
3. Ensure that there are no UEs connected in any of the surrounding cells.
4. Repeat steps 5-6 at each location with the UE static in that location.
5. Connect 1 UE to the sector and ensure there is only this UE connected to the sector.
6. Measure L1 and PDCP layer throughput
a. If dynamic UL/DL ratio is not supported, reconfigure the system for minimum UL DL/UL ratio
b. Download to the UE using UDP or TCP (using iperf) for DL peak test
c. Measure PDCP layer throughput (PDCP throughput is payload bits divided by the aggregated time) and
L1 throughput using measurement tool; session duration should be at least 2 minutes; max./min./avg.
value should be reported
If dynamic UL/DL ratio is not supported, reconfigure the system for minimum DL DL/UL ratio
d. Upload to the test server using UDP or TCP (using iperf) for UL peak test
e. Measure PDCP layer throughput (PDCP throughput is payload bits divided by the aggregated time) and
L1 throughput using measurement tool; session duration should be at least 2 minutes; max./min./avg.
value should be reported.


### Logging at gNB side and UE side
On UE side, the following metrics should be available for performance assessment:

- DL throughput (L1 and PDCP throughput)
- UL throughput (L1 and PDCP throughput)
- RSRP (Reference Signal Received Power)
- RSRQ (Reference Signal Received Quality)
- SINR
- DL BLER (at first retransmission)
- MIMO mode used (incl. MIMO rank)

# Service Deployment Time


| Related Standard/Definition    | Definition | Description |
|-----------------|-------|-------|
| xxx  | xxx| xxx |

## Test environment

###Test Configuration 1: 


### Test procedure

The following test procedure define the xxx:



### Logging at XXXX (e.g.  gNB side and UE side, Core, NFVI, etc)



