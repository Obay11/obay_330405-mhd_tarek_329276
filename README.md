# obay_330405-mhd_tarek_329276
# Customer Journey Optimizer (Machine Learning Project)

## Project Objective
This project aims to analyze and optimize customer journeys using machine learning techniques.  
The main goal is to recommend the next best actions for each customer based on historical interaction data, while also identifying the most effective paths that lead to winning or losing opportunities.

Decision Tree models are used to ensure interpretability, allowing decision-makers to understand which factors influence recommendations.

---

## Implemented Steps

1. Data Loading and Cleaning
   - Load customer interaction data directly from GitHub.
   - Clean missing values, standardize text fields, and remove duplicates.
   - Construct a proper journey_id for lead and opportunity journeys.

2. Journey Construction
   - Build ordered action sequences for each customer journey.
   - Identify journey outcomes (WON, LOST, ONGOING).
   - Compute journey length and duration.

3. Top Path Analysis
   - Group journeys by Country and Solution.
   - Identify the top and shortest customer paths.

4. Next-Action Prediction (Decision Tree)
   - Build a Decision Tree model to predict the next action.
   - Evaluate performance using Top-4 Accuracy and MRR.
   - Extract and visualize Feature Importance to explain model behavior.

5. Segment-Based Recommendations
   - Recommend the top 4 actions by:
     - Country
     - Solution
     - Country + Solution
   - Combine frequency and win-rate into a scoring mechanism.

6. Dynamic Reweighting
   - Adjust action recommendations dynamically based on user interactions.
   - Prevent repetitive recommendations using a decay-based weighting mechanism.

7. Best Trip Planning
   - Use a greedy planning strategy to construct the best action sequence.
   - Maximize the probability of winning an opportunity.
   - Apply early stopping when no meaningful improvement is observed.

---

## Expected Output

- Top 4 recommended actions by:
  - Country
  - Solution
  - Country + Solution
- Dynamic updates to recommendations after user actions.
- Feature Importance table and visualization explaining decision logic.
- A suggested best customer journey with the estimated probability of winning.

---

## How to Run

1. Clone or download the repository.
2. Open the Jupyter Notebook (.ipynb) locally.
3. Run all cells from top to bottom.
4. No manual data upload is required; the dataset is loaded directly from GitHub.
