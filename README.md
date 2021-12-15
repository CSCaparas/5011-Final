# 5011-Final MATLAB Code:

Article we based our project on: https://www.nature.com/articles/s41598-020-61414-3.pdf
Huang, Q., Lin, Y., Zhong, Q., Ma, F., & Zhang, Y. The Impact of Microplastic Particles on Population Dynamics of Predator and Prey: Implication of the Lotka-volterra Model. Sci Rep 10,4500 (2020). https://doi.org/10.1038/s41598-020-61414-3

 <details>
 <summary>How to Create Simulink</summary>
  
### How to create Simulink 'FinalModel'

  ![simulink](https://user-images.githubusercontent.com/96194504/146227437-bbc1ba00-6b73-477f-8bbd-7b79e5cda0df.jpg)

* CE - Addblock('simulink/Sources/constant'); 30
* S1 - Addblock('simulink/Sources/constant'); 0.042
* S2 - Addblock('simulink/Sources/constant'); 0.039
* g1 - Addblock('simulink/Sources/constant'); 1.2
* g2 - Addblock('simulink/Sources/constant'); 1.3
* r10 - Addblock('simulink/Sources/constant'); 4.1
* r20 - Addblock('simulink/Sources/constant'); 4.0
* d1 - Addblock('simulink/Sources/constant'); 0.1
* d2 - Addblock('simulink/Sources/constant'); 0.002
* d3 - Addblock('simulink/Sources/constant'); 0.002
* k1xCE - Addblock('simulink/Math Operations/product')
* k2xCE - Addblock('simulink/Math Operations/product')
* equ1 - Addblock('simulink/Math Operations/product')
* equ2 - Addblock('simulink/Math Operations/product')
* C1 - Addblock('simulink/Continuous/integrator'); C1(0)=0
* C2 - Addblock('simulink/Continuous/integrator'); C2(0)=0
* x1 - Addblock('simulink/Continuous/integrator'); x1(0)=100
* x2 - Addblock('simulink/Continuous/integrator'); x2(0)=10
* k - Addblock('simulink/Math Operations/gain'); 2
* a1 - Addblock('simulink/Math Operations/gain'); 0.052
* a2 - Addblock('simulink/Math Operations/gain'); 0.052
* r11 - Addblock('simulink/Math Operations/gain'); r11
* r21 - Addblock('simulink/Math Operations/gain'); r21
* All subtraction blocks- Addblock('simulink/Math Operations/subtract')
* Prey - Addblock('simulink/Ports & Subsystems/out1')
* Predator - Addblock('simulink/Ports & Subsystems/out1')
 </details>
 
  <details>
 <summary>How to Generate Replicated Figures</summary>
 
### How to Generate Figure 2 from 2020 Paper

![2 1](https://user-images.githubusercontent.com/96194504/146249654-aaf06bfc-6547-464d-b0cf-695f5ccf1fcd.jpg)
![2 2](https://user-images.githubusercontent.com/96194504/146249657-782296f4-60f9-4c8d-a16d-93f19f12e29b.jpg)
* Figure 2a.1 and 2a.2 - Run sim('FinalModel') with r11=0, r21=0

![2b 1](https://user-images.githubusercontent.com/96194504/146249691-ebed31a2-9c81-425c-84e4-2311efe20f90.jpg)
![2b 2](https://user-images.githubusercontent.com/96194504/146249692-70c6efb8-b17a-44bf-b9da-cb4ecc00cdac.jpg)
* Figure 2b.1 and 2b.2 - Run sim('FinalModel') with r11=0.1, r21=0.1
 
![2b 3](https://user-images.githubusercontent.com/96194504/146250177-02655a75-3372-47d1-88cc-ce7642911b4a.jpg)
![2b 4](https://user-images.githubusercontent.com/96194504/146250182-a73c9fb0-8459-454f-9f92-0830fb1563e7.jpg)
* Figure 2b.3 and 2b.4 - Run sim('FinalModel') with r11=1.0, r21=1.0
 
![2b 5](https://user-images.githubusercontent.com/96194504/146250212-4339d8d0-d5d0-4dba-a24b-8ffc3734f409.jpg)
![2b 6](https://user-images.githubusercontent.com/96194504/146250215-53a654f3-23c3-4bcc-a96c-58756fae3437.jpg)
* Figure 2b.5 and 2b.6 - Run sim('FinalModel') with r11=10.0, r21=10.0
 
![2c 1](https://user-images.githubusercontent.com/96194504/146250239-229c9f59-c604-4fb2-8fd0-9daeb994b424.jpg)
![2c 2](https://user-images.githubusercontent.com/96194504/146250243-6ce9b45c-b882-4e4d-af18-69c82538837f.jpg)
* Figure 2c.1 and 2c.2 - Run sim('FinalModel') with r11=0.01, r21=0.1
 
![2c 3](https://user-images.githubusercontent.com/96194504/146250270-55286f8d-a4f3-4293-9aab-537fa7c675a9.jpg)
![2c 4](https://user-images.githubusercontent.com/96194504/146250273-1d4acb43-f07d-4bbd-9069-1851d9ecc235.jpg)
* Figure 2c.3 and 2c.4 - Run sim('FinalModel') with r11=1.0, r21=10.0
 
![2d 1](https://user-images.githubusercontent.com/96194504/146250340-6768e2fd-7956-4249-a731-09f934c57862.jpg)
![2d 2](https://user-images.githubusercontent.com/96194504/146250342-d1bb4f5f-d412-4f43-8be0-5b369154c1ec.jpg)
* Figure 2d.1 and 2d.2 - Run sim('FinalModel') with r11=1.0, r21=0.1
 
![2d 3](https://user-images.githubusercontent.com/96194504/146250366-5abd9800-cf83-4aa8-82c6-1c296ca726b8.jpg)
![2d 4](https://user-images.githubusercontent.com/96194504/146250370-b6199603-043d-486f-a9b2-65c96179b9fc.jpg)
* Figure 2d.3 and 2d.4 - Run sim('FinalModel') with r11=5.0, r21=0.5
 
![2d 5](https://user-images.githubusercontent.com/96194504/146250398-92e65655-09cf-4903-8f94-5a8c898b6450.jpg)
![2d 6](https://user-images.githubusercontent.com/96194504/146250401-7740c5bf-960c-4c80-bb1d-71c5320164ba.jpg)
* Figure 2d.5 and 2d.6 - Run sim('FinalModel') with r11=10.0, r21=1.0
 
</details>

### How to Generate Figure 4 from 2020 Paper

![2 1](https://user-images.githubusercontent.com/96194504/146249654-aaf06bfc-6547-464d-b0cf-695f5ccf1fcd.jpg)
![2 2](https://user-images.githubusercontent.com/96194504/146249657-782296f4-60f9-4c8d-a16d-93f19f12e29b.jpg)
* Figure 2a.1 and 2a.2 - Run sim('FinalModel') with r11=0, r21=0

![2b 1](https://user-images.githubusercontent.com/96194504/146249691-ebed31a2-9c81-425c-84e4-2311efe20f90.jpg)
![2b 2](https://user-images.githubusercontent.com/96194504/146249692-70c6efb8-b17a-44bf-b9da-cb4ecc00cdac.jpg)
* Figure 2b.1 and 2b.2 - Run sim('FinalModel') with r11=0.1, r21=0.1
 
* Figure 2b.3 and 2b.4 - Run sim('FinalModel') with r11=1.0, r21=1.0
 
* Figure 2b.5 and 2b.6 - Run sim('FinalModel') with r11=10.0, r21=10.0
 
* Figure 2c.1 and 2c.2 - Run sim('FinalModel') with r11=0.01, r21=0.1
 
* Figure 2c.3 and 2c.4 - Run sim('FinalModel') with r11=1.0, r21=10.0
 
* Figure 2d.1 and 2d.2 - Run sim('FinalModel') with r11=1.0, r21=0.1
 
* Figure 2d.3 and 2d.4 - Run sim('FinalModel') with r11=5.0, r21=0.5
 
* Figure 2d.5 and 2d.6 - Run sim('FinalModel') with r11=10.0, r21=1.0
 
* Figure 2c.3 and 2c.4 - Run sim('FinalModel') with r11=1.0, r21=10.0
 
* Figure 2d.1 and 2d.2 - Run sim('FinalModel') with r11=1.0, r21=0.1
 
</details>

<details>
 <summary>Summary of src Codes</summary>
 

### Figures/Plot Codes
* sim('FinalModel'); runs 'FinalModel' simulink and exports output to Matlab workspace as 'ans'
* plot(ans.yout{1}.Values,'Linewidth',2); Plots Prey outputs vs time
* plot(ans.yout{2}.Values,'Linewidth',2); Plots Predator outputs vs time
* plot(ans.yout{1}.Values.Data,ans.yout{2}.Values.Data,'Linewidth',2); Plots Prey outputs vs Predator Outputs [Phase Portrait]
 
# 
