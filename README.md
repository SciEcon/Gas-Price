# NFT Marketplaces
## Project information
- **Author**: Yiyang Zhang, Computation and Design with tracks in Digital Media, Class of 2025, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: SRS program instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: Thanks to Professor Luyao Zhang for guiding my project. Thanks to the SciEcon editorial team including Xintong Wu, Wanlin Deng, Xinyu Tian, Zesen Zhuang, Prof. Luyao Zhang.
- **Project Summary**: 
  - [Summarize the Background/Motivation]

  - [Research Questions] 
  - [Application Scenario (Data Source)] 
  - [Methodology]

  - [Results] 

  - [Intellectual Merits and Practical impacts of your project.] 


## Table of Contents
- [Data](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/tree/main#data)
- [Code](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/tree/main#code)
- [Spotlight](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/tree/main#spotlight)
- [GitHub Page](https://github.com/SciEcon/SRS2023-NFT_Marketplaces)



## Data
- Data Source: https://zenodo.org/record/6526192
- Meta Data Infomation:

| Data Files | Data Type | Data Content |
| ----- | ----- | ----- | 
|  [foundationsizetype.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/foundationsizetype.csv) | Processed | The size, duration, file type, and last transaction time of the NFT asset on Foundation. | 
|  [superrareaccount.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/superrareaccount.csv) | Processed | Accessibility of user names and addresses for both sides of the transaction on SuperRare. | 
|  [Raribleaccount.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/Raribleaccount.csv) | Processed | Accessibility of user names and addresses for both sides of the transaction on Rarible. | 
|  [foundationevent.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/foundationevent.csv) | Processed | Classification of NFT events on the Foundation (e.g., mint, buy, sell, auction creation) and when the event occurred. | 
|  [superrareeventtype.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/superrareeventtype.csv) | Processed | Classification of NFT events on the SuperRare (e.g., mint, buy, sell, auction creation) and when the event occurred. | 
|  [Raribleventtype1.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/Raribleventtype1.csv) | Processed | Classification of NFT events on the Rarible (e.g., mint, buy, sell, auction creation) and when the event occurred. （first part)  | 
|  [Raribleventtype2.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/Raribleventtype2.csv) | Processed | Classification of NFT events on the Rarible (e.g., mint, buy, sell, auction creation) and when the event occurred. （second part)  | 


- Data Dictionary

| File Name | Variable Name | Description | Frecuency | Unit | Type |
| ----- | ----- | ----- | ----- | ----- | ----- |
| [ foundationsizetype.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/foundationsizetype.csv) | width | the width of the NFT assets on the Foundation | daily | pixel | int |
|  | height | the height of NFT assets on Foundation | daily | pixel | int |
|  | duration | the duration of NFT assets on Foundation | daily | second | float |
|  | mimetype | the mime type of NFT assets on Foundation | daily | \ | string |
|  | date | the last transaction time of NFT assets on Foundation | daily | day | datetime |
| [ superrareaccount.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/superrareaccount.csv) | from_account_username | accessible or not for the username of the sender account of a transaction on SuperRare | transaction | \ | int |
|  | to_account_username | accessible or not for the username of the recipient account account of a transaction on SuperRare | transaction | \ | int |
|  | from_account_address | accessible or not for the address of the sender account of a transaction on SuperRare | transaction | \ | int |
|  | to_account_address | accessible or not for the address of the recipient account of a transaction on SuperRare | transaction | \ | int |
| [Raribleaccount.csv](https:/github.com/SciEcon/SRS2923-NFT_Marketplaces/b1ob/main/data/Raribleaccount.csv) | from_account_username | accessible or not for the username of the sender account of a transaction on Rarible | transaction | \ | int |
|  | to_account_username | accessible or not for the username of the recipient account account of a transaction on Rarible | transaction | \ | int |
|  | from_account_address | accessible or not for the address of the sender account of a transaction on Rarible | transaction | \ | int |
|  | to_account_address | accessible or not for the address of the recipient account of a transaction on Rarible | transaction | \ | int |
| [foundationevent.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/foundationevent.csv) | time | the time of the NFT event on the Foundation | event | \ | datetime |
|  | type | the typr of the NFT event on the Foundation | event | \ | string |
| [superrareeventtype.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/superrareeventtype.csv) | time | the time of the NFT event on the SuperRare | event | \ | datetime |
|  | type | the typr of the NFT event on the SuperRare | event | \ | string |
| [Raribleventtype1.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/Raribleventtypel.csv) | time | the time of the NFT event on the Rarible | event | \ | datetime |
|  | type | the typr of the NFT event on the Rarible | event | \ | string |
| [Raribleventtype2.csv](https:/Lgithub.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/Raribleventtype2.csv) | time | the time of the NFT event on the Rarible | event | \ | datetime |
|  | type | the typr of the NFT event on the Rarible | event | \ | string |

## Code
- Prediction Code Source: https://github.com/Rising-Stars-by-Sunshine/stats201-tutorial-prediction

- Causal Event Certification Code Source: https://numpy.org/doc/stable/reference/generated/numpy.polyfit.html

| Prediction | Causal Inference |
| ----- | ----- | 
|  [Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb](https://github.com/SciEcon/Gas-Price/blob/main/code/Process_Data_Prepare_X_and_Y_for_Classification_and_Regressions.ipynb)  | [Query_Data.ipynb](https://github.com/SciEcon/Gas-Price/blob/main/code/Query_Data.ipynb) |
| [Analyze_Data_Machine_Learning_for_Predicting_Market_Congestion_ipynb.ipynb](https://github.com/SciEcon/Gas-Price/blob/main/code/Analyze_Data_Machine_Learning_for_Predicting_Market_Congestion_ipynb.ipynb) | [Process_Data.ipynb](https://github.com/SciEcon/Gas-Price/blob/main/code/Process_Data.ipynb) |
|  | [Analyze_Data.ipynb](https://github.com/SciEcon/Gas-Price/blob/main/code/Analyze_Data.ipynb) | 

## Spotlight
  
![image](https://github.com/SciEcon/Gas-Price/blob/main/spotlight/figures/Linear%20Regression.png)
### Figure No.1. Linear regression prediction histogram of the stability of Gas Fee

![image](https://github.com/SciEcon/Gas-Price/blob/main/spotlight/figures/Causal%20Inference%20Research%20Design.png)
### Figure No.2. Causal Inference Research Design

![image](https://github.com/SciEcon/Gas-Price/blob/main/spotlight/figures/Casual%20Inference.png)
### Figure No.3. Result

## More about the Author

![image](https://github.com/SciEcon/Gas-Price/blob/main/headshot.jpeg)
- Yiyang Zhang is from the class of 2025, majoring in Computation and Design with tracks in Digital Media at Duke Kunshan University. She is designated a Summer Research Scholar for the summer of 2023 and awarded by the SRS program. Her research interest is NFT transaction, digital design, and media interaction. 

## References

### Data Source
- 
### Code Source
- https://github.com/Rising-Stars-by-Sunshine/stats201-portfolio
- https://github.com/sunshineluyao/design-principle-blockchain

### Literature
- 
