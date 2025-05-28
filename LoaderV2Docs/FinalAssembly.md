# Final Assembly and Commissioning

## Overview
This guide covers the final assembly steps for the Autonomous Formulation Lab (AFL) system and the commissioning process to ensure all components work together properly.

## Prerequisites
Before proceeding with final assembly, ensure you have completed:
- OT-2 Hardware Modifications
- Pneumatic Module Assembly
- Electronics Module Assembly
- In-Robot Module Assembly
- LabJack Carrier Assembly



## Assembly Steps

### 1. Mounting the Side Rack
1. Attach the 80/20 rail to the OT-2 frame
2. Attach the pneumatic module to the rail system.
3. Attach the electronics module to the rail system.
4. Attach the video-UI module (if using) to the rail system.
5. Attach the in-robot module to the holes in the deck plate using 2 [1/4"-20 socket head screws]{Qty: 2}.


### 2. Make Inter-Module Connections
* Connect the wire from the electronics module to the LabJack carrier - common to the LJTick common / blue line, +24V to the brown line on the dispense controller wire.

* Connect a short RJ45 between the "actuator" port on the electronics module and the RJ45 on the pneumatic module.

* Connect the interlock harness from the in-robot module to the electronics module.

* Connect the ethernet cable from the electronics module to the switch.

* Connect ethernet cables from the video-UI Pi's (if using) and the OT-2 to the switch.

* Connect the [24V power adapter]{Qty: 1} to the electronics module.

### 3. Connecting Pneumatic Lines
1. Connect main pressure supply
2. Connect lines between Pneumatic Module and In-Robot Module (controlled dispense, blow-out, we wil attach the two rinses later)
3. Plumb the dispense bottles: 
    * place two [Duran Pressure Plus 1L bottles]{Qty: 2} in the bottle holders
    * to each bottle, attach a [GL45 two-port bottle cap]{Qty: 2}.
    * each cap will have one port that pressurizes the headspace (in) and one with a long "dip tube" that draws liquid (out).  Using [1/8" tubing] and [flangeless fittings], attach these two lines to each bottle.  The "dip tube" should extend ~past~ the ferrule to the bottom of the bottle, by pushing the tube through the fitting until about 8-10" protrudes.  On the dip tube, leave about 2 ft of tubing on the outside.  On the inlet side, 1 ft is plenty.    

    * using a length of [1/8" tubing]{Qty: 1} and a [1/8" push connect tee]{Qty: 1}, connect the outlet of the system enable valve to above the two  to the dispense bottles and install the tee.
    * connect each end of the tee to the headspace port of a bottle
    * connect the two dispense lines to the inlets of the "rinse 1" and "rinse 2" valves in the robot

4. Connect the measurement cell
    * remove the catch from the loader, and attach a length of [1/16" tubing] to it with [flangeless ferrules] (or did you attach a line earlier?)
    * connect the tubing to the inlet of your sample stick, and the outlet of the stick to a waste container
    * connect the flow-through valve's port to the dangling rj45 from the loader
    

5. Check for leaks

### 4. Plumbing the Dispense Bottles
* Make a 

## Commissioning Process

### 1. Initial Power-Up Sequence
1. Power-up checklist
2. Initial system checks

### 2. Pneumatic System Testing
1. Pressure regulation testing
2. Valve operation verification

### 3. Control System Testing
1. Communication between modules
2. Software interface testing

### 4. End-to-End Testing
1. Simple fluid transfer test
2. Complete workflow testing

## Troubleshooting

### Common Issues
1. Pneumatic leaks
2. Communication failures
3. Mechanical alignment issues

### Diagnostic Procedures
1. Systematic testing approach
2. Component isolation testing

## Maintenance Recommendations
1. Regular inspection schedule
2. Preventative maintenance tasks
