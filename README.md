# Thermal Expansion Compensation Package
A collection of gcode macros and guides to combat the effects of bimetallic (and normal) thermal expansion for enclosed 3D printers running Klipper.

If you suffer from any of the following:
1) Nicely laid first layer, but second layer is too high and looks like crap
2) Z offset changes between prints (too high when the printer is heatsoaked, but too low when it is not, or vice versa)
3) Bed mesh doesn't seem to work well on full plates
4) Have to heatsoak the printer for hours just for the above problems to disappear

Check out the following repositories:

[Virtual Gantry Backers](https://github.com/Deutherius/VGB), a dynamic mesh loading system that counteracts gantry bowing due to bimetallic thermal expansion of gantry members

[Gantry bowing-induced Z-offset correction through relative reference index](https://github.com/Deutherius/Gantry-bowing-induced-Z-offset-correction-through-relative-reference-index), to fix that inconsistent Z offset between heatsoaked and not-as-well heatsoaked printer

[Dumb Frame Comp](https://github.com/Deutherius/DFC), to counteract vertical frame member expansion and fix the first-second layer transition issues

It looks daunting at first, but setting it up is actually very simple (detailed instructions included!), and in my case (using a Voron 2.4 300mm spec), I can literally start a print without heatsoaking for more than 5 minutes and get a nigh *perfect* first layer squish and consistent layers regardless of whether the printer is at ambient temps or heatsoaked from printing all day. All of that without any additional hardware except *one thermistor*.
