# NFT Marketplaces
## Project information
- **Author**: Yiyang Zhang, Computation and Design with tracks in Digital Media, Class of 2025, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: SRS program instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: Thanks to Professor Luyao Zhang for guiding my project. Thanks to the SciEcon editorial team including Xintong Wu, Wanlin Deng, Xinyu Tian, Zesen Zhuang, Prof. Luyao Zhang. Thanks to Colden Johnson and Jiayi Wang for peer review.
- **Project Summary**: 
  - [Data Source] Das, Dipanjan, Priyanka Bose, Nicola Ruaro, Christopher Kruegel, and Giovanni Vigna. 2021. “Understanding Security Issues in the NFT Ecosystem,” November. https://doi.org/10.48550/arxiv.2111.08893.
https://zenodo.org/record/6526192


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
|  [nifty url.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/nifty%20url.csv) | Processed | image url of the NFT asset on Nifty | 

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
| [foundationevent.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/foundationevent.csv) | time | the time of the NFT event on the Foundation | event | day | datetime |
|  | type | the typr of the NFT event on the Foundation | event | \ | string |
| [superrareeventtype.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/superrareeventtype.csv) | time | the time of the NFT event on the SuperRare | event | day | datetime |
|  | type | the typr of the NFT event on the SuperRare | event | \ | string |
| [Raribleventtype1.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/Raribleventtypel.csv) | time | the time of the NFT event on the Rarible | event | day | datetime |
|  | type | the typr of the NFT event on the Rarible | event | \ | string |
| [Raribleventtype2.csv](https:/Lgithub.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/Raribleventtype2.csv) | time | the time of the NFT event on the Rarible | event | day | datetime |
|  | type | the typr of the NFT event on the Rarible | event | \ | string |
| [nifty url.csv](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/data/nifty%20url.csv) | URL | the image url of the NFT asset on Nifty | asset | \ | string | 
|  | DATE | the last transaction date of the NFT asset on Nifty | asset | day | datetime | 
|  | URLTYPE | the website type according to the image url of the NFT asset on Nifty | asset | \ | string | 

## Code

| Changes in NFT asset characteristics | Privacy of NFT transaction accounts | Changes in the types of NFT events | Changes in the type of access link for NFT assets |
| ----- | ----- | ----- | ----- |
| [FoundationSizeType.ipynb](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/code/FoundationSizeType.ipynb) | [SuperrareAccount.ipynb](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/code/SuperrareAccount.ipynb) | [Foundation_Event_Type.ipynb](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/code/Foundation_Event_Type.ipynb) | [NiftyURL.ipynb](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/code/NiftyURL.ipynb) |
|  | [RaribleAccount.ipynb](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/code/RaribleAccount.ipynb) | [SuperRare_Event_Type.ipynb](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/code/SuperRare_Event_Type.ipynb) |  |
|  |  | [RaribleAccount.ipynb](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/code/RaribleAccount.ipynb) |  |

## Spotlight
  
### Changes in NFT asset characteristics
#### MIME Type Distribution
- Figure No.1. MIME Type Distribution on Foundation

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/FundationSizeType/MIME%20Type%20Distribution.png)
-

#### Characteristics Variation of Video
- Figure No.2. Average Width Variation of Video.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/FundationSizeType/Average%20Width%20Variation%20of%20Video.png)

- Figure No.3. Average Height Variation of Video.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/FundationSizeType/Average%20Height%20Variation%20of%20Video.png)

- Figure No.4. Average Duration Variation of Video.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/FundationSizeType/Average%20Duration%20Variation%20of%20Video.png)
-

#### Size Variation of Image
- Figure No.5. Average Width Variation of Image.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/FundationSizeType/Average%20Width%20Variation%20of%20Image.png)

- Figure No.6. Average Height Variation of Image.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/FundationSizeType/Average%20Height%20Variation%20of%20Image.png)

- Figure No.7. Average Height Variation of Image (Log Transformed).png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/FundationSizeType/Average%20Height%20Variation%20of%20Image%20(Log%20Transformed).png)
-

### Privacy of NFT transaction accounts
#### Rarible
- Figure No.8. Account Accessibility of Transactions on Rarible.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/Account%20Accessibility/Account%20Accessibility%20of%20Transactions%20on%20Rarible.png)
-

#### Superrare
- Figure No.9. Account Accessibility of Transactions on Superrare.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/Account%20Accessibility/Account%20Accessibility%20of%20Transactions%20on%20Superrare.png)
-

### Changes in the types of NFT events
#### Foundation
- Figure No.10. Foundation Event Type.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/EventTypeDistribution/Foundation%20Event%20Type.png)
-

#### Rarible
- Figure No.11. Rarible Event Type.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/EventTypeDistribution/Rarible%20Event%20Type.png)
-

#### SuperRare
- Figure No.12. SuperRare Event Type.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/EventTypeDistribution/SuperRare%20Event%20Type.png)
-

### Changes in the type of access link for NFT assets
#### Nifty
- Figure No.13. Nifty Website Proportions.png

![image](https://github.com/SciEcon/SRS2023-NFT_Marketplaces/blob/main/spotlight/NiftyURL/Nifty%20Website%20Proportions.png)
-


## More about the Author

- Yiyang Zhang is from the class of 2025, majoring in Computation and Design with tracks in Digital Media at Duke Kunshan University. She is designated a Summer Research Scholar for the summer of 2023 and awarded by the SRS program. Her research interest is NFT transaction, digital design, and media interaction. 

## References

### Data Source
- https://zenodo.org/record/6526192
### Code Source
- https://github.com/Rising-Stars-by-Sunshine/stats201-portfolio

### Literature

```
@inproceedings{nft-study,
    author = {Dipanjan Das and Priyanka Bose and Nicola Ruaro and Christopher Kruegel and Giovanni Vigna},
    booktitle = {Proceedings of the ACM Conference on Computer and Communications Security (CCS)},
    title = {Understanding Security Issues in the NFT Ecosystem},
    year = {2022}
}
```
