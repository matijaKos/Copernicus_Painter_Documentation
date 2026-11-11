# 3D Path

A **3D Path** mask is made of paths you draw on the model. They stay editable: move a point, add one, change the width, and the mask follows. A path is a **Line** (a stroke) or a **Ribbon** (text or an image laid along it): stitching, piping, seams, labels, lettering along an edge, a row of stars.

Add one with **Right-click a layer > Add Mask > 3D Path** (or the **Mask** button above the stack). It bakes **Position** and **World Normal** first if the project doesn't have them. Select the mask: the viewer goes into the path tool and Properties shows its paths.

## Drawing

| In the viewer | |
|---|---|
| **Click** on the model | a new path, then a point at each click |
| **Drag a point** | move it |
| **Click a segment** | insert a point there |
| **Shift + drag** (or **Draw: Freehand**) | draw freehand; it becomes a path of a few points (**Smoothing**) |
| **Del** | delete the selected point |
| **V** | corner / smooth point |
| **C** | close / open the path |
| **R** | reverse its direction |
| **Enter** / **Esc** | finish the path |

Paths follow the surface in the 3D view and the 2D view. One mask holds several paths: **New Path** starts another, the list shows them all (the check hides one, double-click renames it), **Delete** removes the selected one.

## A path's look

Select a path in the list. **Look** is **Line** or **Ribbon**.

- **Width**, **Opacity**, **Closed**, **Reverse** for both.
- A **Line** has **Softness**: how soft its edges are.
- A **Ribbon** has:
    - **Content**: **Text** (type it, pick a font) or **Image** (pick one of your alphas, by section and with search, or **Other image...** for any file).
    - **Tiling**: **Stretch** the text or image along the whole path, or **Repeat** it.
    - **Offset** slides it along the path; **Flip** mirrors it across the path.
    - **Feather** softens the ribbon's edges and ends; **Blur** softens the text or image itself.

Each path has its own look and content: one mask can hold a line, a ribbon of text and a ribbon of stars.

The mask is made at the project's resolution, so a path stays sharp when you raise it.

## Undo

Every edit (a point added or moved, a width let go, a path deleted) is one undo step. Copying, moving or deleting the mask works as for any mask ([Moving and copying masks and filters](layers.md#moving-and-copying-masks-and-filters)).
