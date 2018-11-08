# mkc-configuration

## Start G-code
```
G28 ;Home
G1 Z15.0 F6000 ;Move the platform down 15mm
;Prime the extruder
G92 E0
G1 F200 E15
G92 E0
```

## End G-code
```
M104 S0
M140 S0
;Retract the filament
G92 E1
G1 E-1 F300
G1 Z215
G28 X0 Y0
G1 X5 Y-10
M84
```
