
### Objectives:
To gain an in-depth understanding of buck converters:   
- Describe the working principle of a buck converter    
- Understand the relationships between key components  
- Design a buck converter with given specifications   

### Introduction:
A buck converter is a DC-DC converter that reduces input voltage to a lower, stable output voltage efficiently. It operates by switching a transistor on and off at high frequency and controlling the duty cycle of the signal. This method ensures high efficiency and precise voltage control, making buck converters crucial in applications like electronic power supplies, battery chargers, and renewable energy systems.

![image](https://github.com/user-attachments/assets/306abaab-7fee-4ee6-bbef-036f5072fec4)


### Working Principle:
1)	Switch closed:       

	![image](https://github.com/user-attachments/assets/348cebcb-b575-478f-96da-257233a2f4d5)	

	Current Path: When the switch is closed, the input voltage is directly applied across the inductor and the load.      

	Inductor Behavior: The inductor stores energy by building up a magnetic field, causing the current through it to increase.    

	Diode State: The diode is reverse-biased and does not conduct, effectively isolating the output from the input.    

	Output Capacitor: The output capacitor supplies energy to the load, smoothing the output voltage.    

	During this phase, energy is being stored in the inductor, and the output capacitor is discharging to the load, helping to maintain a steady output voltage.    


2)	Switch open:   

	![image](https://github.com/user-attachments/assets/1cb2efea-b87d-43bd-b2f5-527ffd03047c)

	Current Path: When the switch is open, the inductor releases its stored energy to the load.   

	Inductor Behavior: The magnetic field in the inductor collapses, and the inductor current flows through the diode to the load and the output capacitor.    

	Diode State: The diode becomes forward-biased and conducts, providing a path for the inductor current.    

	Output Capacitor: The output capacitor continues to smooth the output voltage by supplying energy to the load.    

	During this phase, the inductor discharges its stored energy to maintain the current flow to the load, and the output capacitor helps in stabilizing the output voltage.   

### Design:   
Given the following specifications of a PV panel:   
Vmp = 17V    
Pmp = 54V     

Design a buck converter with switching frequency of 20kHz to step down 17V to 12V.    
Vo = 12V        
fsw = 20kHz                       
             
The following values were calculated:             
T = 1e-5s              
Rload = 2.66 ohm            
D = 0.705                        
Lmin = 1.9617e-5 H               
L = 2.48e-5 H (25% increase to account for ripples and ensure CCM)                
C = 3.899e-5 F                  
Ripple Voltage = 1%                 
                  
### Simulation:                
![image](https://github.com/user-attachments/assets/4b1501c7-f90a-42a0-ab6d-7f6ce866acec)
                                
![image](https://github.com/user-attachments/assets/7d621771-3991-47d2-9793-6ea2f8a026f2)
                        
### Analysis & Conclusion:
- In the operation of a buck converter, an initial current and voltage ripple is observed before reaching a steady state. This transient phase typically lasts for a very short duration, often in the range of milliseconds.                            
- These initial ripples are a result of the converter components adjusting to the desired output conditions.                      

