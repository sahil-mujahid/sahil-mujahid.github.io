---
layout: page
title: Contributions
css: /assets/css/custom.css
---

### sprint 1: Planning, Setup and First Node‑RED Steps  
**Mon 27 Oct – Fri 31 Oct 2025**

This week was about shaping the project and getting the technical ground ready. I co‑planned the overall pipeline on the whiteboard, sketching how PLC data would flow through Node‑RED and InfluxDB into Unity with MRTK3 and WebRequests driving the XR side. I helped Laheeq with the initial Node‑RED environment, especially around testing OPC UA connections and understanding how we might read SIF‑401 data even while wireless access was still unstable.

![Initial pipeline planning on the whiteboard showing PLC → Node‑RED → InfluxDB → Unity with MRTK3 and WebRequest steps](initialplan.png)

While the backend team experimented with live reads, I focused on turning our notes into a clearer plan: which parts belonged to PLC/Node‑RED, which to data storage, and what Unity would eventually need from them. This early planning made it easier later to argue for features like alarm‑driven UI tiles and loader animations because we already had them in the first diagrams.


## Sprint 2 – Wireless Access and Data Path

### Establishing wireless connection to Machine 401

In this sprint my main contribution was getting reliable wireless access to Machine 401 so the rest of the team could develop Node‑RED flows without constantly fighting the network. I analysed how the WLAN_SIF400 network behaved, documented that it had no direct internet, and worked out the steps for connecting laptops to the cell while still being able to reach Node‑RED running locally.

![Whiteboard notes for establishing wireless connection to Machine 401 and accessing Node‑RED and the SMC APIs](wirelessplan.png)

Once the connection procedure was clear, I wrote it down for the team and walked others through it so they could reproduce the setup quickly. This freed Laheeq and the backend group to focus on OPC UA variables and HTTP endpoints, while I kept an eye on how this data path would later feed into InfluxDB and Unity.





