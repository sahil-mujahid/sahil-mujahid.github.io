---
layout: page
title: Contributions

---

### sprint 1: Planning, Setup and First Node‑RED Steps  

This week was about shaping the project and getting the technical ground ready. I co‑planned the overall pipeline on the whiteboard, sketching how PLC data would flow through Node‑RED and InfluxDB into Unity with MRTK3 and WebRequests driving the XR side. I helped Laheeq with the initial Node‑RED environment, especially around testing OPC UA connections and understanding how we might read SIF‑401 data even while wireless access was still unstable.

![Initial pipeline planning on the whiteboard showing PLC → Node‑RED → InfluxDB → Unity with MRTK3 and WebRequest steps](initialplan.png)

While the backend team experimented with live reads, I focused on turning our notes into a clearer plan: which parts belonged to PLC/Node‑RED, which to data storage, and what Unity would eventually need from them. This early planning made it easier later to argue for features like alarm‑driven UI tiles and loader animations because we already had them in the first diagrams.


## Sprint 2 – Wireless Access and Data Path

### Establishing wireless connection to Machine 401

In this sprint my main contribution was getting reliable wireless access to Machine 401 so the rest of the team could develop Node‑RED flows without constantly fighting the network. I analysed how the WLAN_SIF400 network behaved, documented that it had no direct internet, and worked out the steps for connecting laptops to the cell while still being able to reach Node‑RED running locally.

![Whiteboard notes for establishing wireless connection to Machine 401 and accessing Node‑RED and the SMC APIs](wireless.png)

Once the connection procedure was clear, I wrote it down for the team and walked others through it so they could reproduce the setup quickly. This freed Laheeq and the backend group to focus on OPC UA variables and HTTP endpoints, while I kept an eye on how this data path would later feed into InfluxDB and Unity.

## Sprint 3 – Unity Data Link, UI and Animation Experiments

In Sprint 3 my work shifted fully to the Unity side. The first priority was proving that our pipeline actually reached XR, so I helped establish the Unity–Node‑RED link and confirm that live values could be shown on HoloLens before going deeper into animations. The screenshot below documents this milestone, where a simple Unity scene successfully displayed data coming from our backend.

![First successful Unity–Node‑RED data link shown on HoloLens](unitylink.png)

Once the data path was working, I focused on the Unity tasks from the Taiga board: designing the UI, creating placeholder animations for alarms, loading 3D objects, and preparing Unity to display mitigation steps. I set up the main scene with MRTK3, organised the hierarchy, and imported simple loader structures that stood in for the real SIF‑401 equipment. Using these placeholders I began blocking out how alarms would appear in XR and where mitigation information would sit around the user.

I also experimented with different motion ideas for loaders and error reactions. The videos below capture early tests of pallet and cylinder movement, timing experiments, and rough alarm responses. These clips were important for deciding which motions felt readable and believable enough to refine in later sprints.

### Media from this sprint

<video src="/animationideastest.mp4" controls width="640">
  Your browser does not support the video tag.
</video>

<video src="/motionanimator.mp4" controls width="640">
  Your browser does not support the video tag.
</video>

<video src="/placeholders.mp4" controls width="640">
  Your browser does not support the video tag.
</video>

## Sprint 4 – Data‑Driven UI and Refined Pallet Animations

In Sprint 4 the focus shifted to making the Unity scene feel closer to the real system. On the Taiga board this matched stories like “Connect data from Unity with User Interface”, while more API and mapping work happened on the Node‑RED side. My job was to take the values arriving from the backend and show them clearly in XR, while also polishing the pallet animations started in the previous sprint.

I worked on the main HUD layout in Unity, arranging tiles for key signals such as airflow, power, voltage and error status around the operator’s viewpoint. The screenshot below (`unityhud.png`) shows this data‑driven interface, where colours and labels were chosen so operators could quickly distinguish normal operation from problems.

![Data‑driven XR HUD showing live values and error status panel](unityhud.png)

Alongside the UI, I refined the pallet and loader animations so they matched the physical timing we expected from Machine 401. I adjusted easing, start/end positions and clip lengths, and tested how the motions looked when viewed through HoloLens. The video `finalanim.mp4` captures these more polished animations, which replaced the rough placeholder motion from Sprint 3 and prepared us for full end‑to‑end testing in the final sprint.

<video src="/finalanim.mp4" controls width="640">
  Your browser does not support the video tag.
</video>

## Sprint 5 – Final HUD, polish, and hand‑over

Sprint 5 was about bringing everything together and making the XR interface feel like a finished product. I took the lead on finalising the HUD design: deciding the layout, colours, and wording for normal status and error states so operators could quickly understand what the cell was doing.

![Final HUD layout overview used in Sprint 5 planning](sprint5finalhud.jpeg)

I refined the “System Status” and “Error Status” panels so they clearly switched between green normal state and red fault state based on live data.

![Final XR HUD in normal green system status](finalhudgreen.jpeg)

![Final XR HUD in error red system status](finalhudred.jpeg)

At the same time I helped with final tests of the end‑to‑end pipeline and contributed material for the written report and presentation, explaining how the HUD and animations express the underlying error‑handling logic.




