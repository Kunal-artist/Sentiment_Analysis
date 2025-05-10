# Employee Sentiment Analysis

This project analyses employee messages from `test(in).csv` to evaluate sentiment and engagement using a Jupyter notebook (`sentiment_analysis.ipynb`).

## Required Libraries

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `transformers`
- `torch` (with GPU support for faster processing)
- `torchvision`
- `torchaudio`

## Setup and Running the Notebook

1. **Install Anaconda**:
   - Download from [anaconda.com](https://www.anaconda.com/products/distribution).
   - Update: `conda update conda`

2. **Create Environment**:
   ```bash
   conda create -n RP_Env python=3.9
   conda activate RP_Env
   ```

3. **Install Libraries**:
   ```bash
   conda install pandas numpy matplotlib seaborn scikit-learn
   pip install transformers
   conda install pytorch torchvision torchaudio pytorch-cuda=12.8 -c pytorch -c nvidia
   ```

4. **Set Up Jupyter Kernel**:
   ```bash
   conda activate RP_Env
   python -m ipykernel install --user --name RP_Env --display-name "Python (RP_Env)"
   ```

5. **Prepare Input Data**:
   - Place `test(in).csv` in `F:\Green_Tree\Sentiment_Analysis_Project\Test_Csv\`.
   - Ensure columns: `Subject`, `body`, `date` (e.g., `YYYY-MM-DD`), `from`.

6. **Run Jupyter Notebook**:
   ```bash
   conda activate RP_Env
   jupyter notebook
   ```
   - Open `sentiment_analysis.ipynb`.
   - Select `Python (RP_Env)` kernel.
   - Run all cells (Cell > Run All).

## Outputs

- **CSV Files**:
  - `labelled_data.csv`: Messages with sentiment labels (Positive, Negative, Neutral).
  - `monthly_scores.csv`: Monthly sentiment scores per employee.
  - `employee_rankings.csv`: Top 3 positive/negative employees per month.
  - `flight_risks.csv`: Employees with 4+ negative messages in a 30-day period.
  - `model_coefficients.csv`: Linear regression model coefficients.

- **Visualizations** (in `visualization/`):
  - `sentiment_distribution.png`: Bar plot of sentiment counts.
  - `sentiment_trends.png`: Line plot of sentiment over time.
  - `employee_rankings_first_month.png`: Rankings for the first month.
  - `employee_rankings_all_months.png`: Rankings across all months.
  - `flight_risks.png`: Count of high-risk employees (if any).
  - `model_predictions.png`: Predicted vs. actual sentiment scores.

- **Console Outputs**:
  - GPU usage confirmation (e.g., `Pipeline Device: GPU`).
  - Data structure, missing values, sample labelled data, monthly scores, rankings, flight risks, and model performance (MSE, R²).
