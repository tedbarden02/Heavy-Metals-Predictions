# Heavy-Metals-Predictions
Our final year project on Heavy Metals Prediction in Coastal Marine Sediments Using Hybridized Machine Learning Models with Metaheuristic Optimization Algorithm

This repository contains the code and documentation for our final year project: Heavy Metals Prediction in Coastal Marine Sediments Using Hybridized Machine Learning Models with Metaheuristic Optimization Algorithm. The project predicts concentrations of heavy metals (Arsenic and Zinc) in marine sediments using standalone machine learning models (Elman Neural Network - ENN, Boosted Tree Algorithm - BTA, Relevance Vector Machine - RVM) and a hybrid model (RVM with Flower Pollination Algorithm - RVM-FPA).

## Project Overview
This project develops machine learning models to predict Arsenic (As) and Zinc (Zn) concentrations in marine sediments. We implemented three standalone models (ENN, BTA, RVM) and a hybrid RVM-FPA model, which optimizes RVM using the Flower Pollination Algorithm. The project leverages data augmentation, statistical preprocessing, and robust evaluation to support environmental monitoring and remediation strategies.

##Data
The dataset includes 161 sediment samples from the coastal area near Tangshan Harbor, China, measuring heavy metals (Cr, Cu, Zn, As, Cd, Pb, Hg, Ni), Al2O3, clay, silt, sand, mean grain size, and water depth. The data is sourced from the Dryad repository: [Distribution of heavy metals in coastal sediments under the influence of multiple factors: A case study from the south coast of an industrialized harbor city (Tangshan, China)](https://datadryad.org/stash/dataset/doi:10.5061/dryad.mkkwh7150) (August 25, 2023). 
- **Files** (in `/data/`):
  - `new Actual data.csv`: Original dataset (161 samples, 19 columns, no nulls) from the Dryad repository.
 
Data was preprocessed with ILR transformation for compositional data and tested for stationarity (ADF, PP tests) and normality (Jarque-Bera). If data is not included in the repository, download it from the Dryad link above.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/tedbarden02/Heavy-Metals-Predictions.git
   cd Heavy-Metals-Predictions
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Install Jupyter (if needed):
   ```bash
   pip install jupyter
   ```

## Usage
1. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Open `Heavy metals.ipynb` and run cells to:
   - Load and preprocess data (`new Actual data.csv`).
   - Generate synthetic data (CTGAN, GaussianCopula).
   - Train models (ENN, BTA, RVM, RVM-FPA).
   - Evaluate models and visualize results.
  
## Models and Methodology
- **Preprocessing**: ILR transformation for clay/silt/sand, normalization, stationarity tests (ADF, PP).
- **Models**:
  - **ENN**: Captures non-linear patterns.
  - **BTA**: Ensemble boosting for robust predictions.
  - **RVM**: Probabilistic kernel-based regression.
  - **RVM-FPA**: Hybrid model optimizing RVM with FPA for enhanced accuracy.
- **Evaluation**: 5-fold cross-validation; metrics include MAE, RMSE, NSE, MAPE, PBIAS.


## References
- Dataset: [Distribution of heavy metals in coastal sediments under the influence of multiple factors: A case study from the south coast of an industrialized harbor city (Tangshan, China)](https://datadryad.org/stash/dataset/doi:10.5061/dryad.mkkwh7150) (Dryad, August 25, 2023).

## Contributors
- Thomas Barden (ID: 10954047)
- Austin Atsu (ID: 10962018)

**Contact**: [tedbarden02@example.com]
