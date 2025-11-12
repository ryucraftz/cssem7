# LP-3 Laboratory Practice - How to Run

This guide provides instructions for running all projects in the LP-3 directory.

---

## 📁 Directory Structure

```
LP-3/
├── BT/                 # Blockchain Technology (Solidity Smart Contracts)
├── DAA Python/         # Design and Analysis of Algorithms (Python)
├── ML/                 # Machine Learning (Jupyter Notebooks)
└── Dataset/            # Datasets for ML projects
```

---

## 🔗 Blockchain Technology (BT)

### Prerequisites
- Install **Remix IDE** (Online): https://remix.ethereum.org/
- Or install **Ganache** + **Truffle** for local development

### How to Run Solidity Files

#### Method 1: Using Remix IDE (Recommended for Beginners)
1. Open https://remix.ethereum.org/ in your browser
2. Create a new file in Remix with `.sol` extension
3. Copy the code from any of the following files:
   - `3_Bank_account.sol` - Bank account smart contract
   - `3.1_Product_Inventory.sol` - Product inventory management
   - `4_Student.sol` - Student record management
   - `4.1_Employee.sol` - Employee record management
4. Paste the code into Remix
5. Select appropriate Solidity compiler version (check pragma statement in file)
6. Click "Compile" button
7. Go to "Deploy & Run Transactions" tab
8. Select "JavaScript VM" environment
9. Click "Deploy"
10. Interact with deployed contract functions

#### Method 2: Using Ganache + Truffle (Local Development)
```cmd
npm install -g truffle
npm install -g ganache-cli

REM Start Ganache
ganache-cli

REM In new terminal, compile contracts
truffle compile

REM Deploy contracts
truffle migrate

REM Interact with contracts
truffle console
```

---

## 🐍 Design and Analysis of Algorithms (DAA Python)

### Prerequisites
- Python 3.8 or higher
- Install required packages:
```cmd
pip install numpy matplotlib
```

### How to Run Python Files

#### 1. Fibonacci Numbers
```cmd
python "DAA Python/1_fibonacci_numbers.py"
```
**Description:** Implements recursive and iterative Fibonacci calculation with time complexity analysis.

#### 2. Huffman Encoding
```cmd
python "DAA Python/2_huffman_encoding.py"
```
**Description:** Implements Huffman encoding algorithm for data compression.

#### 3. Fractional Knapsack
```cmd
python "DAA Python/3_fractional_knapsack.py"
```
**Description:** Solves fractional knapsack problem using greedy approach.

#### 4. 0-1 Knapsack
```cmd
python "DAA Python/4_0_1_knapsack.py"
```
**Description:** Solves 0-1 knapsack problem using dynamic programming.

#### 5. N-Queens Problem
```cmd
python "DAA Python/5_n_queens.py"
```
**Description:** Solves N-Queens problem using backtracking algorithm.

#### 6. Quick Sort
```cmd
python "DAA Python/6_QuickSort.py"
```
**Description:** Implements Quick Sort with deterministic and randomized pivot selection.

---

## 🤖 Machine Learning (ML)

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Install required packages:
```cmd
pip install -r requirements.txt
```

Or install individually:
```cmd
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow keras jupyter opendatasets
```

### How to Run Jupyter Notebooks

#### Start Jupyter Notebook
```cmd
cd LP-3\ML
jupyter notebook
```

#### Or Start JupyterLab
```cmd
cd LP-3\ML
jupyter lab
```

### Available Notebooks

#### 1. Uber Price Detection
```cmd
jupyter notebook "1. Uber Price Detection.ipynb"
```
**Description:** Predicts uber ride prices using linear regression.  
**Dataset:** `Dataset/1-uber.csv`

#### 2. Email Spam Classification
```cmd
jupyter notebook "2. Email Spam Classification.ipynb"
```
**Description:** Classifies emails as spam or ham using machine learning.  
**Dataset:** `Dataset/2-email.csv`

#### 3. Neural Network
```cmd
jupyter notebook "3. Neural_Network.ipynb"
```
**Description:** Implements artificial neural network for classification.  
**Dataset:** `Dataset/3-Churn_Modelling.csv`

#### 4. Gradient Descent
```cmd
jupyter notebook "4. GradientDescent.ipynb"
```
**Description:** Demonstrates gradient descent optimization algorithm.  
**Dataset:** Built-in dataset

#### 5. KNN on Diabetes
```cmd
jupyter notebook "5. KNN_on_Diabetes.ipynb"
```
**Description:** Applies K-Nearest Neighbors algorithm on diabetes dataset.  
**Dataset:** `Dataset/4-diabetes.csv`

#### 6. KMeans on Sales
```cmd
jupyter notebook "6. KMeans_on_sales.ipynb"
```
**Description:** Performs customer segmentation using K-Means clustering.  
**Dataset:** `Dataset/5-sales_data_sample.csv`

---

## 📊 Alternative: Run Notebooks in VS Code

### Prerequisites
1. Install **Python extension** in VS Code
2. Install **Jupyter extension** in VS Code

### Steps
1. Open VS Code
2. Open the LP-3 folder
3. Navigate to `ML/` directory
4. Click on any `.ipynb` file
5. Select Python kernel (top-right corner)
6. Run cells using Shift+Enter or click "Run All"

---

## 🔧 Troubleshooting

### Python Issues
- **Module not found:** Run `pip install <module_name>`
- **Python not recognized:** Add Python to system PATH
- **Jupyter not starting:** Try `python -m jupyter notebook`

### Solidity Issues
- **Compiler error:** Check pragma version and use matching compiler
- **Deployment fails:** Ensure sufficient gas limit
- **Function not visible:** Check function visibility (public/private)

### Dataset Issues
- **File not found:** Ensure you're running from correct directory
- **Dataset missing:** Check `Dataset/` folder for required CSV files
- **Encoding error:** Try adding `encoding='unicode_escape'` or `encoding='utf-8'`

---

## 📝 Notes

- All Python files can be run directly from command line
- Jupyter notebooks should be run in browser or VS Code for interactive experience
- Solidity contracts require Ethereum development environment
- Datasets are included in `Dataset/` folder for ML projects
- Some notebooks may download datasets from Kaggle (requires `opendatasets` package)

---

## 🎯 Quick Start Commands

```cmd
REM Install all Python dependencies
pip install -r requirements.txt

REM Start Jupyter for ML projects
cd LP-3\ML
jupyter notebook

REM Run any DAA Python file
cd LP-3
python "DAA Python/1_fibonacci_numbers.py"

REM Open Remix IDE for BT projects
start https://remix.ethereum.org/
```

---

## 📚 Additional Resources

- **Remix IDE Documentation:** https://remix-ide.readthedocs.io/
- **Solidity Documentation:** https://docs.soliditylang.org/
- **Python Documentation:** https://docs.python.org/3/
- **Scikit-learn Documentation:** https://scikit-learn.org/
- **TensorFlow Documentation:** https://www.tensorflow.org/

---

**Created for SPPU CSE Semester 7 - Laboratory Practice 3**
