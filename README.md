# Drug Targets 3D — Desk & Bench

Everyday medicines and their target proteins in 3D, for undergraduate students. Part of the Study Hall in [Desk & Bench](https://ugurlab.github.io/desk-and-bench/).

- Open the app: https://ugurlab.github.io/drug-targets-3d/app/
- Tool page: https://ugurlab.github.io/drug-targets-3d/
- ZIP package (offline use on a computer): https://ugurlab.github.io/drug-targets-3d/drug-targets-3d.zip
- Catalogue: https://ugurlab.github.io/desk-and-bench/

The tool page uses the catalogue's shared stylesheet and rules: read https://github.com/ugurlab/desk-and-bench/blob/main/DESIGN.md before editing it.

## Files
| File | Purpose |
| --- | --- |
| `app/index.html` | The app itself, a single HTML file with the 3D viewer and structure data inside. The ZIP contains the same file as `drug-targets-3d.html` |
| `index.html` | The tool page |
| `drug-targets-3d.zip` | `drug-targets-3d.html` and `READ-ME.txt` |
| `assets/` | Screenshots |

## Use
Open the app from the link above on a computer, tablet or phone. To use it offline on a computer, extract the ZIP and open `drug-targets-3d.html` in Chrome, Edge or Firefox. The app keeps nothing between visits and sends nothing over the internet.

## What it covers

For each drug:

- **Bind the drug:** the protein and the drug start apart; a button moves the drug into its crystal-structure pose.
- **Zoom to the pocket:** a close-up of the interactions that hold the drug (salt bridges, hydrogen bonds, non-polar contacts), with distances.
- **Can the substrate get in?:** the natural substrate enters the empty site and leaves as product; with the drug bound, it is blocked.
- **Check yourself:** a short question, and the structure and literature sources.

Version 1.0 has one drug: **ibuprofen** and its target, **cyclooxygenase (COX-1)**.

## Data and sources
- Ibuprofen in sheep COX-1: PDB [1EQG](https://www.rcsb.org/structure/1EQG); Selinsky et al., *Biochemistry* 2001, [doi:10.1021/bi010045s](https://doi.org/10.1021/bi010045s). Chain A, rotated into a display frame. Measured contacts: carboxylate O–Arg120 2.8–2.9 Å (salt bridge), O–Tyr355 OH 2.8 Å (hydrogen bond).
- Arachidonic acid in sheep COX-1: PDB [1DIY](https://www.rcsb.org/structure/1DIY); Malkowski et al., *Science* 2000, [doi:10.1126/science.289.5486.1933](https://doi.org/10.1126/science.289.5486.1933). Superposed on 1EQG (551 Cα atoms, RMSD 0.5 Å).
- Both coordinate files were downloaded from RCSB and checked against the live files by SHA-256. PDB data are available under CC0 1.0.
- The bound poses are the crystal poses. The paths in and out, the stop at the drug and the colour change to the product are drawn for illustration; the product is not shown with its real shape.
- 2D structures were drawn with RDKit.

## Changes
- 1.0: First release, with ibuprofen and cyclooxygenase.

## Credits

Drug Targets 3D was designed by Ugur Comlekcioglu and built with Claude (Anthropic).

The 3D viewer is [3Dmol.js](https://3dmol.csb.pitt.edu/) 2.5.5 (BSD-3-Clause), bundled in the HTML file together with the licence texts of its components.

## Licence
Drug Targets 3D is open source under the [MIT License](LICENSE). You are welcome to use, change and share it, including in your own projects, as long as you keep the copyright notice and the licence text, which credit the original author. The licence text is also kept in a comment at the top of the app's HTML file, together with the licences of the bundled 3D viewer, so every downloaded copy carries them.
