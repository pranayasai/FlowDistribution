# FlowDistribution
<H2>Description:</H2>
Version 3.0.0<br>
Title: Flow Distribution in a Doublet EGS<br>
Authors: Pranay Asai (UoU) & Robert Podgorney (INL)<br>
Edited by: Pranay Asai<br>
Date: 06/26/2021<br>
<br>
It allows your to evaluate fluid flow distribution in a multi-fractured doublet (EGS) Enhanced Geothermal System model.

<H2>Rules/Assumptions:</H2>
1. Fluid flows from high pressure zone to low pressure zone.<br>
2. Gravity is not included.<br>
3. Constant density and viscosity is used (Isothermal).<br>
4. Fractures are rectangular and Darcy's law used to solve for pressure drop.<br>
5. Frictional pressure drop is calculated using various flow equations depending on the Reynolds number.<br>
6. All the fractures are identical and have same width (calculated using cubic law).<br>


<H2>How to use it:</H2>
<pre> 
1. Download both the files and make sure they are in the same folder.
2. Open the files in Jupyter Lab
3. Add path(windows or macOS) to save the output.
4. Input all the parameters the Fracture, Pipe (wellbore) and Perforations (all the values in SI units).
5. All variables are initalized
6. Input flowrate and injection pressure
7. CONTROL variables would help to run a specific scenario.
    7.1.  Turn on pressure drop in Wells
      7.1.1.  If 1, the pressure drop in the Injection well is on.
      7.1.2.  If 1, the pressure drop in the Production well is on.
    7.2.  Activate Perforations
      7.2.1.  If 0, Production perforation pressure drop is zero.
      7.2.2.  If 0, Injection perforation pressure drop is zero.
    7.3.  Permeability of Fracture
      7.3.1.  If 0, All fractures have same permeability.
      7.3.2.  If 1, The permeability values are assigned at random with respect to the base value.
                The permeabilities are assigned at random using two random values. The first value is the base and the second is the magnitude.
                Permeability=var1*BasePermeability*(10^var2)
      9.3.3.  If 2, Option to input custom permeability values.
                Input custom values for all the fractures.
    7.4.  Well Orientations
      7.4.1.  If 1, The wells are Parallel
      7.4.2.  If 2, The wells are Anti-Parallel
      7.4.3.  If 3, The wells are Non-Parallel
        7.4.3.1.  Input the Difference between first and last fracture
    7.5. Adaptive Perforations (This is still in the test phase and not fully developed)
      7.5.1.  If 0, Adaptive Perforations are turned off
      7.5.2.  If 1, Adaptive Perforations are turned on
      7.5.3.  If 2, Custom input for Perforations
 8. The setup of control variables would give the output for the desired scenario.
 </pre>
