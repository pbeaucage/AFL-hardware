[M4x10 screws]:Parts.yaml#M4x10PanSteel
[No. 2 Phillips screwdriver]:Parts.yaml#Screwdriver_Philips_No2
# Pneumatic Module

{{BOM}}

The role of the pneumatic module is multi-fold: 

*   provide switched, high pressure (60-80 psig) nitrogen/air to the loader actuator in the robot
*	provide a series of streams of reduced pressure nitrogen to dispensing components: (15-20 psig to dispense bottles, 15-30 psig to electronic dispense regulator), including safety features like pressure relief valves
*	(in revision 2 and greater) house the electronic dispense regulator

It is worth noting that a number of configuration changes can be made in the pneumatic module to adapt the robot to locally available utilities; for instance, sometimes facilities have high-pressure filtered clean dry air available but nitrogen is only available at lower pressure.  In this case one can supply the actuator with air and the dispense system with nitrogen.

Materials:
	[AFL Pneumatic System Frame]{Qty: 1}
	[FiveWayValve]{Qty: 1}
	[AirRegulator]{Qty: 2}
	[PushConnector14NPTto14Tube]{Qty: 8}
	[PushConnector14NPTto18Tube]{Qty: 4}
	[PushConnectTee14]{Qty: 2}
	[NylonTube14OD]{Qty: 1, Unit: ft, Qty_Value: 10}
	[ETFETube18OD]{Qty: 1, Unit: ft, Qty_Value: 5}
	[M4x10 screws]{Qty: 8}
	[No. 2 Phillips screwdriver]{Qty: 1, Cat: tool}
	[RJ45 jack]{Qty: 1}

## Assemble the frame and main components {pagestep}

{{includetext: "[![](models/AFL-102-004-01-0D.stl)](models/AFL-102-004-01-0D.stl){previewpage}", if: targetformat is html}}
{{includetext: "[![](models/AFL-102-004-01-1B.stl)](models/AFL-102-004-01-1B.stl){previewpage}", if: targetformat is html}}



* 3D print the [AFL Pneumatic System Frame]{Qty: 1} if not already available.

* Setup the valves and regulators with fittings.


   - [FiveWayValve]{Qty: 1}  On the valve, install [PushConnector14NPTto14Tube]{Qty: 3} on ports marked 1, 2, and 4.  
   - [AirRegulator]{Qty: 2}: 
     - On the first regulator (actuator), install a [PushConnector14NPTtoTee14Tube]{Qty: 1} on the inlet side and a [PushConnector14NPTto14Tube]{Qty: 1} on the outlet side.  

![Actuator regulator detail](images/actuator_regulator_detail.jpg)

	 - On the other regulator (dispense), install a [PushConnector14NPTto14Tube]{Qty: 1} on the inlet side and a 
	 [14NPTnipple]{Qty: 1}, [14NPTtee]{Qty: 1}, [14NPT20psiPRV]{Qty: 1}, and [PushConnector14NPTtoTee18Tube]{Qty: 1} on the outlet side.

![Dispense regulator detail PRV](images/dispense_regulator_detail_prv.jpg)
   -  [DispenseController]{Qty: 1} install a [PushConnector14NPTto18Tube]{Qty: 1} on the inlet side and a [PushConnector14NPTto18Tube]{Qty: 1} on the outlet side.
   - [SystemEnableValve]{Qty: 1}, install a [1032to18Tube]{Qty: 1} fitting on one side, and a [1032to18TubeTee]{Qty: 1} fitting on the other side. 

* Flip the regulator dials: 
    - rotate the covering on the face with the dial in the direction indicated by the arrow, about 5-10 degrees until it lifts off:
    
    ![Regulator flip step 1](images/regulator_flip_1.jpg)

	- undo the two philips screws on that face, and the plate opposite.  Remove the plate and dial carefully.
	
	![Regulator flip step 2](images/regulator_flip_2.jpg)
	
	![Regulator flip step 3](images/regulator_flip_3.jpg)
	- install the dial on the side you took the plate off of, and the plate on the opposite side, using the screws you removed.  Tighten screws snug, you will feel the rubber o-rings engaging on both sides.
	
	![Regulator flip step 4](images/regulator_flip_4.jpg)
	
	![Regulator flip step 5](images/regulator_flip_5.jpg)
	
	![Regulator flip step 6](images/regulator_flip_6.jpg)
	- set the green arrows on the dial face to the pressure range for the regulator (10-20 psig for the dispense regulator, 40-80 psig for the actuator regulator).  These are just a usability indicator.
	- replace the faceplate aligning the grooves and rotate to lock in place.
	- you should now have a regulator that sits flat on the bottom, inlet on left, outlet on right.

* Mount the valve to the designated position on the frame using [M3x35 screws]{Qty: 3}, [M3 nuts]{Qty: 3}, and a [2.5mm hex wrench]{Qty: 1, Cat: tool}. The valve should be oriented matching the holes on the frame.

* Place the two regulators in their designated positions on the frame. One regulator will be used for the actuator pressure (60-80 psig) and the other for the dispensing pressure (15-30 psig), actuator on left, dispense on right

## Install pneumatic connections {pagestep}

* Place the fitting-equipped components into the slots on the frame.  Thread the wires from the enable valve through the slot in the bottom of its housing and into the connection box at front right.

![Pneumatic tray with components](images/pneumatic_tray_with_components.jpg)

![Pneumatic tray with components - alternate view](images/pneumatic_tray_with_components_2.jpg)

