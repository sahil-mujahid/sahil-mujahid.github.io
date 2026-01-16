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
