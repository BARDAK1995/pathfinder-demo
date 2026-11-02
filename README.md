# PATHfinder demo

A static copy of the PATHfinder slide viewer, built for the Ashby 2026 hackathon. Open it at
https://bardak1995.github.io/pathfinder-demo/.

Every Claude answer on the page was recorded in advance. The page makes no model call.

- Region reader: Claude Sonnet 5.5 at effort medium, one recorded read for each of the 131 regions the page offers,
  recorded on 2026-11-01.
- Ask the slide and the phrase pick: answers recorded in the tests of 2026-10-18.

The page holds four colorectal slides from TCGA, one for each bin of the app's slide picker: TCGA-A6-A5ZU (viewer),
TCGA-AD-6899 (mucinous adenocarcinoma), TCGA-AD-6963 (adenocarcinoma NOS) and TCGA-AA-3660-11A-TS1 (frozen normal).
The frozen-tumour bin is left out, because none of its tiles has a ground truth to check Claude's answers against.

Ground truth comes from the tumour outlines of Loeffler and Kather, Manual tumor annotations in TCGA, Zenodo 5320076,
CC BY 4.0. The outlines do not cover all tumour, so a tile far outside an outline is only presumed not tumour.

Zooming into the map loads the slide itself, at up to 0.5 micrometres per pixel (about 20x, the resolution the two
classifiers read). The images are in `deep/`, one pyramid of 512-pixel JPEG images per slide, cut from the TCGA
whole-slide images (NCI Genomic Data Commons, open access). The page draws only the images of the area on screen.
Set the map's opacity to 0 to see the tissue in its own colours.

The page is a demonstration. It is not a diagnostic tool.
