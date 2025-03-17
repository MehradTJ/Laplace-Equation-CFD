# 🔥 Numerical Solution of 2D Laplace Equation 🔥

## 📌 Overview
This project aims to solve the **2D Laplace equation**, which governs steady-state heat conduction in a domain, using **various numerical methods**. The methods include:
- ✅ Gauss-Seidel Method
- ✅ Jacobi Method
- ✅ Successive Over-Relaxation (SOR)
- ✅ Line SOR (Semi-Implicit)
- ✅ Fully Implicit Method

The project also evaluates **accuracy** and **CPU runtime** for different **mesh sizes**.

---

## 🖼️ Problem Description
The **physical domain** and boundary conditions are shown below:

![Problem Domain](problem-1.png)  
*Figure 1: Schematic of the Physical Problem Domain Showing Geometry and Boundary Conditions*

The **Laplace equation in 2D**:

$$
\frac{\partial^2 T}{\partial x^2} + \frac{\partial^2 T}{\partial y^2} = 0
$$

The **exact solution** for the problem:

$$
T(x,y) = \frac{\sinh(\pi y)}{\sinh(\pi)} \sin(\pi x)
$$

where \(T(x,y)\) represents the temperature distribution in the domain.

---

## 📂 Project Structure
📁 **Numerical-Laplace-Solver**  
├── 📜 `code.ipynb` - Jupyter Notebook with implementation 🧑‍💻  
├── 📜 `requirements.txt` - Required Python libraries 📦  
├── 📜 `README.md` - Project documentation 📖  
└── 📜 `LICENSE` - License file ⚖️  

---

## 🛠️ Implementation Details
✅ The code is written in **Python** using **Jupyter Notebook**.  
✅ The domain is discretized with **mesh sizes**: `10x10`, `20x20`, `30x30`, `40x40`.  
✅ The solution convergence criterion is set to:  
\( L_2 \) **norm error <** \(10^{-12}\).

**Numerical Methods Implemented:**
- 📌 **Gauss-Seidel Method** - Iterative solver using point relaxation.
- 📌 **Jacobi Method** - Basic iterative solver updating all points simultaneously.
- 📌 **SOR (Successive Over-Relaxation)** - Accelerated Gauss-Seidel with relaxation factor ($\omega = 1.5$).
- 📌 **Line SOR (LSOR)** - Solves lines implicitly for better stability.
- 📌 **Fully Implicit Method** - Direct solver using matrix inversion.

---

## 📊 Results & Analysis
- **Accuracy**: Second-order discretization achieves **order of accuracy ~2**.
- **Runtime**: 
  - 🚀 **SOR with ($\omega = 1.5$)** is the fastest among **iterative methods**.
  - ⚡ **Fully Implicit Method** is the most efficient for **large-scale problems**.

**Comparative Runtime Analysis:**
| Method | Speed ⏳ | Accuracy 🎯 |
|--------|--------|-----------|
| Gauss-Seidel | Moderate | High |
| Jacobi | Slow | High |
| SOR (ω=1.5) | Fastest (Iterative) | High |
| Line SOR | Faster than Gauss-Seidel | High |
| Fully Implicit | **Fastest Overall** | **Very High** |

---

## 🚀 How to Run
1️⃣ Clone the repository:
```bash
  git clone https://github.com/yourusername/Numerical-Laplace-Solver.git
  cd Numerical-Laplace-Solver
```
2️⃣ Install dependencies:
```bash
  pip install -r requirements.txt
```
3️⃣ Open the **Jupyter Notebook** and run the cells:
```bash
  jupyter notebook code.ipynb
```

---

## 🔮 Future Improvements
🔹 Parallel computing for large-scale problems.  
🔹 Adaptive mesh refinement for improved accuracy.  

---

## 📜 License
This project is licensed under the **MIT License**. See the `LICENSE` file for details. ✅

---

## 🙌 Contributions
Feel free to **fork** this repository, create **issues**, and submit **pull requests**! 🚀🎯
