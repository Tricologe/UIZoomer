# UIZoomer for Roblox Studio

**UIZoomer** is a robust Roblox Studio plugin that brings vector-style navigation to your 2D Interface. It allows you to zoom and pan around your ScreenGuis just like you navigate the 3D viewport or design tools like Figma.

It works by temporarily wrapping your UI in a container with a `UIScale`, ensuring a smooth, non-destructive workflow that doesn't mess up your actual UI properties when saving.

## 🎮 Controls

The plugin uses **Ctrl** (or Command on Mac) as the primary modifier key to prevent conflicts with standard Studio scrolling.

| Action | Input | Description |
| :--- | :--- | :--- |
| **Zoom In/Out** | `Ctrl` + `Scroll Wheel` | Zoom in towards your mouse cursor. |
| **Pan View** | `Ctrl` + `Middle Mouse Click` | Hold and drag to move around the canvas. |
| **Reset View** | `Ctrl` + `Spacebar` | Instantly resets zoom to 100% and centers the view. |

> **Note:** You can customize the Zoom Speed, Smoothness, and Invert Zoom direction in the settings menu.

## ✨ Key Features

* **Smooth Interpolation:** Features a custom render loop with adjustable smoothness for a "buttery" feel when zooming and panning.
* **Selection Mode:** Choose between zooming the entire `StarterGui` or focusing only on the specific UI element you have selected.
* **Non-Destructive:** The plugin wraps your UI in temporary frames that have `Archivable = false`. This means you can save your place while zoomed in, and it **won't** save the zoom state or the temporary containers to your file.
* **Undo/Redo Support:** Integrated with `ChangeHistoryService` to handle undo actions gracefully without breaking the wrapper state.
* **Visual Border:** Optional customizable border that draws around your UI while zooming, helping you visualize the bounds of your interface.
* **Custom Color Picker:** Includes a built-in HSV/Hex color picker for customizing the UI border.

## ⚙️ Settings

Click the **Settings** button in the toolbar to configure:

* **Behavior:** Toggle "Target Selection Only" to limit zooming to specific objects.
* **Motion:** Adjust **Smoothness Amount** and **Zoom Speed**.
* **Visuals:** Toggle the bounding border, change its **Thickness** (positive for outer, negative for inner), and adjust the **Color**.

## 🔧 How It Works

When activated, UIZoomer:
1.  Creates a temporary `Frame` (Container) with a `UIScale`.
2.  Parents your target UI elements into this container.
3.  Manipulates the `UIScale` and `Position` of the container based on your input.
4.  Automatically unwraps and restores original parents when you disable the plugin or unload it.

## 📥 Installation

1.  Download the latest release or grab the model from the Roblox Marketplace.
2.  Open Roblox Studio.
3.  Navigate to the **Plugins** tab and enable **UIZoomer**.

## 📝 License

This project is open-source. Feel free to modify and use it in your projects.
