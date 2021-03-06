# Thermal Expansion Compensation Package
A collection of gcode macros and guides to combat the effects of bimetallic (and normal) thermal expansion for enclosed 3D printers running Klipper.

If you suffer from any of the following:
1) Nicely laid first layer, but second layer is too high and looks like crap
2) Z offset changes between prints (too high when the printer is heatsoaked, but too low when it is not, or vice versa)
3) Bed mesh doesn't seem to work well on full plates
4) Have to heatsoak the printer for hours just for the above problems to disappear

Check out the following repositories:

[Gantry bowing-induced Z-offset correction through relative reference index](https://github.com/Deutherius/Gantry-bowing-induced-Z-offset-correction-through-relative-reference-index), to fix that inconsistent Z offset between heatsoaked and not-as-well heatsoaked printer (pairs nicely with virtual gantry backers, but do this one first)

[Virtual Gantry Backers](https://github.com/Deutherius/VGB), a dynamic mesh loading system that counteracts gantry bowing due to bimetallic thermal expansion of gantry members

~~[Dumb Frame Comp](https://github.com/Deutherius/DFC), to counteract vertical frame member expansion and fix the rest of the first-second layer transition issues~~
There is a bug in the current version of dumb frame comp which causes random blobs to appear on curved sections of prints. Do not use DFC, go with the [Frame Comp](https://github.com/alchemyEngine/klipper_frame_expansion_comp) Moonraker plugin instead. If you are running DFC, remove it from your printer config (disabling it through enable=0 is *not* enough) and burn it to the ground. Sorry if this issue affected you.

It looks daunting at first, but setting it up is actually very simple (detailed instructions included!), and in my case (using a Voron 2.4 300mm spec), I can literally start a print without heatsoaking for more than 5 minutes and get a nigh *perfect* first layer squish and consistent layers regardless of whether the printer is at ambient temps or heatsoaked from printing all day. All of that without any additional hardware except *one thermistor*.

These three are meant to be used together as they solve intertwined issues, but you can omit some of them if you don't need them, i.e. if you run physical gantry backers on a small-enough printer and your gantry does not bow, you likely don't need the first two (maybe consider just frame comp).
