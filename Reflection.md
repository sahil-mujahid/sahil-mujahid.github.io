---
layout: page
title: Reflection
css: /assets/css/custom.css
---

# Self‑Assessment and Reflection

This reflection looks at how I grew as a pipeline architect, unofficial manager, and Unity contributor during the XR industrial project, not just at what I delivered.

## What went well

What went best was turning a messy situation into a coherent pipeline and vision. With six people and lots of overlapping skills, I stepped into an architect/coordination role even though I initially wanted to be more purely technical.[file:54] I proposed the idea of using live machine alarms to trigger XR mitigation views, mapped out the PLC → Node‑RED → InfluxDB → Unity pipeline, and later translated that into a working Unity scene with a clear HUD and meaningful animations.

I am also happy with how the final XR interface turned out. The HUD, status panels, and loader animations communicate errors and normal operation in a way that makes sense to non‑experts, and this came from many iterations of sketches, whiteboard plans, and Unity tests.

## What was challenging

The hardest part was the team setup. Six people is a lot for one project, and there were times when too many of us were trying to work on the same area. I did not start the project wanting to be “the manager”, but everyone naturally came to me with questions, so I ended up coordinating tasks, clarifying priorities, and keeping the pipeline consistent. That took energy away from hands‑on building and sometimes left me feeling overworked and a bit frustrated.

It was also tiring to hold the whole system in my head: PLC variables, Node‑RED flows, JSON formats, Unity WebRequests, animations, and UI states. Making sure all of these lined up while still helping others debug their parts was a constant mental load.

## Skills I developed

Over the project I feel I grew in three main areas:

- **System design and integration:** designing and maintaining the end‑to‑end pipeline so that Node‑RED, InfluxDB, and Unity stayed compatible. 
- **XR UI and animation thinking:** planning HUD layouts, status states, and loader animations that explain functional industrial behaviour using some of my experience in Human computer interaction and UI design. 
- **People and project skills:** tolerating chaos, mediating disagreements, and keeping work moving even when I was tired and would have preferred to just code.

## What I would do differently

If I did a similar project again, I would push harder at the start to define clear roles and ownership so I could keep more time for technical work. I would also formalise data and naming conventions earlier, because a lot of integration pain came from small inconsistencies that could have been avoided.

I would try to protect my own workload better, instead of always saying yes when someone needed help. Stepping up was the right thing to do, but I would like to do it in a way that is more sustainable for me.

## What I learned from Scrum and teamwork

Scrum‑style sprints and boards were helpful for keeping everyone roughly aligned, but they do not magically fix team‑size and responsibility problems. I learned that “doing Scrum” only works if roles, hand‑offs, and expectations are clear. In this project I learned to use stand‑ups, boards, and whiteboards to keep the big picture visible, and I realised that technical leadership sometimes means quietly taking on the unglamorous coordination work so the rest of the team can succeed.

Overall, even though I was often tired and stretched, I am confident that I did my best within the constraints and that my architectural decisions, Unity work, and coordination effort were critical for getting the project to a working XR demo.
