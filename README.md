# 🛰️ Satellite Launch Velocity Optimization & Orbit Simulation

This project models a satellite launch as a **2D velocity optimization problem** and simulates its orbit using **Newton’s law of gravitation**.

## 🔧 Numerical Methods Used (Course Scope)
- **Newton’s Method** → Solves ideal circular orbit speed magnitude  
  $F(v) = v^2 - \mu/r_0 = 0$
- **Multi-Dimensional Gradient Descent** → Optimizes launch velocity vector  
  $\mathbf{v}_{k+1} = \mathbf{v}_k - \alpha \nabla C(v_x, v_y)$  
  where $C = e^2$ (orbital eccentricity²)

## 📊 Visualization
- Cost vs iteration (convergence)
- $v_x$, $v_y$ vs iteration (stability)
- Orbit path plots (initial vs optimized vs circular reference)

## 🎯 Goal
Find a realistic velocity vector $(v_x, v_y)$ that produces a near-circular orbit by minimizing eccentricity².

## 🧪 Implementation
Fully built in **Jupyter Notebook** with embedded math, solver loops, and plots.  
(Default parameters use Earth gravitational constant $\mu = 398600\ \text{km}^3/\text{s}^2$ and launch radius $r_0 = 6771\ \text{km}$)

## ✅ Outcome
- Circular speed baseline found ≈ **7.67 km/s** (Newton converges fast)
- GD gradually reduces $e^2$ over iterations
- Optimized vector forms a realistic near-circle orbit after enough steps

## 🧾 Notes
- Uses **standard GD with fixed step size (`α`)**
- Euler orbit stepping is only used inside the simulator, not as a solver
