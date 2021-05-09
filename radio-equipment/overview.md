<!-- Radio Equipment -->
<!-- Overview of the radio equipment used in Patars 5G facility.-->

# Overview



| RADIO EQUIPMENT|                    |                   |
| -----------------------| -------------| ----------- |
| TYPE                          | MODEL       |DETAILS       |
| [gNodeB ](#gNodeB) | Amarisoft Classic <br>   LimeNET Crowd Cell   <br> LimeNet <br>  LimeNET Mini |4G/5G, SA/NSA, NB-IoT, 3SDR 2X2 <br>4G/5G, NSA, NB-IoT (future SA) 2X2<br>4G, NB-IoT, external 2X2<br>4G, NB-IoT, internal 2x2   |
| SDR                         |ETUS N310 <br>   ETUS b210  <br> ETUS b205 mini <br>  LimeSDR mini |gNodeB 4X4 <br>UE/gNodeB 2X2<br>UE 1X1<br>1X1  |
| [UE ](#ue)                      |Huawei CPE Pro  <br>   Huawei CPE Pro 2  |NSA/SA <br> SA  |
| [Mobile Phones](#ue)       |Huawei P40 Pro  <br>  Oneplus NORD N10 <br>Redmi Note 9T <br> Realme X50<br> Samsung A90  |SA <br> SA <br> NSA <br> ~~SA~~ <br> NSA  |
| [Other Devices](#other_devices)         |SIM8200 M2   <br>Sodaq Sara M410 |SA <br> NB-IoT  |


| RADIO EQUIPMENT|                    |                   |
| -----------------------| -------------| ----------- |
| TYPE                          | MODEL       |DETAILS       |
| [gNodeB ](radio-equipment/g-node-bs) | Amarisoft Classic <br>   LimeNET Crowd Cell   <br> LimeNet <br>  LimeNET Mini <br> ETUS N310 <br> ETUS b210  <br>  |4G/5G, SA/NSA, NB-IoT, 3SDR 2X2 <br> 4G/5G, NSA, NB-IoT (future SA) 2X2<br>4G, NB-IoT, external 2X2<br>4G, NB-IoT, internal 2x2 <br> gNodeB 4X4 <br> gNodeB 2X2 |
| [User Equipment](radio-equipment/u-es)       |Huawei CPE Pro  <br>   Huawei CPE Pro 2 <br> Huawei P40 Pro  <br>  Oneplus NORD N10 <br>Redmi Note 9T <br> Realme X50<br> Samsung A90<br> ETUS b210  <br> ETUS b205 mini  | NSA/SA <br> SA <br>SA <br> SA <br> NSA <br> ~~SA~~ <br> NSA  <br>UE 2X2<br>UE 1X1   |
| [Other Devices](radio-equipment/other-devices)       |SIM8200 M2   <br>Sodaq Sara M410 <br>  LimeSDR mini |SA <br> NB-IoT <br> General Purpose SDR 1X1  |


# Available gNodeBs {#gNodeB}

GNodeBs (gNBs) are the 5G wireless base stations that transmit and receive communications between the user equipment and the mobile network.

## AMARI Callbox Classic.



 - Allows for multiple cells configuration. 
 - Supports both 5G NR NSA and SA mode.
 - 3 2x2 MIMO SDRs
 - UL/DL: 600/150 Mbps
 - LTE and NB-Iot Capable
 - Internal use | 

![Amari Call Box 1](/uploads/images-radio-equipment/amari-call-box-1.jpg "Amari Call Box Single")
![Amari Call Box 3](/uploads/images-radio-equipment/amari-call-box-3.jpg "Amari Call Box Multiple") 


## LimeNET CrowdCell
- Allows for multiple cells configuration.
- Supports 5G NR NSA mode. SA to be supported.
- 2 2x2 MIMO SDRs
- 4 antennas
- Power amplifier
- External use

![Limenet Crowd Cell](/uploads/images-radio-equipment/limenet-crowd-cell.png "Limenet Crowd Cell")
## LimeNET
- Allows for multiple cells configuration.
- Supports LTE and NB-IoT
- 2x2 MIMO SDR (PCI)
- 4 antennas
- External use

![Limenet](/uploads/images-radio-equipment/limenet.jpg "Limenet")

## LimeNET Mini
- Allows for multiple cells configuration.
- Supports LTE and NB-IoT
- 2x2 MIMO SDR (USB)
- 4 antennas
- Internal use (mainly for NB-IoT)

![Limenet Mini](/uploads/images-radio-equipment/limenet-mini.jpg "Limenet Mini")


## ETUS N310
- SDR
- 4X4 MIMO
- Up to 100MHz BW

![Etus N 310](/uploads/images-radio-equipment/etus-n-310.png "Etus N 310")
## ETUS B210
- SDR
- 2X2 MIMO
- Up to 56MHz BW

![Etus B 210](/uploads/images-radio-equipment/etus-b-210.jpg "Etus B 210")

# Available User Equipment  {#ue}
A subscriber’s mobile device, such as a cell phone, tablet, or modem. 
## Available CPEs
Some General content regarding CPEs...
- Huawei CPE Pro 
- Huawei CPE Pro2
## Huawei CPE Pro /Pro 2

- 4G
- 5G (SA/NSA)
- WiFi
- Ethernet
- Balong 5000 chipset
- Pro
    - NSA/SA
    - DL/UL: 2300/150 Mbps (theoretical)
    - DL/UL: 300/40 Mbps (tested)
- Pro 2
    - NSA
    - DL/UL: 3600/250 Mbps (theoretical)
    - DL/UL: 250/40 Mbps (tested)

![Huawei Cpes](/uploads/images-radio-equipment/huawei-cpes.png "Huawei Cpes")

## Available Mobile Phones
Some General content regarding Mobile phones...
- Huawei P40 Pro
- Oneplus NORD N10
- RealMe x50
- Xiaomi Redmi Note 9T 
- Samsung Galaxy A90 



## Huawei P40 Pro

- Android phone
- Kirin 990 5G chipset
- DL/UL: 325/38 Mbps (tested)
- SA

![Huawei P 40 Pro](/uploads/images-radio-equipment/huawei-p-40-pro.jpg "Huawei P 40 Pro")
## Oneplus NORD N10

- Android phone
- Qualcomm SM 6350 chipset
- DL/UL: 98/22 Mbps (tested)

![Oneplus Nord N 10](/uploads/images-radio-equipment/oneplus-nord-n-10.jpg "Oneplus Nord N 10")
## RealMe x50

- Android phone
- Qualcomm SM 6350 chipset

![Realme X 50](/uploads/images-radio-equipment/realme-x-50.jpg "Realme X 50")
## Xiaomi Redmi Note 9T 
- Android phone
- Mediatec 800U 5G chipset
- NSA

![Xiaomi Redmi Note 9 T](/uploads/images-radio-equipment/xiaomi-redmi-note-9-t.jpg "Xiaomi Redmi Note 9 T")
## Samsung Galaxy A90 

- Android phone
- SDM855 Snapdragon 855 chipset
- NSA
- DL/UL: 200/25 Mbps (tested)

![Samsung Galaxy A 90](/uploads/images-radio-equipment/samsung-galaxy-a-90.jpg "Samsung Galaxy A 90")


# Other Devices {#other_devices}

Some General content regarding other devices....
## SIM8200-m2
- HAT for raspberry pi
- 3G/4G/5G
- Snapdragon X55 chipset
- SA
- DL/UL: 120/40 Mbps (tested)

![Sim 800](/uploads/images-radio-equipment/sim-800.jpg "Sim 800")
## Sodaq SARA
- Arduino Based
- NB-IoT 
- Ublox chipset
- GPS
- Temperature/Humidity Sensors

![Sodaq Sara](/uploads/images-radio-equipment/sodaq-sara.jpg "Sodaq Sara")
