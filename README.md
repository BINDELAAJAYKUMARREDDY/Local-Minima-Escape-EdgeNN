# Local-Minima-Escape-EdgeNN

**Comparative Analysis of Optimization Algorithms**  
**Local Minima Escape and Convergence Dynamics in Resource-Constrained Simple Neural Networks**

**AJAY KUMAR REDDY BINDELA**  
Faculty of Engineering  
Blekinge Institute of Technology, Karlskrona, Sweden  
**October 2025**

A rigorous empirical study comparing five gradient-based optimizers (SGD, SGD with Momentum, Adam, RMSprop, Adagrad) on **four benchmark datasets** — with a novel focus on **local minima escape behavior**, convergence speed, generalization, and **edge deployment suitability**.

![Key Results](optimizer_comparison_results.png)

---

### Key Findings
- **Best optimizer for edge devices**: **Adam** — highest **Escape-Time Ratio**, excellent accuracy, and strong recovery from poor local minima  
- **Fastest training**: **SGD** (~105 seconds average)  
- **Best escape success rate**: Adam (76%)  
- **Lowest generalization gap**: Adagrad (4.37%)  
- All optimizers achieve **<150 ms inference time** — suitable for real-time edge inference  
- **20–30% energy savings** achievable through optimizer selection  

**Final Recommendation**:  
**Adam** is the optimal choice for edge-deployed neural networks requiring robustness and high accuracy.

---

### Datasets (Automatically Downloaded)
All datasets are **downloaded and preprocessed automatically** when you run the code:

| Dataset    | Source                    | Size       | Type           | Downloaded By               |
|------------|---------------------------|------------|----------------|-----------------------------|
| MNIST      | `torchvision.datasets.MNIST` | 70,000     | Images (28×28) | PyTorch torchvision         |
| CIFAR-10   | `torchvision.datasets.CIFAR10` | 60,000   | Images (32×32) | PyTorch torchvision         |
| Iris       | `sklearn.datasets.load_iris` | 150      | Tabular        | Scikit-learn                |
| Wine       | `sklearn.datasets.load_wine` | 178      | Tabular        | Scikit-learn                |

**No manual download required** — fully automated and reproducible.

---

### Repository Contents
.
├── optimizer_comparison.py              # Main experiment runner (PyTorch + sklearn)
├── results_analyzer.py                  # Auto-generates plots & report
├── optimizer_comparison_results.csv     # Full results (40 experiments)
├── experiment_log.json                  # Timestamped experiment tracking
├── optimizer_comparison_report.txt      # Ranked summary & recommendations
├── optimizer_comparison_results.png     # 6 publication-quality plots
└── README.md
text---

### How to Run (2 Minutes Setup)
```bash
# 1. Clone the repository
git clone https://github.com/yourusername/Local-Minima-Escape-EdgeNN.git
cd Local-Minima-Escape-EdgeNN

# 2. Install dependencies
pip install torch torchvision scikit-learn pandas matplotlib seaborn psutil

# 3. Run all experiments (downloads datasets automatically)
python optimizer_comparison.py

# 4. Generate updated plots and report
python results_analyzer.py
All outputs will be regenerated: CSV, PNG, TXT report.

Visualizations Included

Escape-Time Ratio by Dataset & Optimizer
Training Time Distribution
Accuracy vs Training Time Trade-off
Average Escape Success Rate
Convergence Speed (Epochs)
Generalization Gap (Train vs Test Difference)


Fully automated • 100% reproducible • Zero manual steps • Edge-focused analysis
This work demonstrates deep understanding of optimization dynamics in constrained environments — ideal for edge AI, IoT, and embedded systems.


AJAY KUMAR REDDY BINDELA
Blekinge Institute of Technology
October 2025
