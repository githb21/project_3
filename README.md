![Crypto Sneaks Logo](images/CryptoSneaks.gif)

## DApp Summary

This application is a decentralized collectible sneaker auction platform built on Ethereum

## Demo App

Click [here](https://githb21.github.io/auction_dapp) to launch the dapp

---
## Table of Contents

* [About](#About)
* [Market Analysis and Modeling](#market-analysis-and-modeling) 
* [Development Platforms](#development-platforms)
* [Digital Tokens - Non-Fungible Tokens(NFT)](#digital-tokens-non-fungible-tokens(NFT)) 
* [Initial Coin Offering (ICO)](#initial-coin-offering-(ICO)) 
* [Collaborators](#collaborators)
* [Resources](#resources)

---
## Summary

CryptoSneaks is a decentralized auction platform for caollectible sneakers, which enables a transparent, real-time bidding process for buyers who are interested in collectible sneakers. CryptoSneaks will be able to register new sneakers with their account, minting and creating a new auction for the sneaker. When the endAuction function is called, the auction will complete and the token will be transferred to the highest bidder Each collectible sneaker will be a unique ERC721 token, with its own metadata including the name, size and image URL, to be registered on the [Pinata](https://pinata.cloud/) - a decentralized InterPlanetary File System.

In order to fund the development of CryptoSneaks, an Initial Coin Offering was created. We have also used Machine Learning to analyze the sneaker resale markets data which provides valuable market intel for investors of collectible markets.

---
## ICO

### Deplopy the crowdsale
![deployICO](screen_shot/deployICO.gif)

### Purchase AUC token
![buyAUC](screen_shot/buyAUC.gif)

### Finalize sale
![finalizeSale](screen_shot/finalizeSale.gif)

You can the AUC token on Ropsten testnet Etherscan by inputting the token_address

![etherscan_AUC](screen_shot/etherscan_AUC.jpg)

In order to fund the development of CryptoSneaks, an Initial Coin Offering was created.









## Market Analysis and Modeling
Using the dataset provide by StockX we evaluated the different aspects of the sneakers resale market and develop a regression model to predict resale price identify the most relevant features of the sneakers market. 

![by_name](MarketAnalysis/media/by_name.png)


![by_retail_price](MarketAnalysis/media/by_retail_price.png)


![by_shoe_size](MarketAnalysis/media/by_shoe_size.png)


![by_region](MarketAnalysis/media/by_region.png)


![avg_sale_price](MarketAnalysis/media/avg_sale_price.png)

### Parameters
```python
# Define features set
X = df.drop(['sale_price'], axis=1)

# Define target vector
y = df.sale_price

# Encoding variables
X = pd.get_dummies(X, columns=["brand", "sneaker_name", "buyer_region"])
X.head()

# Splitting into Train and Test sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state = 27)

# Create the random forest regresor instance
rf_model = RandomForestRegressor(n_estimators=500,random_state=27)
```

### Results
```python
R²: 0.98
Mean Absolute Error: 14.49
Median Absolute Error: 7.10
Accuracy: 97.14%
```
![feature_importances](MarketAnalysis/media/feature_importance.png)

---
## Development Platforms
![ethereum](images/ethereum.png)
![infura](images/infura.png)
![jupyterlab](images/jupyterlab.png)
![metamask](images/metamask.png)
![pinata](images/pinata.png)
![python](images/python.jpeg)
![remix](images/remix.png)
![solity](images/solidity.png)

---
## Blockchain Technology
## Smart Contracts

---
## Digital Tokens - Non-Fungible Tokens (NFT)

---
## Initial Coin Offering (ICO)

---



---
## Collaborators
- Sylvia Li
- Emmanuel Lopez 
- Etienne Alcaraz

---
## Resources
- [Random Forest Regression](MarketAnalysis/notebooks/Random_Forest_Regression.ipynb)
- [Sneakers Analysis](MarketAnalysis/notebooks/Sneakers_Data_Analysis.ipynb)
- [Auction Smart Contract]()
- [ICO Smart Contract]()
- [StockX Data Contest](https://stockx.com/news/the-2019-data-contest/)

