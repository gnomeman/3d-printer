# Print in air after bed level

Date: FEB-11-2024


## Issue

The printer would not print on the bed, rather it would print a few mm above the surface.
This was still a problem after height mapping and KAMP plugin install.


## Troubleshooting

1. Print in the air, not on surface
1. What is the 1st layer height in the slicer?
	- Default 0.2
	- Changed to 0.09 and saw little no changes in behavior
1. What is the offset in Klipper?
	- [Calibrated X and Y offset](https://www.klipper3d.org/Probe_Calibrate.html)
	- Calibrate Z axis offset
	- Physically clean and grease Z axis rod
	- Little to no effect
1. What does the START_PRINT macro look like?
	- I didn't have one and relied on slicer
	- Wrote a custom macro for starting and stopping
	- Having moderate success and prints are printing on surface
