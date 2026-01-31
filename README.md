<h1 align="center">Perceptron Algorithm: Binary Classification</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" />
</p>

<p align="center">
  A clean implementation of the <b>Perceptron Learning Algorithm</b> for binary classification tasks. This project demonstrates the iterative weight adjustment process to separate data points into distinct classes (2 and 4) using a threshold-based decision function and structured Excel datasets.
</p>

<p align="center">
  <a href="#technical-architecture">
    <img src="https://img.shields.io/badge/Architecture-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#project-structure">
    <img src="https://img.shields.io/badge/Structure-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#mathematical-foundations">
    <img src="https://img.shields.io/badge/Math-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#technical-specifications">
    <img src="https://img.shields.io/badge/Specs-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#deployment--installation">
    <img src="https://img.shields.io/badge/Deploy-222222?style=flat" />
  </a>
</p>

---
<br>

<h2 align="center">Technical Architecture</h2>

The implementation follows a modular linear classification pipeline designed for binary prediction. It manages both training and inference with custom logic:

1.  **Data Ingestion:** Utilizes `pandas` to read structured multi-sheet Excel files, separating Training (`TRAINData`) and Test (`TESTData`) environments.
2.  **Perceptron Training:** Implements the stochastic weight update rule. It iterates through the dataset for 1000 epochs, adjusting the hyperplane at each misclassification.
3.  **Threshold Activation:** Employs a zero-threshold activation function to categorize inputs into binary labels (Class 2 / Class 4).
4.  **Result Serialization:** Includes a feature to save predicted test results back into an formatted Excel output for further analysis.

---
<br>

<h2 align="center">Project Structure</h2>

```
Perceptron-Binary-Classifier/
├── LICENSE                                   # MIT License
├── README.md                                 # Project documentation
├── .gitattributes                            # Git configuration
├── DataForPerceptron.xlsx                    # Raw dataset (TRAIN/TEST sheets)
├── Project Report.pdf                        # Technical research report
│
└── Implementation/
    └── PerceptronAlgorithm.py                # Core algorithm and execution script
```

---
<br>

<h2 align="center">Mathematical Foundations</h2>

### 1. Linear Combination (Summation)
The input features are multiplied by their respective weights and added to the bias term.
```text
z = Σ (wᵢ * xᵢ) + b
```

### 2. Step Activation Function
The decision rule that classifies the output based on the value of `z`.
```text
f(z) = { 2  if z < 0
       { 4  if z ≥ 0
```

### 3. Weight Update Rule
The perceptron learning rule used to adjust weights when a misclassification occurs.
```text
w := w + α * (y_actual - y_pred) * x
b := b + α * (y_actual - y_pred)
```

---
<br>

<h2 align="center">Technical Specifications</h2>

<table align="center">
  <tr>
    <th align="center">Component</th>
    <th align="center">Specification Details</th>
  </tr>
  <tr>
    <td align="center"><b>Algorithm</b></td>
    <td align="center">Perceptron Learning Rule</td>
  </tr>
  <tr>
    <td align="center"><b>Classification Type</b></td>
    <td align="center">Binary Category (2 vs 4)</td>
  </tr>
  <tr>
    <td align="center"><b>Learning Rate (α)</b></td>
    <td align="center">0.1 (Constant)</td>
  </tr>
  <tr>
    <td align="center"><b>Max Epochs</b></td>
    <td align="center">1000 Iterations</td>
  </tr>
  <tr>
    <td align="center"><b>Input Format</b></td>
    <td align="center">Excel (.xlsx) with Feature Matrix</td>
  </tr>
  <tr>
    <td align="center"><b>Weight Initialization</b></td>
    <td align="center">Zero Initialized Weights & Bias</td>
  </tr>
</table>

---
<br>

<h2 align="center">Deployment & Installation</h2>

### Repository Acquisition
To setup the environment locally, execute:

```bash
git clone https://github.com/Zer0-Bug/Perceptron-Binary-Classifier.git
```
```bash
cd Perceptron-Binary-Classifier
```

### Environment Preparation
The project requires the following numerical and data manipulation libraries:

```bash
# Optional: Setup virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install essential dependencies
pip install numpy pandas openpyxl
```

### Running the Classifier
Execute the primary script to train the model and generate predictions:

```bash
python PerceptronAlgorithm.py
```

---
<br>

<h2 align="center">Contribution</h2>

Contributions are always appreciated. Open-source projects grow through collaboration, and any improvement—whether a bug fix, new feature, documentation update, or suggestion—is valuable.

To contribute, please follow the steps below:

1. Fork the repository.
2. Create a new branch for your change:  
   `git checkout -b feature/your-feature-name`
3. Commit your changes with a clear and descriptive message:  
   `git commit -m "Add: brief description of the change"`
4. Push your branch to your fork:  
   `git push origin feature/your-feature-name`
5. Open a Pull Request describing the changes made.
<br>
All contributions are reviewed before being merged. Please ensure that your changes follow the existing code style and include relevant documentation or tests where applicable.

---
<br>
<h2 align="center">References</h2>

1. **Frank Rosenblatt (1958)** - [The Perceptron: A Probabilistic Model for Information Storage and Organization](https://doi.org/10.1037/h0042519). *Psychological Review*.  
2. **Hastie et al. (2009)** - [The Elements of Statistical Learning](https://web.stanford.edu/~hastie/ElemStatLearn/). *Springer New York*.  
3. **Goodfellow, I., Bengio, Y., & Courville, A. (2016)** - [Deep Learning, MIT Press](https://www.deeplearningbook.org/).  

---
<br>
<p align="center">
  <a href="mailto:777eerol.exe@gmail.com">
    <img src="https://cdn.simpleicons.org/gmail/D14836" width="40" alt="Email">
  </a>
  <span> × </span>
  <a href="https://www.linkedin.com/in/eerolexe/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/c/ca/LinkedIn_logo_initials.png"
         width="40"
         alt="LinkedIn">
  </a>
</p>

---

<p align="center" style="margin-top:10px; letter-spacing:4px;">
  ∞
</p>
