---
layout: page
title: Benefits & Ethics
css: /assets/css/custom.css
---

# Benefits, Limitations, System Requirements & Ethics

## Benefits

For operators, the XR HUD turns numbers and alarm codes into something they can see and understand quickly: coloured status panels, clear text, and animated loaders that show what is happening. For the company, it creates a space to rehearse error situations without stopping the real machine. For future developers, the pipeline and HUD layout give a starting point for other XR monitoring ideas.

## Limitations

The system only works as well as the data it receives. If the PLC, network, or backend flows fail, the XR view may be out of date or simply wrong. The current design is tuned to one cell and one headset; using it in other factories would need more design and testing. XR hardware can also be uncomfortable or distracting for some users, so it is not a universal solution.

## System requirements

The solution depends on:

- An industrial controller exposing process values and alarms  
- A machine or server running the data pipeline and API that Unity calls  
- A Unity XR application (with MRTK3 or similar) running on a headset with network access  

On top of that, the whole chain needs a consistent data format so that HUD tiles and animations always “speak the same language” as the backend.

## Ethics and stakeholders

**Operators**  
Need tools that help, not tools that blame. The HUD should support quick decisions without flooding them with colours, numbers, or warnings.

**Maintenance staff**  
Should be able to see how an error was detected and why a certain message appears, instead of trusting a black box.

**Management**  
Can benefit from better visibility but must resist turning technical monitoring into personal surveillance of workers.

**Developers (including me)**  
Have a responsibility to be honest about what the system can and cannot do, document assumptions, and design in a way that leaves room for human judgment.

The main ethical lesson for me was that a nice‑looking XR interface is not enough; it has to be transparent, respectful of the people using it, and clear about the limits of both the data and the technology.
