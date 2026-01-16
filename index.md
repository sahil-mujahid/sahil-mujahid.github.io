# XR Individual Project Portfolio (IPP2)

**Author:** Your Name  
**Project:** Project Title  

---

## 1. Individual Contribution Tracking

This section documents my personal work on the project, focusing on animation, XR UI design, and light management tasks.

| Week / Sprint | Tasks | Tools / Artefacts |
|--------------|-------|-------------------|
| Week 1 | Set up Unity XR project. Imported Solid Edge models (pallet, canister, cylinder). Created first pallet drop animation rig. | Unity, XR Interaction Toolkit. Screenshots of pallet in scene and first animation clip. |
| Week 2 | Built **PalletDrop_Rig** with arrow indicating motion. Added rigs for square canister loader and cylinder drop. Tweaked timing and easing of animations. | Unity Animator / Animation windows. GIF of loading sequence. Small C# snippet triggering animations from API values. |
| Week 3 | Designed alarm and status UI panels in world space. Implemented colour‑coding (green/amber/red) and text changes at runtime. Helped decide layout and interaction flow for XR operator view. | Unity UI canvases, TextMeshPro. Screenshots of final HUD and alarm panel. Script for updating text and colours via API data. |
| Week 4 | Packaged rigs as reusable prefabs and Unity packages. Coordinated short stand‑ups and task breakdown (informal management role). Assisted teammates integrating their logic scripts with my animations. | Prefab + `.unitypackage` exports. Notes and chat logs about integration issues and fixes. |
this is a rough estimate for what actually happened

---

## 2. Self‑Assessment / Reflection

### What went well
I took ownership of the animation pipeline and XR interface visuals. The pallet, canister, and cylinder rigs clearly show the flow of material through the cell, and the UI layout is readable and operator‑friendly in XR.

### What was challenging
The hardest part was connecting imported CAD models and timing‑sensitive animations with live data from the API layer. Small mistakes in pivots, scales, or clip lengths often broke the realism. Balancing my informal management role with hands‑on development time was also challenging.

### Skills I developed
- Unity animation: rig organisation, clips, Animator controllers  
- World‑space UI design for XR (layouts, colours, readability)  
- Team communication and documenting small, incremental deliverables  

### What I would do differently
Next time I would prototype interactions earlier and agree on naming conventions and folder structures from the start. This would reduce refactoring and make it easier for teammates to plug into my rigs and UI components.

### What I learned from Scrum / teamwork
Short check‑ins kept everyone aligned and exposed blockers quickly. I learned to make my work visible with small, finished pieces (new clip, new panel, updated prefab) so others could build on them without waiting for a big final merge.

---

## 3. Peer Review & Group Feedback

### Feedback received
- **Comment A:** Make the portfolio structure clearer and show the timeline of contributions more explicitly.  
  *From:* teammate \[Initials\]  
- **Comment B:** Add more screenshots of the Unity scene and Animator so non‑technical readers can understand the work.  
  *From:* teammate \[Initials\]  
- **Comment C:** Explain the connection between API data and visual error states in the XR UI.  
  *From:* teammate \[Initials\]

### My response to feedback
- For Comment A I added the chronological log table at the top and labelled each week/sprint.  
- For Comment B I embedded multiple screenshots/GIFs next to the log entries and reflection.  
- For Comment C I expanded the ethics/system‑requirements section with a description of how alarms and error states flow from the API into the UI.

---

## 4. Benefits, Limitations, System Requirements & Ethics

### Potential benefits
- Gives operators an intuitive 3D view of the cell, showing where each pallet or canister is.  
- Colour‑coded alarms and animated rigs help distinguish normal operation from faults at a glance.  
- Reusable Unity prefabs mean similar cells could be visualised quickly in future projects.

### Limitations
- Requires XR‑capable hardware and a reasonably powerful PC.  
- If API data is delayed or incorrect, the visualisation can mislead users.  
- Some users may experience fatigue or motion sickness when using XR.

### System requirements (example)
- Unity (version you used), URP, XR Interaction Toolkit  
- Windows PC with XR‑ready GPU and headset (e.g. headset model)  
- Network access to backend API / OPC UA server providing equipment data  

### Ethical considerations (stakeholder view)

**Operators**  
- *Benefits:* clearer alarms, easier understanding of cell status.  
- *Risks:* over‑reliance on visuals, XR discomfort.  
- *Design response:* simple language, explicit alarm states, option to exit XR quickly.

**Maintenance / Engineers**  
- *Benefits:* better visualisation of faults and sequences.  
- *Risks:* misinterpretation if data is incomplete.  
- *Design response:* show connection status and error states transparently instead of hiding them.

**Management**  
- *Benefits:* improved training and monitoring of processes.  
- *Risks:* temptation to track individuals rather than systems.  
- *Design response:* focus metrics on process performance, not personal surveillance.

**Company / Society**  
- *Benefits:* potential for safer, more efficient production.  
- *Risks:* ignoring accessibility or privacy concerns.  
- *Design response:* consider ergonomics, data‑handling policies, and inclusive design for different users.

Overall, the goal is to use XR to make industrial status information more transparent while being honest about data quality, hardware limits, and user comfort.
