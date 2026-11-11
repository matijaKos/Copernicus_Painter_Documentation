# 3D Path

A **3D Path** mask is made of paths you draw on the model. They stay editable: move a point, add one, change the width, and the mask follows. A path is a **Line** (a stroke, solid or dashed), a **Ribbon** (text or an image laid along it, or stamped along it) or a **Fill** (the inside of a closed path): stitching, piping, seams, labels, lettering along an edge, a row of stars, a painted patch.

Add one with **Right-click a layer > Add Mask > 3D Path** (or the **Mask** button above the stack). It bakes **Position** and **World Normal** first if the project doesn't have them. Select the mask: the viewer goes into the path tool and Properties shows its paths.

## Stitches

**Add Mask > 3D Path: Stitches** makes a ready **Stitches** layer above the layer: a thread colour, **Height** (the stitches are raised) and a **Height to Normal** filter, so they show in the normal map too. Its 3D Path mask is selected: every path you draw on it is a row of stitches (the *Stitches* alphas: slanted, straight, cross). Change the thread's colour and height on the layer, the stitch image, size and spacing (**Gap**) on the path.

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

Select a path in the list. **Look** is **Line**, **Ribbon** or **Fill**.

- **Width**, **Opacity**, **Closed**, **Reverse** for all of them.
- **Point Width**: select a point (click it in the viewer) to make the path wider or thinner there; it blends smoothly to the next points.
- A **Line** has **Softness** (how soft its edges are), and **Dash** / **Gap** for a dashed line: dashes *Dash* long, *Gap* apart (Dash 0 is a solid line). **Offset** slides the dashes along.
- A **Ribbon** has:
    - **Content**: **Text** (type it, pick a font) or **Image** (pick one of your alphas, by section and with search, or **Other image...** for any file).
    - **Tiling**: **Stretch** the text or image along the whole path, or **Repeat** it.
    - **Offset** slides it along the path; **Flip** mirrors it across the path.
    - **Feather** softens the ribbon's edges and ends; **Blur** softens the text or image itself.
    - With **Repeat**, **Gap** spaces the repeats apart: separate **stamps** along the path (stars, stitches, footprints).
- **Fill** fills the inside of a closed path (choosing it closes the path). **Width** with **Softness** sets how soft its edge is. It suits a patch on a fairly even part of the model: on a strongly curved part, draw the loop with more points.

Each path has its own look and content: one mask can hold a line, a ribbon of text and a ribbon of stars.

The mask is made at the project's resolution, so a path stays sharp when you raise it.

## Undo

Every edit (a point added or moved, a width let go, a path deleted) is one undo step. Copying, moving or deleting the mask works as for any mask ([Moving and copying masks and filters](layers.md#moving-and-copying-masks-and-filters)).
