---
layout: page
title: Home
css: /assets/css/custom.css
---


# XR Individual Project Portfolio (IPP2)

**Author:** Sahil Mujahid  
**Project:** XR‑driven industrial error mitigation system  

I was the project designer, pipeline architect, and later Unity animation/UI lead. I proposed the idea of using live machine alarms to trigger mitigation steps in XR, designed the end‑to‑end pipeline (OPC UA/SMC APIs → Node‑RED → InfluxDB → Unity), coordinated work across our six‑person team, and contributed hands‑on to Unity WebRequest integration, alarm‑driven UI, and loading‑rig animations.

---

## 1. Individual Contribution Tracking

This section documents my work as pipeline architect, integration lead, and Unity contributor.

### Personal sprint log

**Sprint 1 – concept, planning, setup**  
I led the discussion that shaped the core concept: when the machine raises an alarm, the operator should automatically see mitigation steps visualised in XR. I drew the first architecture diagram showing PLC/OPC UA and SMC APIs feeding Node‑RED, InfluxDB, and finally Unity on HoloLens. Together with Laheeq I helped set up Node‑RED, then shifted into a management and planning role, organising tasks while starting to explore Unity environments and sketching how C# scripts and WebRequests would drive the UI and animations.

**Sprint 2 – variables, alarms, data layer**  
I worked with the backend team to explore SIF‑401 variables and alarm types, guiding which tags were most useful for detection and which should be exposed to Unity. I helped document variable mappings, advised on function‑node logic so that Node‑RED produced clean JSON, and supported the initial InfluxDB setup for storing time‑series data.

**Sprint 3 – pipeline alignment, early UI and animations**  
I led a review of the full project pipeline, checking that each part from PLC to Unity still supported the error‑mitigation idea. I bridged technical questions between Node‑RED and Unity, helped extend Node‑RED logic, and started adding placeholder Unity animations and a rough XR UI to visualise key values and alarms.

**Sprint 4 – Unity WebRequest and animation planning**  
I collaborated on Unity WebRequest integration, defining endpoints, testing sample calls, and mapping JSON output to Unity alarm logic. I planned the animation workflow for the loaders and alarm events, worked on loading‑rig animations in Unity, and discussed how new error scenarios could reuse the same approach.

**Sprint 5 – UI refactor, testing, documentation**  
I refactored the XR UI for consistency, cleaned up naming and hierarchy in the Unity project, and supported full end‑to‑end testing from Node‑RED through to XR visualisation. I also documented how alarms, variables, and animations are connected so future teams can extend the system more easily.

---

## 2. Self‑Assessment / Reflection

### What went well
Owning the overall pipeline design gave the team a clear technical direction and made hand‑offs between Node‑RED and Unity smoother. When Unity work ramped up, I could quickly shift from coordinator to contributor because I already understood how data and alarms were supposed to flow.

### What was challenging
Balancing a management role with hands‑on technical work was difficult, especially with six members and many dependencies. It was also challenging to keep track of all PLC variables and ensure that the Unity side always matched the latest alarm logic coming from Node‑RED.

### Skills I developed
- System and pipeline design across multiple platforms (PLC, Node‑RED, InfluxDB, Unity)  
- Cross‑team communication and resolving integration issues between backend flows and XR front‑end behaviour  
- Unity skills around WebRequests, JSON handling, UI layout, and animation planning for industrial scenarios  

### What I would do differently
Next time I would formalise ownership of some technical tasks earlier so I could spend more time building and less time context‑switching. I would also introduce stricter naming and documentation standards at the start to reduce refactoring later.

### What I learned from Scrum / teamwork
Short sprints and regular check‑ins made problems visible early and helped align Node‑RED and Unity work. I realised that a “jack‑of‑all‑trades” role can be valuable if it is clearly defined as architect and integration lead, not just informal management.

---

## 3. Peer Review & Group Feedback

*(To be completed when feedback is available. Placeholder text describing expected themes.)*  

### Feedback received
- Comment A: Ask for feedback on how clearly the pipeline and responsibilities are explained in this portfolio.  
- Comment B: Ask teammates whether the Unity screenshots and diagrams make the architecture understandable to non‑developers.  
- Comment C: Ask whether the description of alarm‑to‑animation mapping reflects how the team actually implemented it.  

### My response to feedback
Once feedback is collected, this section will summarise what was said and what changes were made. For example, if structure or clarity is mentioned, additional diagrams, captions, or reworded sections will be added to highlight my contributions more explicitly.

---

## 4. Benefits, Limitations, System Requirements & Ethics

### Potential benefits
- Gives operators an intuitive 3D view of the cell, showing where alarms occur and what needs attention.  
- Alarm‑driven animations and colour‑coded UI help distinguish normal operation from faults at a glance.  
- A reusable pipeline means similar cells can be connected with less setup in future projects.  

### Limitations
- Requires XR‑capable hardware and a reasonably powerful PC, which may limit deployment locations.  
- If backend data is delayed, missing, or wrong, the XR view can give a false sense of accuracy.  
- Some users may experience discomfort or fatigue when using XR for long periods.  

### System requirements (example)
- Unity (project version), URP, XR Interaction Toolkit, and HoloLens or a similar XR headset  
- Windows PC with XR‑ready GPU and network access to OPC UA/SMC APIs via Node‑RED and InfluxDB  

### Ethical considerations (stakeholder view)

**Operators**  
- *Benefits:* Clearer alarms and guided mitigation steps lower stress and can improve safety.  
- *Risks:* Over‑reliance on visuals or discomfort from XR use.  
- *Design response:* Use simple language, show connection status transparently, and allow quick exit from XR.

**Maintenance / Engineers**  
- *Benefits:* Better visualisation of fault locations and sequences across the pipeline.  
- *Risks:* Misinterpretation if alarms or variables are mapped incorrectly.  
- *Design response:* Make data sources and alarm mappings visible and well documented rather than hidden behind the UI.

**Management**  
- *Benefits:* Improved training possibilities and clearer understanding of system behaviour.  
- *Risks:* Temptation to use the system for monitoring individuals rather than processes.  
- *Design response:* Focus metrics on system states and process performance, not personal tracking.

**Company / Society**  
- *Benefits:* Potentially safer, more efficient industrial environments and transferable XR practices.  
- *Risks:* Neglecting accessibility, data privacy, or long‑term ergonomics.  
- *Design response:* Consider inclusive design, robust data‑handling policies, and evaluation of XR workloads over time.
