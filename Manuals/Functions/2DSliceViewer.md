---
layout: default
title: 2DSliceViewer
category: FunctionDocs 
function: 
  chapter: Seg3DViewer
  subchapter: ViewerPanels 
---

# {{ page.title }} 

## Category

**{{ page.chapter }}{{ page.subchapter }}**

## Description

Tables <a href="#tab2dmouse">3.1TODO</a> & [3.2TODO](#2dkey) show the mouse and keyboard actions which can be used to control the visualization and manipulation of image and segmentation data. Though these functions are general, there are tools which used these functions for specify purposes or may otherwise block a couple of these functions, the most prominent example is the scroll wheel in the paint brush tool is used to change brush size. In this case, you can still scroll through slices by holding Shift. In all cases, an alternative is given in the software. Also presented in this section is a list and description of the icons presented in the 2D slice viewer ([Table 3.3](#2dicons)).

| **Mouse Command** | **Function**<a name="tab2dmouse"></a>                              |
|:----|:----|
| left button drag               | Modify brightness and contrast. Vertical is contrast, horizontal is brightness.                          |
| scroll up/down                 | Move up/down a slice Note: using Shift maybe needed while using some tools (like paint brush) |
| CMD/CTRL+right button          | Move slices in other planes to intersect at cursor. Viewers must have the picking icon enabled ([Table 3.3](#2dicons)).      |
| Shift+left button drag         | Pan view         |
| Shift+right button drag        | Zoom view in/out       |

Table 3.1: List of mouse functions in the 2D viewers.

| **Keyboard Action** | **Function** <a name="2dkey"></a>         |
|:----|:----|
| up arrow,&gt;                    | move up one slice              |
| down arrow,&lt;                  | move down one slice                  |
| Shift+up arrow,Shift+&gt;        | Jump up n slices (set n in preferences)                     |
| Shift+down arrow,Shift+&lt;      | Jump down n slices (set n in preferences)                   |
| left/right arrow                 | Change active layer to previous/next layer                  |
| SPACE                            | Toggle layer visibility on/off (active layer)               |
| G                                | Toggle grid visibility                                      |
| P                                | Toggle picking state                                        |
| T                                | Toggle overlay visibility                                   |
| L                                | Toggle lock viewer (to other locked views of the same type) |

Table 3.2: List of keyboard actions in the 2D viewers.TODO

| **Icon** | **Function** <a name="2dicons"></a>|
|:----|:----|
|![alt text](Seg3DBasicFunctionality_figures/AutoViewOff.png)    | Autoview Icon: This icon forces the panel to fit the objects in viewer with maximum size.|
|![alt text](Seg3DBasicFunctionality_figures/LockOff.png)        | Lock View Icon: This icon toggles the viewer lock on the panel (shortcut: L). Any changes to any locked viewers will change all the views. Viewers must be the same type and each must be locked to use this funtion.|
|![alt text](Seg3DBasicFunctionality_figures/VisibleOff.png)     | Visibility Icon: This icon toggles the visibility of the plane in the 3D volume viewer.|
|![alt text](Seg3DBasicFunctionality_figures/PickingOff.png)     | Picking Icon: This icon toggles the ability of other planes to pick the slice to view in the panel. Only one viewer can have this option enabled. If there is only one type of plane, this cannot be disabled.|
|![alt text](Seg3DBasicFunctionality_figures/GridOff.png)        | Grid Icon: This icon toggles the visibility of the grid in the viewer.           |
|![alt text](Seg3DBasicFunctionality_figures/FlipHorizOff.png)   | Flip Horizontal Icon: This icon will horizontally flip the visualization of the slices in the viewer.|
|![alt text](Seg3DBasicFunctionality_figures/FlipVertOff.png)    | Flip Vertical Icon: This icon will vertically flip the visualization of the slices in the viewer.|
|![alt text](Seg3DBasicFunctionality_figures/OverlayOff.png)     | Overlay Icon: This icon will toggle the visibility of the overlay on the viewer. This will allow unobstructed viewing of the slices.|
|![alt text](Seg3DBasicFunctionality_figures/PickingLinesOff.png)| Picking Lines Icon: This icon toggles the visibility of the picking lines (shows other slices) in the viewing panel.|

Table 3.3: List of icons and actions in the 2D viewers.

%![alt text]({{ site.github.url }}/images/{{ page.title }}GUI.png)TODO

{% capture url %}{% include url.md%}{% endcapture %}
{{ url }}