![Pneumatic tray with components - view 3](images/pneumatic_tray_with_components_3.jpg)

![Pneumatic tray with components - view 4](images/pneumatic_tray_with_components_4.jpg)

We will generally proceed in the order from inlet to outlet.

* Run a [NylonTube14OD]{Qty: 1, Unit: mm, Qty_Value: 117} from either the tee on the inlet of the actuator regulator, or a separate [14NylonPushTee]{Qty: 1} to the inlet of the dispense regulator.  If using a separate tee, run a short stub of [NylonTube14OD]{Qty: 1, Unit: mm, Qty_Value: 32} to connect the tee to the inlet of the actuator regulator - we found 32 mm sufficient for the insertion depth of two fittings.

![Pneumatic tray plumbing 1](images/pneumatic_tray_plumbing_1.jpg)

![Pneumatic tray plumbing 2](images/pneumatic_tray_plumbing_2.jpg)

* Connect the actuator regulator output to the input of the five-way valve - port #1 on the bottom using [NylonTube14OD]{Qty: 1, Unit: ft, Qty_Value: 1}.  It is easiest to make up the fitting at the regulator with excess tubing, run the line, and mark/cut the precise length to reach the valve.  We're done with the first (actuator) system!

* Next, we'll run a line from the dispense regulator output to the enable valve inlet tee (or a separate Nylon push connect tee).  Connect some [TefzelTube18OD]{Qty: 1, Unit: ft, Qty_Value: 1} to the tee, and run it to the enable valve tee on the bottom input.

![Pneumatic tray plumbing 18 to enable valve 3](images/pneumatic_tray_plumbing_18toenablevalve_3.jpg)

![Pneumatic tray plumbing 18 to enable valve 4](images/pneumatic_tray_plumbing_18toenablevalve_4.jpg)  

* Next, we'll run a line from the enable valve input to the dispense controller inlet.  Connect some [TefzelTube18OD]{Qty: 1, Unit: ft, Qty_Value: 1} to the tee, and run it to the left side of the dispense controller.  Done with dispense!

![Pneumatic tray plumbing 18 to dispense controller 5](images/pneumatic_tray_plumbing_18todispensectrl_5.jpg) 

We now have 4 exposed ports on the pneumatic controller:
 - two 1/4" push connect ports for the actuator up and down lines
 - a 1/8" push connect port for the controlled dispense
 - a 1/8" push connect port to the bottles and blowout valves


## Make up electrical connections {pagestep}

* Using a [Phillips No. 2 screwdriver]{Qty: 1, Cat: tool}, remove the two connectors from the two sides of the five-way valve.

![Pneumatic tray connector detail 1](images/pneumatic_tray_connector_detail_1.jpg)  

* It is helpful for space-saving reasons to flip the inner part of the connector so the wires face inward.  To do so, insert a [flathead screwdriver]{Qty: 1, Cat: tool} into the slot on the connector and pry the terminal block out, you may need to unscrew the top screw more to get past the captive section.  When we reassemble these connectors, we will want to have the cable exit facing the ~single~ side of the connector rather than the double.

![Pneumatic tray connector removal detail](images/pneumatic_tray_connector_removal_detail.jpg)

* Get some hook-up wire; almost any two-conductor wire will do.  We will be connecting the RJ45 jack to the control inputs of the five-way valve.  It is helpful to have two colors or ideally three - up, down, and common.  The conventions here are mostly a suggestion.

* Connect the red line to the #1 terminal inside the beige connector and a black line to the #2 terminal.  Run the wire through the strain relief and out.  Re-seat the screw, tighten the strain relief, and snap the connector into place

![Pneumatic tray connector wiring](images/pneumatic_tray_connector_wiring.jpg)

* Repeat for the blue line on the #1 terminal of the black connector.

* Connect the plugs to the five-way valve and route the wires into the connector box.

![Pneumatic tray wired connector 2](images/pneumatic_tray_wired_connector_2.jpg)

![Pneumatic tray wired connector 3](images/pneumatic_tray_wired_connector_3.jpg)

* Land the wires on the RJ45 following the pinout:

![Pneumatic tray both connectors wired](images/pneumatic_tray_both_connectors_wired.jpg)

| Pin | Color | Function |
| --- | --- | --- |
| 1   | Red   | Up |
| 2   | Black | Up-Common |
| 4   | Blue  | Down |
| 5   | Black | Down-Common |
| 7   | Black (unlabeled) | Enable |
| 8   | Black (unlabeled) | Enable-Common |

* Place the RJ45 in position and neatly store the excess wire in the box.

![Pneumatic tray with valve wiring](images/pneumatic_tray_with_valve_wiring.jpg)

![Pneumatic tray valve wiring detail](images/pneumatic_tray_valve_wiring_detail.jpg)

## Test the pneumatic system {pagestep}

* Before connecting to the robot, test the pneumatic system for leaks by applying pressure and using soapy water to check all connections.

* Verify that the regulators can be adjusted to the required pressure ranges:
  * Actuator regulator: 60-80 psig
  * Dispensing regulator: 15-30 psig

* Test the operation of the five-way valve by applying control signals through the RJ45 connection.

* Ensure that all safety features, including pressure relief valves, are functioning correctly.

## Connect to the robot system {pagestep}

* Once testing is complete, the pneumatic module is ready to be connected to the robot system.

* Connect the actuator line to the in-robot module using the appropriate tubing and connectors.

* Connect the dispensing lines to their respective components.

* Connect the RJ45 cable from the pneumatic module to the electronics module to enable control of the pneumatic system.