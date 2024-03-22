# Theory

 **Rectilinear Motion:**
				  
Rectilinear motion is another name of straight-line motion. This type of motion describes the movement of a particle or a body.
A body is said to experience rectilinear motion if any two particles of the body travel the same distance along two parallel straight lines.
The fig 1 illustrates rectilinear motion for a body.
						   
<div align = "center">
<img alt="" src="./images/rectibody.png" class="img-fluid">
<b>Fig 1: Rectilinear Motion</b>
</div>
							
The experimental control system in practical laboratory is comprised of the electromechanical plant which consists of the spring-mass mechanism, its actuator and sensors and a subsystem 
i.e. an operating program or software which runs on a PC.
<b>Encoder:</b>

An encoder is a sensor that converts a positional output into an electronic signal. In this experiment, encoder counts are used as the system units of position, where the counts correspond to the encoder pulses and controller-internal register values. Here, 1 encoder revolution is equivalent to 16,000 encoder counts, which corresponds to 7.06 cm.
								
                                                            
**Rectilinear Motion Setup in Control Systems:**

<div align = "center">
<img alt="" src="./images/plant.png" class="img-fluid">
<b>Fig 2: Rectilinear Motion Setup without dashpot connected</b>
</div>
<div align="center">
<img alt="" src="./images/plant2.png" class="img-fluid"><br/>
<b>Fig 3: Rectilinear Motion Setup with dashpot connected</b>
<img alt="" src="./images/tfequation.png" class="img-fluid">
</div>
Re arranging the equation (2) and comparing the denominator terms with the characteristics equation of a second order control system we get,

$$s^2 + 2 \zeta \omega_n s + \omega_n^2 = s^2 + \frac{c}{m}s + \frac{k}{m}$$
								
$$\omega_n^{2} = \frac{k}{m}$$

$$\zeta (damping \ ratio) = \frac{c}{2 \sqrt{k m}}$$

$$\omega_d = \omega_n \sqrt{(1 - \zeta^{2})}$$
								
Where,
								
m = Total mass (mass of the cart + weights)

k = Spring constant

c = Damping coefficient

F(t) = Applied force

X(t) = Time-Varying position of the cart

&omega;<sub>n</sub> = Natural frequency of oscillations

&omega;<sub>d</sub> = Damped natural frequency of oscillations
								
								
<div align = "center">
<img alt="" src="./images/plot.png" class="img-fluid"></br>
<b>Fig 4: Open loop step plot for 1 kg mass on Mass Spring Damper system without connecting the dashpot</b>
</div>
<div align = "center">
<img alt="" src="./images/tpic.png" class="img-fluid"></br>
<b>Fig 5: Rectilinear Plant</b>
</div>

								
The hardware gain, k<sub>hw</sub>,  of the system is comprised of the product: k<sub>hw</sub> = k<sub>c</sub> k<sub>a</sub> k<sub>t</sub> k<sub>mp</sub> k<sub>e</sub> k<sub>ep</sub> <!--k<sub>s</sub>--> 

where the theoretical values are:

k<sub>c</sub>, the DAC gain, = 10V / 32,768 DAC counts

k<sub>a</sub>, the Servo Amp gain, = approx 2 (amp/V)

k<sub>t</sub>, the Servo Motor Torque constant =  approx 0.1 (N-m/amp)

k<sub>mp</sub>, the Motor Pinion pitch radius inverse = 26.25 m-1

k<sub>e</sub>, the Encoder gain, = 16,000 pulses / 2&#960; radians

k<sub>ep</sub>, the Encoder Pinion pitch radius inverse = 89 m-1
                              

						
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>								
