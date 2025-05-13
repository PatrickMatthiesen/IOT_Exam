# Exam questions and answers

## Q1 – Designing a Networked Sensor Device for Asset Tracking (40%)

You are tasked with designing sensor devices to track assets (vehicles and animals) in two wildlife parks:

- Knuthenborg: 1,600 acres, Denmark (lat/lon 54.811358, 11.5082552)
- Mpala Research Center: 48,000 acres, Kenya (lat/lon 0.2882139, 36.9017593)

Each device must:

- Track location (≥500 m accuracy, preferably better)
- Measure acceleration (motion state)
- Measure particulate matter concentration
- Record data every hour (preferably real-time reporting)

__Considerations:__

- Asset Diversity: Vehicles can carry larger, heavier devices with higher power needs; animals require lightweight, non-intrusive, low-power devices.
- Location Differences: Mpala is much larger and more remote, requiring long-range, low-power networking (e.g., LoRaWAN, satellite). Knuthenborg may support cellular or Wi-Fi.
- Device Design: One device cannot fit all cases. Vehicle trackers can be larger and use vehicle power; animal trackers must be small, battery-powered, and rugged.
- Exclusions: Large, heavy, or high-power devices are unsuitable for small animals. Real-time reporting may not be feasible for all animals due to power/network constraints.

__Conclusion:__  
Design at least two device types:

- Vehicle tracker: Larger, powered, supports frequent or real-time reporting, more sensors.
- Animal tracker: Lightweight, battery-efficient, records hourly, transmits when in range or via low-power networks.

Networking/System Choices:  

- Use GPS for location.
- LoRaWAN or satellite for remote, large areas (Mpala); cellular/Wi-Fi for smaller, accessible areas (Knuthenborg).
- Optimize reporting frequency and data transmission for power and network availability.

notes:
Data sent - Batery voltage? - GPS location - acceleration - particulate matter concentration     - timestamp - device id

Mpala considerations:
It seems that the area has some research stations, so we might be able to use some of the existing infrastructure, so we dont have to consider power in these areas.

knuthenborg considerations:
the area is well covered by cellular networks. Some cellular technologies might not have the best coverage due to the trees, but we can assume that the area is well covered by 4G and 5G networks.


