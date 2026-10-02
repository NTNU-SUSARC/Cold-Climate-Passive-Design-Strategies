# Ground Temperature and Earth Berming

To set ground temperatures by hand, use the ```add_str_``` input on the **```HB Model to OSM```** component.
```
Site:GroundTemperature:BuildingSurface,
  18.0,  !- January
  17.5,  !- February
  15.0,  !- March
  12.0,  !- April
  10.0,  !- May
  9.0,   !- June
  9.5,   !- July
  11.0,  !- August
  13.0,  !- September
  15.0,  !- October
  16.5,  !- November
  17.5;  !- December
```
To do this automatically with ground temperatures from the ```EPW``` (for depths of 0.5 m, 2 m and 4 m), components are already provided in the [ground_temp_and_earth_berming.gh](ground_temp_and_earth_berming.gh) example file.

For depths below 4 m, we can **approximate(!)** ground temperatures with the following formula (Labs, 1779):

$T(x,t) = T_m - A_s \cdot e^{-x \sqrt{\frac{\pi}{365\alpha}}} \cdot \cos\left(\frac{2\pi}{365} \left[ t - t_o - \frac{x}{2} \sqrt{\frac{365}{\pi\alpha}} \right]\right)$, where:

*$T_{(x t)}$ = Ground temperature at depth $x$ and day $t$
* $T_m$ = mean annual temperature of the ground
* $A_s$ = annual range of the surface temperature
* $t$ = day of the year
* $t_o$ = day with minimum surface temperature
* $a$ ($\alpha$) = soil thermal diffusivity
* $x$ = depth below the ground surface
  
> Use this for depths below 10 m, accuracy varies for shallower depths.

Components are provided in the example file.
