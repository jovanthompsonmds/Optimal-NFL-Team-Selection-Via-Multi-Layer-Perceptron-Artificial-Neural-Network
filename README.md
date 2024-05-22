# Optimal NFL Team Selection Via Multi-Layer Perceptron Artificial Neural Network

## Overview
This project aims to select optimal NFL team players from a pool of active and retired players using a Multi-Layer Perceptron (MLP) Artificial Neural Network. The players are evaluated across various performance metrics and categorized into offense, special teams, and defense to form an ideal football team. The model utilizes player statistics and performance data to identify top-performing players for each position.

## Features
- **Player Pools:** Selection from 200 active and 200 retired players.
- **Performance Metrics:** Analysis based on passing, rushing, receiving, punting, kick returns, tackles, sacks, and forced fumbles.
- **MLP Architecture:** Neural network with three hidden layers for regression tasks.
- **Data Preprocessing:** Standard scaling, one-hot encoding, and data aggregation.
- **Team Optimization:** Identification of top players based on predicted performance scores and predefined thresholds.

## Project Workflow
1. **Data Loading:** Load player and game data from CSV files.
2. **Data Preprocessing:** Merge and clean datasets, engineer features, and prepare data for modeling.
3. **Model Training:** Train MLP models for each performance category.
4. **Threshold Calculation:** Classify players into optimal or non-optimal based on performance percentiles.
5. **Optimal Team Selection:** Identify top players for offense, special teams, and defense.
6. **Evaluation:** Analyze model metrics (MAE, MSE, validation loss) and validate selections.

## Files

**Main Folder:** `NFL Players Dataset`
- `players.csv`: Contains player IDs, names, positions, and dates of birth.
- `plays.csv`: Includes play IDs, game IDs, and play-level statistics.
- `games.csv`: Records game dates and IDs.
- `passer.csv`: Passing statistics for players.
- `rusher.csv`: Rushing statistics for players.
- `receiver.csv`: Receiving statistics for players.
- `kicks.csv`: Kicking statistics for special teams.
- `kickReturns.csv`: Kick return statistics for special teams.
- `tackles.csv`: Tackling statistics for defensive players.
- `sacks.csv`: Sacks statistics for defensive players.
- `fumblForced.csv`: Forced fumble statistics for defensive players.
-  These files are too large to be included here but can be downloaded at: https://www.kaggle.com/datasets/toddsteussie/nfl-play-statistics-dataset-2004-to-present/data

**Code Notebook:**
- `Optimal NFL Team Selection Via Multi-Layer Perceptron Artificial Neural Network.ipynb`: Jupyter Notebook containing all code for data processing, model training, and analysis.

## Installation and Setup
1. Clone the repository:
   git clone https://github.com/jovanthompsonmds/Optimal-NFL-Team-Selection-Via-Multi-Layer-Perceptron-Artificial-Neural-Network.git   
2. Navigate to the project directory:   
   cd repo-name
3. Install required Python packages:   
   pip install -r requirements.txt
   
## Usage
1. Open the Jupyter Notebook:   
   jupyter notebook "Optimal NFL Team Selection Via Multi-Layer Perceptron Artificial Neural Network.ipynb"   
2. Run each cell sequentially to execute data preprocessing, model training, and team selection.
3. Review the outputs to analyze optimal team selections and performance metrics.

## Model Architecture
The MLP model includes:
- **Input Layer:** Matches the number of features in each dataset.
- **Hidden Layers:**
  - Layer 1: 256 neurons, ReLU activation
  - Layer 2: 128 neurons, ReLU activation
  - Layer 3: 64 neurons, ReLU activation
- **Output Layer:** Single neuron for regression tasks.

## Insights
The MLP models successfully identified optimal players for each category. Example selections:
- Active Passing: Jameis Winston, Dak Prescott, and Philip Rivers are classified as optimal passers based on their performance scores.
- Active Rushing: Raheem Mostert, Jamaal Charles, Alvin Kamara, and Joe Williams are classified as optimal rushers.
- Active Receiving: Sean McGrath, Chris Thompson, Eric Wallace, and Jesper Horsted are classified as optimal receivers.

## Contributing
Contributions are welcome! If you'd like to improve the project, add features, or provide feedback, feel free to open an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Author
Developed by Jovan Thompson as part of a data science portfolio project.
