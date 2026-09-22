# Case 02 - Slow Wi-Fi on One Device

## Problem
  A laptop and a smartphone were connected to the same home network, 
  but the smartphone consistently achieved lower Internet throughput than the laptop.

  The issue was observed on the 2.4 GHz Wi-Fi network.

## Initial Observation
  Initial Speedtest results:

  |   Device   |  Download  |   Upload   | Ping  |
  | ---------- | ---------: | ---------: | ----: |
  | Laptop     | 93.44 Mbps | 85.39 Mbps | 20 ms |
  | Smartphone | 28.63 Mbps | -          | 16 ms |

<p align="center">
  <img src="troubleshooting/img/Screenshot_2026-09-22_021902.png" width="58%">
  <img src="troubleshooting/img/Screenshot_20260922-022026_init.png" width="39%">
</p>

The laptop was able to achieve around 90 Mbps, while the smartphone was significantly slower.

## Wi-Fi Information

### Laptop
  - Wi-Fi adapter: Intel(R) Wi-Fi 6 AX200 160MHz
  - Wi-Fi protocol: Wi-Fi 4 (802.11n)
  - Frequency: 2.4 GHz
  - Channel: 7
  - Signal: 87%
  - RX/TX link speed: 300/144 Mbps

### Smartphone
  - Frequency: 2.4 GHz
  - Wi-Fi protocol: Wi-Fi 4 (802.11n)
  - Link speed: approximately 65–72 Mbps
  - Signal: very good when tested close to the router

##  Troubleshooting Tests

### Test 1 - Change Channel Bandwidth
  Router configuration:
  - Channel: 7
  - Bandwidth: 40 MHz

  Result:
  - Download: 28.63 Mbps
  - Ping: 16 ms

  **Bandwidth was then changed to 20 MHz.**
  
  Result:
  - Download: 40 Mbps
  - Ping: 18 ms

  This indicated that Wi-Fi throughput changed when the channel bandwidth was modified.

### Test 2 - Change Channel
  Configuration:
  - Bandwidth: 20 MHz
  - Channel: 1

  Result:
  - Download: 22.31 Mbps
  - Ping: 25 ms

  The result was lower than the previous 20 MHz / Channel 7 test.

### Test 3 - Return to 40 MH
  Configuration:
  - Channel: 7
  - Configured bandwidth: 20/40 MHz
  - Current bandwidth: 40 MHz

  Result:
  - Smartphone download: 31.11 Mbps
  - Ping: 21 ms

  Laptop tested under the same router configuration:

  - Download: 94.47 Mbps
  - Upload: 91.62 Mbps
  - Ping: 22 ms

  This showed that the laptop continued to achieve around 90+ Mbps while the smartphone remained significantly slower.

### Test 4 - Test Smartphone Close to Router
  The smartphone was placed very close to the router to reduce the possibility of distance or weak signal affecting performance.

  Result:
  - Download: 31.31 Mbps
  - Ping: 18 ms
  - Link speed remained approximately 65–72 Mbps

  Moving closer to the router did not significantly improve throughput.

### Test 5 - Test With Another Router
<img src="troubleshooting/img/Screenshot_20260922-215021.png" align="right" width="350">

  The original router was temporarily replaced with another router.

  Configuration of the replacement router:
  - 2.4 GHz
  - 802.11b/g/n
  - Channel: Auto
  - Bandwidth: Auto

  Only the smartphone was connected during the test.

  Result:
  - Download: 47.14 Mbps
  - Ping: 18 ms

  The test was short because the replacement router is not mine.


<br clear="right">

## Findings
  The investigation showed several observations:
  1. The laptop consistently achieved around 90+ Mbps on the same Internet connection.
  2. The smartphone negotiated a much lower Wi-Fi link speed, approximately 65–72 Mbps.
  3. Moving the smartphone closer to the router did not significantly change its link speed or throughput.
  4. Changing the router's bandwidth affected the smartphone's throughput.
  5. A different router temporarily produced a higher smartphone throughput of approximately 47 Mbps.

## Possible Cause
  The available evidence suggests that the issue may be related to the Wi-Fi link between the smartphone and the original router.
 
  Possible factors include:
  - Wi-Fi rate negotiation
  - Compatibility between the smartphone and router
  - 2.4 GHz channel/bandwidth conditions
  - Router-specific Wi-Fi configuration

  The **exact root cause** was not conclusively identified.

## Limitations
  The tests were performed with a limited number of measurements.

  The replacement-router test was also brief and was performed under different network conditions, 
  with only the smartphone connected.

  Therefore, the results are not sufficient to conclusively identify the root cause.

  Further testing with another smartphone or another client device would help isolate 
  whether the limitation is specific to that smartphone or related to the original router.

## Conclusion
  The investigation confirmed that the smartphone experienced significantly lower Wi-Fi throughput 
  than the laptop on the same network.

  The smartphone also negotiated a lower Wi-Fi link speed than the laptop, and changing Wi-Fi configuration 
  and router hardware affected its observed throughput.

  However, the exact root cause could not be conclusively determined from the available tests.

 ---
 
  > Further testing with other smartphones will be conducted in the future. 
