# Baseball Analytics Models

## Overview
This project focuses on two data-driven models aimed at enhancing baseball performance using Trackman data from Chapman University's 2024 baseball season. These models are designed to provide insights into pitching strategies and player development.

## Models

### 1. Pitch Predictor
**Purpose**: Predict the next pitch type based on historical pitch data and game context.

**Key Features**:
- Uses variables such as pitch location, batter advantage, and whether the pitcher and batter are on the same side.
- Implements an LSTM-based neural network to handle sequential data.
- Outputs predicted pitch types to assist hitters in preparing for upcoming pitches.

**Input Variables**:
- Pitch sequence (previous pitch types)
- Location data (plate height and side)
- Context variables: `AdvantageCount`, `SameSide`

**Output**:
- Predicted pitch type (e.g., fastball, curveball).

### 2. Pitcher Improver
**Purpose**: Analyze pitch performance metrics to identify areas for improvement in a pitcher's repertoire.

**Key Features**:
- Evaluates pitch metrics such as velocity, spin rate, and movement.
- Uses logistic regression to determine the impact of each variable on successful pitch outcomes.
- Helps pitchers optimize their pitches based on data-driven insights.

**Input Variables**:
- Velocity, spin rate, break metrics
- Plate location
- Outcome variables (e.g., strikes, hits)

**Output**:
- Coefficients indicating which pitch metrics are most influential.

## Data
- **Source**: Trackman data from 21 home games.
- **Key Variables**: 
  - Pitch metrics (velocity, spin rate, break)
  - Context (outs, count, inning, batter/pitcher side)
  - Outcome (strike, ball, hit)

## How to Run
1. **Install Dependencies**:
   ```bash
   pip install numpy pandas scikit-learn tensorflow matplotlib seaborn
   ```

2. **Prepare Data**:
   - Ensure the dataset is clean and includes the required variables.
   - Add calculated variables like `AdvantageCount` and `SameSide`.

3. **Run Models**:
   - For the Pitch Predictor, execute the LSTM-based neural network.
   - For the Pitcher Improver, run the logistic regression model to generate coefficients.

4. **Visualize Results**:
   - Confusion matrix and feature importance plots for model evaluation.


