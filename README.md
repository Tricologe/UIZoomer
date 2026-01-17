# UIZoomer

UIZoomer brings vector-style navigation to the 2D interface in Roblox Studio. It allows developers to zoom and pan around ScreenGuis similarly to the 3D viewport or vector design tools like Figma.

The plugin operates non-destructively by wrapping target interfaces in temporary containers, ensuring that zoom states are not saved to the place file.

## Controls

| Action | Shortcut |
| :--- | :--- |
| **Zoom In / Out** | Ctrl + Scroll Wheel |
| **Pan View** | Ctrl + Middle Mouse Button |
| **Reset View** | Ctrl + Spacebar |

## Key Features

* **Non-Destructive Workflow:** UI elements are wrapped in temporary frames with `Archivable = false`. Saving the place while zoomed in will not persist the zoom state or the container hierarchy.
* **Smart Selection:** Logic prioritizes selected GUI objects. If no object is selected, the plugin targets the entire `StarterGui`.
* **Fluid Navigation:** Uses custom interpolation for smooth zooming and panning. Speed and damping are configurable via the settings menu.
* **Undo/Redo Support:** Fully integrated with `ChangeHistoryService` to ensure standard Studio undo operations function correctly while the plugin is active.
* **Visual Aid:** Optional bounding box visualization to delimit the zoom area.

## Installation

**Option 1: Roblox Creator Store (Recommended)**
Install directly from the Roblox Creator Store to receive automatic updates.

**Option 2: Manual Installation**
1. Download the latest `.rbxmx` file from the Releases page.
2. Drag the file into the Roblox Studio viewport.
3. Right-click the folder in the Explorer and select **Save as Local Plugin**.

## License

Distributed under the MIT License.
