# 5011-Final

# MATLAB Code for two publications:

Article we based our project on: https://www.nature.com/articles/s41598-020-61414-3.pdf
Huang, Q., Lin, Y., Zhong, Q., Ma, F., & Zhang, Y. The Impact of Microplastic Particles on Population Dynamics of Predator and Prey: Implication of the Lotka-volterra Model. Sci Rep 10,4500 (2020). https://doi.org/10.1038/s41598-020-61414-3

 <details>
 <summary>How to Create Simulink</summary>
  
### How to create Simulink

  ![simulink](https://user-images.githubusercontent.com/96194504/146227437-bbc1ba00-6b73-477f-8bbd-7b79e5cda0df.jpg)

* CE - Addblock('simulink/Sources/constant')
* S1 - Addblock('simulink/Sources/constant')
* S2 - Addblock('simulink/Sources/constant')
* g1 - Addblock('simulink/Sources/constant')
* g2 - Addblock('simulink/Sources/constant')
* r10 - Addblock('simulink/Sources/constant')
* r20 - Addblock('simulink/Sources/constant')
* d1 - Addblock('simulink/Sources/constant')
* d2 - Addblock('simulink/Sources/constant')
* d3 - Addblock('simulink/Sources/constant')
* k1xCE - Addblock('simulink/Math Operations/product')
* k2xCE - Addblock('simulink/Math Operations/product')
* equ1 - Addblock('simulink/Math Operations/product')
* equ2 - Addblock('simulink/Math Operations/product')
* C1 - Addblock('simulink/Continuous/integrator')
* C2 - Addblock('simulink/Continuous/integrator')
* x1 - Addblock('simulink/Continuous/integrator')
* x2 - Addblock('simulink/Continuous/integrator')
* k - Addblock('simulink/Math Operations/gain')
* a1 - Addblock('simulink/Math Operations/gain')
* a2 - Addblock('simulink/Math Operations/gain')
* r11 - Addblock('simulink/Math Operations/gain')
* r21 - Addblock('simulink/Math Operations/gain')
* All subtraction blocks- Addblock('simulink/Math Operations/subtract')
* Prey - Addblock('simulink/Ports & Subsystems/out1')
* Predator - Addblock('simulink/Ports & Subsystems/out1')
 </details>
 
  <details>
 <summary>How to Generate Replicated Figures</summary>
 
### How to Generate Figures from 2020 Paper

* Figure 2.2 -  
* Figure 2.3 -  R
* Figures 2.4 and 2.5 - R
* Figure 2.6 - R
* Figure 3.1 - R
* Figures 3.2, 3.3 and 3.4 - R
* Figure 3.5 - R
* Figure 3.6 - R
* Figure 3.7 - R
* Figures 4.1 and 4.2 - B
* Figures 4.3 and 4.4 - S
* Figures 4.5 and 4.6 - R
* Figure 4.7 - S
* Figures 4.8-4.13  - R
* Figures 4.14 and 4.15 - R
* Figure 5.2 - P
* Figure 5.5 - R
* Figure 5.6 - R
* Figures 6.1, 6.2 and 6.3 - R
* Figure 6.4 - R
</details>

<details>
 <summary>Summary of src Codes</summary>
 
### Model Codes
* full_state_model_odes.m - function that generates ODEs for the forward locomotion system (dim neuromechanical modules)
  * full_state_model_odes_backwardsprop.m - same as above but with opposite-direction and signed proprioception
* coupled_oscillator_phase_difference_odes.m - function that generates phase-equation ODEs for the forward locomotion system (n oscillators)
   * coupled_oscillator_phase_difference_odes_backwardsprop.m - same as above but with opposite-direction and signed proprioception
* coup_currents_and_oscillator_coupling_fns.m / oscillator_coupling_fns.m - computes the coupling functions for the full coupled system from the single oscillator limit cycle and PRC
* single_oscillator_LC.m - computes the limit cycle oscillations for the single (uncoupled) neuromechanical module
*  single_oscillator_Eulerstep.m - gives an Euler's-method solution step for the single (uncoupled) neuromechanical module
* single_oscillator_PRC.m - computes the infinitessimal Phase Response Curves for the single (uncoupled) neuromechanical module
*  single_oscillator_adjoint_Eulerstep.m - gives an Euler's-method solution step for the adjoint equations to the single (uncoupled) neuromechanical module (needed to find the PRC)
* full_timetrace_to_phasediffs.m - computes phase-differences between each oscillator module in the full-state model over time from states
* full_timetrace_to_phasediffs.m - computes phase-differences between each oscillator module in the full-state model over time from states
* phasediffs_to_full_timetrace.m -  computes time-trace for the full state model from a vector of phase-locked phase differences between each oscillator module
* phases_to_init_cond.m - creates an initial condition for the full state model from a vector of initial phase differences between each oscillator module
* phase_locked_state_solve.m - solves for the phase-locked phase-differences of the full model using the phase model ODES (up to dim=4 modules)
* neuromechanical_module.ode - [XPP/Auto](http://www.math.pitt.edu/~bard/bardware/tut/xppauto.html) ode file for the single neuromechanical oscillator module 
 

### Figures/Plot Codes
* timetrace_to_curv_kym.m - creates a curvature kymograph from the time-trace of the full-state model
* blueblackred.m, bluewhitered.m, colorblind_colormap.mat, fireice.m, linspecer.m, shade.m - colormaps used for figures (not my own codes)
  </details>

# 
