# rocky-project

## 1) Initial System
### a. Motor Parameter Estimation
Given a transfer function for the motors:
$$M(s) = \frac{V(s)}{V_c(s)} = \frac{\frac{K}{\tau}}{s + \frac{1}{\tau}}$$

Given a unit step input of $v_c(t) = V_{step} * u(t)$, the time domain reponse for $v(t)$ is given by:
$$v(t) = V_{step}K(1 - e^{\frac{1}{\tau}t})$$

Linear velocity data was collected for each wheel of Rocky for a step input of $V_{step} = 300$. By fitting the time domain response equation to the collected data, the motor parameters $K$ and $\tau$ for each motor were determined to be:
$$K_{left} = 0.00275$$
$$\tau_{left} = 0.05122s$$
$$K_{right} = 0.002644$$
$$\tau_{right} = 0.05315s$$

<!--TODO: Motor cal curve fit plot-->

### b. Gyroscope Calibration
To calibrate the gyroscope, the gyroscope outputs with Rocky lying horizontally and vertically were found as follows:

- Horizontal Reading: $\pm 1.66$
- Vertical: 0.26
- Fixed Angle Correction: 0.26

### c. Natural Frequency
To calculate the natural frequency of the system, gyroscope data was collected while letting Rocky swing back and forth. By plotting the gyroscope output over time, the natural frequency could be calculated by finding the number of cycles per second and converting to radians per second:
$$\omega_{n} = 4.0998 rad/s$$

From the natural frequency, the effective length of the rod was determined as follows:

$$\omega_{n} = \sqrt{\frac{g}{l_{eff}}}$$
$$l_{eff} = 0.5836m$$

<!--TODO: Gyro cal plot-->

### d. Performance Specifications
### e. Poles
### f. Controller Parameters
### g. Simulink Model
<!--TODO: Picture of Simlink block model-->

## Stationary Balancing System
### h. Rocky Balancing Code
### g. Rocky Simulink Model
### Demos
