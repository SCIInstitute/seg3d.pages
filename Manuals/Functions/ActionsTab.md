---
layout: default
title: ActionsTab
category: FunctionDocs 
function: 
  chapter: Seg3DWindows
  subchapter: ControllerWindow
---

# {{ page.title }} 

## Category

**{{ page.function.subchapter }}**

## Description

The Actions tab displays all of the actions that have been taken during the Seg3D session. Console entries can also be made with this feature.

<figure>
  <img src="../Seg3DBasicFunctionality_figures/Controller_OnStartup.png" id="OnStartup">
  <figcaption>Figure 4.9 Controller Window on inital open.</figcaption>
</figure>

A series of actions area provided in a drop-down menu at the bottom of the window (<a href="#ControllerActionList">Figure 4.10</a>). Once selected, the action will be placed into a command line to the right of the drop-down menu.

<figure>
  <img src="../Seg3DBasicFunctionality_figures/Controller_ActionList.png" id="ControllerActionList">
  <figcaption>Figure 4.10 Controller Window action list.</figcaption>
</figure>

The user can then define the parameters for the action, or simply press enter to see what parameters are required to make the action valid. If additional parameters are needed to run the action, they will be displayed in a message in the box below the command line (<a href="#UsabilityMsg">Figure 4.11</a>).

<figure>
  <img src="../Seg3DBasicFunctionality_figures/Controller_UsabilityMsg.png" id="UsabilityMsg">
  <figcaption>Figure 4.11 Action usability message.</figcaption>
</figure>

{% capture url %}{% include functionurl.md%}{% endcapture %}
{{ url }}

