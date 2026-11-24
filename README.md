# Impulsive Delay Differential Equations (DDE) Simulator

Interactive numerical and graphical solver for nonlinear systems of **Impulsive Delay Differential Equations** with state-dependent switching surfaces ($\tau_1, \tau_2$), developed as part of PhD mathematical research by **Dr. Adem Ibushev Zeinev (PhD)**.

🔗 **Live Interactive Simulator:** [https://azeynev.github.io/impulsive-dde-simulator/](https://azeynev.github.io/impulsive-dde-simulator/)

## Mathematical Model

The simulator solves the coupled system with constant delay $\tau = 0.5$:

$$
\begin{cases}
x'(t) = x(t) + \cos^2 x(t - 0.5) + \sin^2 y(t - 0.5) - 1.1 \\
y'(t) = y(t) + \sin^2 x(t - 0.5) + \cos^2 y(t - 0.5) + 0.1
\end{cases}
$$

with initial history function $x(t) \equiv y(t) \equiv 0.05$ for $t \in [-0.5, 0]$, subject to state-dependent impulse surfaces:
* **Surface $\tau_1$:** $x + y = t + 0.08$ with jump $\Delta_1 = \left(\frac{\sin^2(x)}{20}; \frac{\cos^2(x)}{10}\right)$
* **Surface $\tau_2$:** $x + y = t + 1$ with jump $\Delta_2 = \left(\frac{\cos^2(y)}{10}; \frac{\sin^2(y)}{5}\right)$

## Key Features
* **Numerical Integration:** 2nd-order Runge-Kutta (RK2) solver with history buffer interpolation and configurable step size.
* **Dual Visualization (Plotly.js):** Real-time time-series plots $x(t), y(t)$ (linear & logarithmic scales) and 2D phase-plane trajectories showing state jumps and switching lines.
* **Impulse Event Log:** Automatic detection and breakdown of exact switching times, pre/post-impulse states, and jump magnitudes ($\Delta x, \Delta y$).

## Author
**Dr. Adem Ibushev Zeinev, PhD**  
Digital Educational Library: [https://azeynev.github.io/materials/](https://azeynev.github.io/materials/)
