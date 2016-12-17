# monolayer-highlighter

In my first lab, I studied MoS2 (Molybendum Disulfide). Our fabrication process created flakes of variable thickness. To determine which ones were most thin, we had to analyze images from a constrast microscope.
![example](http://i.imgur.com/tJCGvRs.jpg)
The above shows a (compressed) sample output. The color would change relative to the thickness, so we simply needed to highlight the relevant sections for later modeling.

The code presented in this repository is a Processing method for doing so.

The program takes a target RGB color and accepted tolerances as inputs, then highlights all pixels that fit the chosen parameters and blacks out all that do not:
![output](http://i.imgur.com/CKpkzH3.jpg)

The highlight and blackout can be selected. If needed, by commenting lines n and n, the highlight/blackout colors can be not applied, preserving the colors below them. For example:
![only highlighting target](http://i.imgur.com/k0TjECz.jpg)
![only blacking out background](http://i.imgur.com/uiuRLb8.jpg)

This code can be applied to relatively large images (4000 by 2000) thanks to bit shifting where the image color data is stored.

Note that this code cannot run extremely large images; it runs into memory problems. To fix this in the future, this program should be written inside PGraphics, instead of being shown in the view window.
