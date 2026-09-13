# AE Modular KiCad Templates

A set of blank KiCad templates for designing custom [AE Modular](https://www.aemodular.com/) synthesizer modules. 

These templates were designed to provide a robust starting point that strictly respects real-world mounting constraints while keeping the PCB design process as straightforward as possible.

## Key Features

* **Mounting-Hole Referenced:** These templates calculate all critical dimensions relative to the mounting hole axes. The mounting holes are the primary reference points that position the module in the physical system, maintaining a strict 25.4mm horizontal pitch.
* **Integrated Front Panels:** The front panel outline (`Edge.Cuts`) and mounting holes are included directly within the main PCB file. You can design your panel side-by-side with your circuit, or simply copy the outline to a new file if you prefer a separate project.

## 100mm vs 101mm Variants

The repository includes templates for 1U, 2U, 3U, and 4U widths. Each width comes in two vertical dimensions (and horizontal for 4U), following this naming convention (e.g., for 1U):

* **`ae_tpl_1u` (101mm - Official):** True to the original AE Modular hardware specifications.
* **`ae_tpl_1u_100mm` (100mm - Fab-Friendly):** Shaved down by 0.5mm on the top and bottom. Since many PCB fabs have a strict price jump for anything over 100x100mm, this version keeps your boards in the cheapest prototyping tier while still fitting perfectly into standard AE cases. 

*(Note: This 100x100mm limit is also why the templates stop at 4U. To keep the 4U "Fab-Friendly" version in the cheapest tier, its horizontal width is also shaved down by about 1mm so it fits exactly within the 100x100mm maximum).*

## How to Install and Use

1. Download or clone this repository.
2. Copy the template folders into your KiCad user templates directory:
   * **Windows:** `C:\Users\<YourUsername>\Documents\KiCad\10.0\template\`
   * **macOS:** `~/Documents/KiCad/10.0/template/`
   * **Linux:** `~/.local/share/kicad/10.0/template/`
   *(Adjust the version number based on your KiCad installation).*
3. Open KiCad, click **File -> New Project from Template...**, select the "User Templates" tab, and choose your desired AE Modular size.

## Background

I originally developed these templates for upcoming **Moonbase** DIY module series. Since the alignment and grid logic turned out to be incredibly solid, I decided to release them as a universal open-source tool for the entire AE Modular community. 

## License

This project is open-source and available under the [MIT License](LICENSE). Feel free to use these templates for both personal DIY projects and commercial modules.
