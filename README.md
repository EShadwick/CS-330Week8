# CS-330Week8
Interactive 3D scene in C++/OpenGL with Phong lighting, applied textures, and perspective/orthographic camera controls. Computational graphics portfolio piece.
# CS 330: Computational Graphics and Visualization

## Project Overview

This repository contains my final project for CS 330, a fully realized 3D scene
built in C++ with OpenGL using the CS330Content framework. The scene recreates a
small still life: an oil lamp on a wooden surface, with a brass body, a frosted
glass reservoir, and a wood-textured base plane. It is lit by a two-source Phong
lighting rig (ambient, diffuse, and specular) and is fully navigable through
keyboard and mouse camera controls, including a toggle between perspective and
orthographic projection.

**Artifacts in this repository**

- `3D_Scene.zip` — the complete Visual Studio project, source, textures, and
  executable for the 3D scene.
- `Design_Decisions.docx` — the document explaining the objects, textures,
  lighting, and camera design choices behind the scene.

---

## Reflection

### How do I approach designing software?

This project pushed me to design around how light and surfaces actually behave,
not just where objects sit in space. The new design skill I built was reasoning
about a scene as a system of materials and light rather than a collection of
shapes. I followed an iterative, milestone-driven process: I started by blocking
out the objects from primitives, then layered on textures, then lighting, then
camera control, treating each layer as a design decision I had to justify rather
than a feature to bolt on. A turning point was learning to read the actual shader
implementation instead of trusting the variable names, since the framework treats
its lighting uniforms differently than the textbook diagram implies. That habit,
verifying how a system really behaves before designing on top of it, is something
I will carry into any future software work, where assumptions about a dependency
are exactly where designs tend to break.

### How do I approach developing programs?

My main new development strategy was building the scene in deliberate,
verifiable increments and confirming each one worked before moving on. Iteration
was the core of the whole project. Milestone Two came back at 79.5, and rather
than patch over it, I went back and rebuilt the lighting and material handling
from a more accurate understanding of the pipeline, which is what let the frosted
glass finally read as glass instead of plastic. I also learned to separate a
rendering problem from a logic problem. When the scene first looked like a dome
floor with floating shapes, I traced it to the camera setup in the view manager
rather than wasting time tuning lights that were never the cause. Over the
milestones my approach evolved from placing objects until something looked right
toward isolating one variable at a time, reading the evidence on screen, and
confirming a clean build before interpreting results.

### How can computer science help me in reaching my goals?

The mathematics under this project, the matrix transforms, vector operations, and
coordinate spaces, is the same foundation that machine learning and 3D medical
imaging rest on, which connects directly to my educational path toward applied
healthcare AI. Learning to think in terms of how spatial data is transformed and
rendered gives me a concrete handle on the volumetric and spatial data that
clinical work is full of, from imaging reconstruction to device placement
visualization. Professionally, the larger skill is the discipline this project
forced: reading the real implementation, verifying the build state, and changing
one thing at a time. That is the exact way I want to approach debugging models and
data pipelines, where a wrong assumption is costly and the evidence is the only
reliable guide. I expect to extend these skills toward interactive data
visualization and eventually toward representing clinical and operational data in
ways that help people reason about it.

---

## AI Acknowledgment

Generative AI (Anthropic Claude) was used to assist with development, debugging,
and drafting portions of the written reflection for this project. All design
choices, code, and final work were reviewed, tested, and verified by the author.

**Reference**

Anthropic. (2026). *Claude (Opus 4.8)* [Large language model]. https://claude.ai
