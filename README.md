# NUMERA

A desktop scientific and analytical calculator built with Python. Designed for students and data analysts, the application integrates advanced mathematical functions, statistical analysis, and interactive graphing into a single workspace with a custom dark theme.

## Features

### 1. Scientific & Advanced Modes
- **Basic Math:** Evaluates expressions, parentheses, powers, roots, and factorials securely.
- **Trigonometry & Logs:** Supports trigonometric functions and logarithms with custom bases, including Degree (DEG) and Radian (RAD) modes.
- **Variable Memory:** Assign values (e.g., `a = 5`) for reuse in subsequent calculations.
- **Equation Solver:** Features an inline step-by-step menu to solve 2-variable, quadratic, and cubic equations directly on the main screen.
- **Combinatorics:** Calculates combinations (nCr) and permutations (nPr).
- **Fraction Mode:** Toggles the "S⇔D" button to switch results between decimals and exact fractions.

### 2. Statistics Workspace
- **Dataset Input:** Accepts comma-separated or individual paired X and Y data points.
- **Live Summary:** Automatically updates to display Count, Mean, Median, and Standard Deviation.
- **Advanced Metrics:** Provides direct access to Quartiles (Q1, Q3), IQR, MAD, Variance, and Regression metrics.
- **Linear Regression:** Calculates Correlation (r), Slope (m), and Y-Intercept (b) for matched datasets.

### 3. Interactive Graphing (Matplotlib)
- **Embedded Canvas:** Renders graphs directly within the application interface.
- **Navigation:** Supports mouse-wheel zooming and click-and-drag panning.
- **Graph Types:**
  - **Linear Regression:** Scatter plot with a line of best fit.
  - **Histogram:** Displays the frequency distribution of the dataset.
  - **Normal Curve:** Plots a bell curve based on the data.
  - **Poisson Distribution:** Displays the probability mass function for count data.
- **Summary Panel:** Displays relevant equations, R² values, and statistical parameters below the graph.

## Tech Stack & Architecture

The project uses a modular architecture to separate the UI from the math engine:

- **`customtkinter`**: Modern, rounded UI widgets with a custom dark color palette.
- **`sympy`**: Symbolic mathematics for exact equation solving.
- **`matplotlib` & `numpy`**: For plotting interactive graphs and handling arrays.
- **`ast` & `math`**: Built-in Python libraries for safe parsing and basic math.

### File Structure

```text
Advanced_Calculator/
├── code/                  # All Python source files
│   ├── main.py            # Entry point to run the app
│   ├── theme.py           # Colors, fonts, and styling constants
│   ├── calculations.py    # The math engine (no GUI code)
│   ├── interface.py       # Main window, keyboard bindings, and controller
│   ├── keypads.py         # Layouts for Scientific and Advanced buttons
│   ├── statistics_mode.py # UI and logic for the Statistics workspace
│   ├── graph.py           # Matplotlib embedding and interactive controls
│   └── requirements.txt   # Python dependencies
├── docs/                  # Project documentation and presentation
│   ├── Assignment.pdf     # Original assignment brief
│   └── Calculator.pptx    # Final presentation slides
├── .gitignore             # Files to exclude from Git tracking
├── LICENSE                # Open-source license
└── README.md              # You are here
```

## How to Run
1. Clone the repository and open the code folder:

```
git clone https://github.com/Aditi020/Scientific_and_Advanced_Calculator.git
cd Scientific_and_Advanced_Calculator/code
```

2. Create and activate a virtual environment (recommended):

```
python -m venv venv
```

Windows:

```
venv\Scripts\activate
```

macOS/Linux:

```
source venv/bin/activate
```

3. Install the dependencies:

```
pip install -r requirements.txt
```

4. Run the application:

```
python main.py
```

