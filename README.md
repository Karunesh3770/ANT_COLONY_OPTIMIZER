# ANT_COLONY_OPTIMIZER
This interactive Streamlit app combines **Ant Colony Optimization (ACO)** with a **Long Short-Term Memory (LSTM)** model to solve the **Traveling Salesman Problem (TSP)** for delivery route planning. It allows users to upload location data, optimize delivery paths, and visualize both the route and how ACO improves it over iterations — enhanced with LSTM-based insights (e.g., distance prediction or learning route patterns).

---

## 🚀 Features

- 📤 Upload delivery location CSV
- 🧠 ACO for route optimization
- 🔁 LSTM model for distance/path forecasting
- 🔧 User control over ACO parameters (ants, iterations, pheromone decay, alpha, beta)
- 📊 Visualize the optimized route on a 2D plot
- 🎞 Animated GIF showing ACO's learning process
- 💬 Insights into how routes evolve and converge

---

## 🧠 Models Used

### 🐜 Ant Colony Optimization (ACO)
- Meta-heuristic algorithm mimicking how ants find the shortest path using pheromone trails.
- Determines the optimal order to visit all delivery locations.

### 🔁 Long Short-Term Memory (LSTM)
- Deep learning model used to forecast:
  - Route cost trends across iterations
  - Travel distances between locations (based on historical patterns)
- Helps improve convergence stability of ACO.

---

## 📦 Tech Stack

- **Frontend**: Streamlit
- **Backend Algorithms**: Custom ACO, LSTM (via PyTorch or Keras)
- **Animation**: Matplotlib + PIL
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `pillow`, `streamlit`, `torch` or `tensorflow`

---

## 🗂 Input Format

Upload a `.csv` file with latitude and longitude columns. For example:

| dest_lat | dest_lng |
|----------|----------|
| 12.9716  | 77.5946  |
| 13.0827  | 80.2707  |

---

## 🧪 ACO Parameters

| Parameter | Description |
|----------|-------------|
| Number of Ants | Number of ants exploring paths |
| Iterations | Number of optimization cycles |
| Decay | Pheromone evaporation rate |
| Alpha | Importance of pheromone strength |
| Beta | Importance of distance (visibility) |

---

## 📊 Outputs

- 📈 **Best Delivery Route**
- 🧠 **LSTM Prediction Trends**
- 🌀 **Animated ACO Convergence**
- 🧾 **Metrics:**
  - Route order
  - Total distance
  - Path evolution

---

## ▶️ Run Locally

### 1. Install Required Packages

```bash
pip install streamlit pandas numpy matplotlib pillow torch
If you're using TensorFlow instead of PyTorch for LSTM:

bash
Copy
Edit
pip install tensorflow
2. Run the App
bash
Copy
Edit
streamlit run app.py
💡 Potential Use Cases
Courier and logistics route planning

Smart city last-mile delivery

AI-based educational simulation of swarm intelligence + neural networks

📌 To-Do
 Visualize LSTM predictions on route graphs

 Add support for vehicle capacity (VRP)

 Live integration with Google Maps or Mapbox

 Export optimized path and logs

🙌 Acknowledgments
ACO Algorithm by Marco Dorigo

LSTM architecture from [Hochreiter & Schmidhuber, 1997]

Streamlit for making rapid UI possible

PyTorch/TensorFlow for LSTM modeling

📜 License
Open source under MIT License
