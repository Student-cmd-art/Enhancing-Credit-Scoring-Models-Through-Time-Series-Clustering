# Enhancing Credit Scoring Models Through Time-Series Clustering

## Project Overview

Experian’s credit-scoring product, Banking and Finance Delphi for New Business Generation 11 (Delphi), is widely used by UK lenders to assess consumer credit risk. It employs 1,600 aggregated attributes from multiple credit bureau datasets to predict the probability of default and score risk. However, Delphi’s attributes are based on a static snapshot of a consumer’s credit file, neglecting changes in credit behavior over time.

This project hypothesized that the evolution of consumer credit behavior is a significant factor in default prediction, a factor overlooked by Delphi’s attributes. To validate this hypothesis, the project aimed to compete with Delphi’s default prediction performance using time-series attributes from the CAIS dataset. This dataset spans 72 months and contains detailed account data for 313,513 consumers.

## Methodology

The methodology comprised two experimental stages:

1. **Experiment 1:** Clusters whole time-series data to derive cluster-based distance attributes. These attributes are then employed in a Random Forest classifier to predict default probability.

2. **Experiment 2:** Uses subsequence clustering to generate similar distance attributes, which are then used in a Logistic Regression classifier to predict default probability. For a baseline comparison, Delphi’s summary attributes are also implemented in a Logistic Regression classifier.

## Key Findings

The second experiment outperformed the Delphi model, demonstrating significant improvements in key metrics:
- **Recall:** 82.61% vs. 70.68%
- **F1-Score:** 68.17% vs. 67.98%
- **AUC:** 91.97% vs. 90.47%
- **Gini:** 83.93% vs. 80.93%

Transition analysis further validated the hypothesis by showing that a consumer’s credit journey significantly impacts their default rate. Additionally, the clustering of multivariate time-series data improved explainability by capturing variable interactions.

## Conclusion

The results underscore the importance of incorporating behavioral changes into credit-scoring models. These findings have been presented to Data Labs and team stakeholders, demonstrating the potential to enhance Delphi products by integrating insights from time-series analysis.

## Repository Contents

- **Delphi Model:** Contains the PDF notebooks and visualizations related to the baseline Delphi model.
- **Experiment 1:** Includes the PDF notebooks and visualizations for the first experiment using whole time-series clustering.
- **Experiment 2:** Contains the PDF notebooks and visualizations for the second experiment using subsequence clustering.
- **Gantt Chart:** Attached for project timeline reference.

## Note

In compliance with Experian’s data and privacy policies and with the approval of the company supervisor and compliance team, the notebooks are shared in PDF format. Certain code sections have been redacted, and the datasets are excluded. For better clarity, visualizations are provided separately.
