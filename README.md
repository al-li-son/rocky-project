# rocky-project

## 1) Initial System
### a. Motor Parameter Estimation
Given a transfer function for the motors:
$$M(s) = \frac{V(s)}{V_c(s)} = \frac{\frac{K}{\tau}}{s + \frac{1}{\tau}}$$

Given a unit step input of $v_c(t) = V_{step} * u(t)$, the time domain reponse for $v(t)$ is given by:
$$v(t) = V_{step}K(1 - e^{\frac{1}{\tau}t})$$

Linear velocity data was collected for each wheel of Rocky for a step input of $V_{step} = 300$. By fitting the time domain response equation to the collected data, the motor parameters $K$ and $\tau$ for each motor were determined to be:
$$K_{left} = 3.05*10^{-3}$$
$$\tau_{left} = 0.051s$$
$$K_{right} = 2.98*10^{-3}$$
$$\tau_{right} = 0.0519s$$

### b. Gyroscope Calibration
Fixed Angle Correction: 0.28
