# NFT Transaction Fee：Analysis of the Impact of the London Upgrade on the stability of Gas Fee
## Project information
- **Author**: Yiyang Zhang, Computation and Design with tracks in Digital Media, Class of 2025, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: SRS program instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: Thanks to Professor Luyao Zhang for guiding my project. Thanks to the SciEcon editorial team including Xintong Wu, Wanlin Deng, Xinyu Tian, Zesen Zhuang, Prof. Luyao Zhang. Thanks to Yu Wang for giving me emotional support and encouragement.
- **Project Summary**: 
  - [Summarize the Background/Motivation]
  - [Research Questions]
  - [Application Scenario (Data Source)]
  - [Methodology]
  - [Results]
  - [Intellectual Merits and Practical impacts of your project.]

## Table of Contents
- data
- code
- spotlight



## Data
- Data Source: https://etherscan.io/chart/gasprice
- Meta Data Infomation:

| Data Files | Data Type | Data Content |
| ----- | ----- | ----- | 
|  [GasPrice.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Queried_Data/GasPrice.csv) | Queried | the daily average gas price used of the Ethereum network | 
| [GP.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Queried_Data/GP.csv) |  Processed | arranged average gas price used of the Ethereum network |
| [GPR.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Processed_Data/GPR.csv) | Processed |the standard deviation of the daily average gas price used of the Ethereum network |
| [Regression_Train.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Processed_Data/Regression_Train.csv) | Processed | Training data for regression | 
| [Regression_Test.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Processed_Data/Regression_Test.csv) | Processed | Testing data for regression | 

- Data Dictionary
- 
| File Name | Variable Name | Description | Frecuency | Unit | Type |
| ----- | ----- | ----- | ----- | ----- | ----- |
| [GasPrice.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Queried_Data/GasPrice.csv)  | Date(UTC) | date of data collected | daily | day | datetime |
|  | UnixTimeStamp | UnixTimeStamp of data collected | daily | None | Timestamp |
|  | Value (Wei) | the daily average gas price used of the Ethereum network | daily | Wei | int |
| [GP.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Queried_Data/GP.csv) | Date(UTC) | date of data collected | daily | day | datetime |
|  | UnixTimeStamp | UnixTimeStamp of data collected | daily | None | Timestamp |
|  | Value (Wei) | the daily average gas price used of the Ethereum network | daily | Wei | int |
| [GPR.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Processed_Data/GPR.csv)  |  Date | date of data collected | daily | day | datetime |
|  | Rate | the standard deviation of the daily average gas price used of the Ethereum network | daily | None | float |
| [Regression_Train.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Processed_Data/Regression_Train.csv) | theta | the daily average gas price used of the Ethereum network | daily | None | float |
|  | theta_past_ma10 | average standard deviation of past 10 days | daily | None | float |
| [Regression_Test.csv](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/data/Processed_Data/Regression_Test.csv) | theta | the daily average gas price used of the Ethereum network | daily | None | float |
|  | theta_past_ma10 | average standard deviation of past 10 days | daily | None | float |

## Code
- Prediction Code Source: https://github.com/Rising-Stars-by-Sunshine/stats201-tutorial-prediction

- Causal Event Certification Code Source: https://numpy.org/doc/stable/reference/generated/numpy.polyfit.html

| Prediction | Causal Inference |
| ----- | ----- | 
|  [Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/code/Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb)  | [Query_Data.ipynb](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/code/Query_Data.ipynb) |
| [Analyze_Data_Machine_Learning_for_Predicting_Market_Congestion_ipynb.ipynb](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/code/Analyze_Data_Machine_Learning_for_Predicting_Market_Congestion_ipynb.ipynb) | [Process_Data.ipynb](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/code/Process_Data.ipynb) |
|  | [Analyze_Data.ipynb](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/code/Analyze_Data.ipynb) | 

## Spotlight
- Prediction
  
![image](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/spotlight/figures/Linear%20Regression.png)
### Figure No.1. Linear regression prediction histogram of the stability of Gas Fee
The predicted and actual values have a low degree of fitting, and this event has remarkable impact on life expectancy.

- Causal Inference Research Design

![image](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/spotlight/figures/Causal%20Inference%20Research%20Design.png)
### Figure No.2. Causal Inference Research Design


- Causal Inference

![image](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/spotlight/figures/Casual%20Inference.png)
### Figure No.3. Result


## More about the Author

![image](https://github.com/YiyangZhangyz738/Gas-Price/blob/main/headshot.jpeg）
- Yiyang Zhang is from the class of 2025, majoring in Computation and Design with tracks in Digital Media at Duke Kunshan University. She is designated a Summer Research Scholar for the summer of 2023 and awarded by the SRS program. Her research interest is NFT transaction, digital design, and media interaction. 

## References

### Data Source
- https://etherscan.io/chart/gasprice
### Code Source
- https://github.com/Rising-Stars-by-Sunshine/stats201-portfolio
- https://github.com/sunshineluyao/design-principle-blockchain

### Articles
- Article Source Title and URL
### Literature
- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.

```
@article{levin2022bridging,
  title={Bridging level-k to nash equilibrium},
  author={Levin, Dan and Zhang, Luyao},
  journal={Review of Economics and Statistics},
  volume={104},
  number={6},
  pages={1329--1340},
  year={2022},
  publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…}
}
```

