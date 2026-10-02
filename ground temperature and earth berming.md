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
To do this automatically with ground temperatures from the ```EPW``` (for depths of 0.5 m, 2 m and 4 m), components are already provided in the [ground_temp_and_earth_berming.gh](ground_temp_and_earth_berming.gh).
