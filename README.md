# Wi-Fi RTT(Round-Trip-Time) Indoor Position
###### tags: `Notes`

## References
:::warning
- [Android Docs](https://developer.android.com/guide/topics/connectivity/wifi-rtt)
- [Smartphone-based Indoor Positioning Using Wi-Fi Fine Timing Measurement Protocol](https://core.ac.uk/download/pdf/233003516.pdf)
- [A Machine Learning Approach for Wi-Fi RTT Ranging](https://www.researchgate.net/publication/329887019_A_Machine_Learning_Approach_for_Wi-Fi_RTT_Ranging)
:::

## Introduction
:::success
**Wi-Fi Round Trip Time (RTT)** is a feature of the **Wi-Fi protocol** that enables **devices to measure the distance between one another and the Wi-Fi access point (AP)**. RTT technology is based on the **IEEE 802.11mc protocol**, also known as Wi-Fi RTT or **fine timing measurement (FTM)**.
:::

## How it works
:::success
Wi-Fi RTT **measures the time** it takes for a wireless device to **send a signal to an access point and receive a response**. By calculating this round-trip time, Wi-Fi RTT **can determine the distance between** the device and the access point. This can be useful for **indoor positioning systems, asset tracking, and location-based services**.

![](https://i.imgur.com/J1VfocA.png)

The distance calulated using this equation : 
\begin{equation} Range= c . {\frac {(t_{4} - t_{1})-(t_{3} - t_{2})}{2}}\end{equation}

where 
* t~1~ is **the time of departure (ToD)** measured by the RSTA, and 
* t~4~ is the **time of arrival (ToA)**, which is estimated by the RSTA
*  c = 3.108m/s is the **electromagnetic propagation speed**. 
*  The values of t~1~ and t~4~ are **reported back to the ISTA** after the completion of the FTM measurement phase. 
*  The ISTA **combines the values of t~1~ and t~4~** along with its own estimated ToA (t~2~) and measured ToD (t~3~) values, to obtain a range estimate w.r.t. the RSTA.
:::

## Implementation
:::info
Wi-Fi RTT can **provide location accuracy to within one meter**, which is much **more precise** than traditional Wi-Fi location methods. This is achieved by using **multiple access points** to **triangulate** the device's position.

Wi-Fi RTT can also be used to **improve the performance** of Wi-Fi networks. By knowing the **distance** between the device and the access point, the Wi-Fi network can **adjust the signal strength and channel allocation** to optimize the connection.
:::


## Supported Device
:::   warning
Not all devices support Wi-Fi RTT. The technology is currently limited to **newer Android devices running Android 9 or later**, and it requires support from the Wi-Fi access point as well.
List device that supported the RTT protocol is provided in [Android Docs](https://developer.android.com/guide/topics/connectivity/wifi-rtt)
:::



