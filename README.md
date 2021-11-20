## Project Overview 
---
## Introduction
### Our Task 

We are a new new business group at a Pennsylvania Asset Management firm tasked with leading the firms integration effort of digital assets with traditional investment porfolios. The firm is interested in exploring risk profile of digital assets and how they may be combined with traditional investment portfolios for investors with Conservative, Moderate, & Agressive risk appetite. Our task is to compare the risk profile of Digital Asset with Traditional Asset (ETFs, Mutual Funds) and recommend combination of the asset types for investor intersted in a exposure to this 'new' asset class. Then gather demographic data (such as Avg income) in the state, to consider a marketing strategy for potential new funds. 

Questions / Issues to Answer or Analyze: 

1. Analyze the risk profile of Bitcoin & Eethereum can compare with broader market as represented by SPY ETF (S&P 500).
2. Analyze historical data of the last 5 years for a traditonal Conservative, Moderate, & Agressive Porfolio for a baseline.
3. Consider combination of Digital / Crypto Assets with Traditonal ETFs or Mutual Funds & anlayze the risk / return of blended portfolios.
4. Anlayze Pennsylvania Census Data to consider marketing plan for potential blended funds (mutual funds + digital assets).

---

## Data Sources 
Data for this analysis was found in three parts: 
1. We research the make up of Traditional Pofolios (Vanguard funds) & incorprated digital / crypto assets. 
* Conservative includes: BIV, BSV, VB, VV, VXUS
* Moderate & Agressive include: BND, VB, VV, VWO, VXUS

(Data Source API saved as well as saved files)

2. Bitcoin & Eethereum choosen for name recongnition to novice digital investors, 

(Data Soruce from Google Finance for the last 5 years & saved as a CSV)
3. S&P data from Google Finance 

4. PA Market Data: Household Income Data Sourced from Kaggle pull from Census API
---

## Data Analysis

### Part 1. Analysis of the risk profiles of Bitcoin & Eethereum. 
Location: Crypto_Analysis.ipynb
1. Import  Libraries & Depencencies 
2. Read and Process Bitcoin, Eethereum, & SPY Data. Steps include: Setting the path, sorting the index, organizing close prices by date, preparing multi level index as input to Monte Carlo Anlaysis funcitons
3. Calculate & Plot Daily Returns for each (Line Chats)
![ETH DR](ETHDailyReturns.jpeg)
![BTC DR](BTCDailyReturns.jpeg)
![SPY DR](SPYDailyReturns.jpeg)
4. Prepare a Pandas Dataframes for Concatenation of Daily Returns 
5. Blend Bitcoin & Eethereum with S&P, then prepare a Box Plot of Daily Returns to compare Volatility
![Box Plot](BoxPlotDailyReturnDigital.jpeg)
6. Calculate and Plot Rolling 1y Volatility Plots using standard deviation function
![STD Plot](1yrRollingSTD.jpeg)
7. Calculate Cumulative Returns & Plot to check historical returns
![total return](Cumulativereturns.jpeg)
8. Calculate Rolling Three Month Betas & Plot (to compare the realationship between Crypto & Stock Market)
![3m rolling ETH SPY](3mRollingBetaETH&SPY.jpeg)
![3m rolling BTC&SPY](3mRollingBetaBTC&SPY.jpeg)
![3m rolling Agressive](3MRollingBetaAgressiveSPYETH&SPYBeta.jpeg)
![3m Rolling Agressive](3MRollingBetaModerate&SPY.jpeg)
9. Using a Monte Carlo Anlaysis perform a one year projection of Ethereum. Plot Daily Returns of the simulation. Then simulate behavior of a $10,000 Inbvestment & Plot Returns
![1yr DR ETH](FinalSimulatedDailyReturnsBehaviprofETHovernextyear.jpeg)
![10k 1 yr returns ETH](SimulatedReturnsETH10k.jpeg)
10. Using a Monte Carlo Anlaysis perform a one year projection of S&P. Plot Daily Returns of the simulation. Then simulate behavior of a $10,000 Inbvestment & Plot Returns.
![1yrDRSPY](SimulatedDailyReturnsofSPYnext year.jpeg)
![10k 1 yr returns SPY](10kInvestSPYSimulation.jpeg)
11. Using a Monte Carlo Anlaysis perform a one year projection of Bitcoin. Plot Daily Returns of the simulation. Then simulate behavior of a $10,000 Inbvestment & Plot Returns.
![1yr DR BTC](SimulatedDRBTCoverthenextyear.jpeg)
![10k 1 yr returns BTC](10KSimulatedReturnsBTC.jpeg)
12. Analysis of outcomes 
![Adnan results](Adnantable.jpeg)

### Part 2. Anlysis of Traditional Pofolios 
Location: project_1_all_portfolios.ipynb
1. Import  Libraries & Depencencies, Load .env variables, Set alpaca key and Secret key
2. Set weigths of a Conservative Moderate & Aggresive porfolios 
3. Run a Monte Carolo Simulation of a Conservative Porfolio: Plot Returns & Note Summary Statistics
![CON MCline](ConservMCLine.jpeg)
![Con MCDis](ConservMCdis.jpeg)
![Con MCSS](SummarystatsCONSMC.jpeg)
4. Run a Monte Carolo Simulation of a Moderate Porfolio: Plot Returns & Note Summary Statistics
![MOD MCline](MODMCLine.jpeg)
![MOD MCDis](MODMCDIS.jpeg)
![MOD MCSS](MODMCSS.jpeg)
5. Run a Monte Carolo Simulation of a Agressive Porfolio: Plot Returns & Note Summary Statistics
![Agr MCline](AgressMCLine.jpeg)
![ARG MCDis](AggresMCDis.jpeg)
![ARG MCSS](AgressMCSS.jpeg)
6. Calculate & Plot Returns of each simulation
![Con por](Aggressiveporfolioreturns.jpeg)
![MOD poris](Moderateporfolioreturns.jpeg)
![ARG por](Aggressiveporfolioreturns.jpeg)
7. Calulate Porfolio Betas & Sharpe Ratios 
8. Summarize Benchmark Statistics 
### Part 3. Anlysis of Combined Porfolios
Location: project_1_all_portfolios.ipynb
1. From the end of the analysis in PArt 1 Combine data gathered for digital assets in part 2 with the porfolios in part 1. 
* Set Porfolio weights 
* Clean data to show close prices 
2. Define assets and weights for conservative portfolio with 2% digital assets
3. Define assets and weights for moderate portfolio with 5% digital assets
4. Define assets and weights for aggressive portfolio with 10% digital assets
5. Find cumulative returns for all 3 portfolios with digital assets
![COM AG](Combinedagress.jpeg)
![COM MOD](Combinedmod.jpeg)
![COMB CON](Combinedcons.jpeg)
6. Run a Monte Carolo Simulation of a Conservative Porfolio: Plot Returns & Note Summary Statistics
![Crypto con MCline](CryptocombinedMCline.jpeg)
![Crypto con CDis](CryptocombinedMCdis.jpeg)
![Crypto con MCSS](CryptocombinedMClSS.jpeg)

7. Run a Monte Carolo Simulation of a Moderate Porfolio: Plot Returns & Note Summary Statistics
![MOD CZR MCline](MODCRMCLINE.jpeg)
![MOD CR MCDis](MODCRMCDIS.jpeg)
![MOD CR MCSS](MODCRMCDD.jpeg)
8. Run a Monte Carolo Simulation of a Agressive Porfolio: Plot Returns & Note Summary Statistics

![Agr CR MCline](CRAGRESSMCLINE.jpeg)
![ARG MCDis](CRAGRESSMCDIS.jpeg)
![ARG MCSS](CRAGRESSMCSS.jpeg)
9. Find Beta and Sharpe Ratios for all portfolios
![Mike Table](Miketable.jpeg)

### Part 4. Anlysis of PA Household Income Data
Location: PA Household Income by City.ipynb
1. Import  Libraries & Depencencies, Load .env variables, Set alpaca key and Secret key
2. Loadin in Census Data sourced from Kaggle 
3. Creat a Mapbox Plot to visulatize the Market Data. 
![Map Box PA](MapboxPA.jpeg)

--- 

## Results, Conclusions, & Implications
Based on our analysis our recomendations for integrating digital assets into traditional investment profilios are as follows: Conservative 2% digital, Moderate 5% digital, Agressive 10% digital. 

Test Results 
Results: Average yearly returns
* Conservative +6.9%
* Moderate +13.3%
* Agressive +22.1%

Results: Monte Carlo Ratio
* Conservative +3.0%
* Moderate +7.5%
* Agressive +12.2%

Results: Beta increase
* Conservative +.26
* Moderate +1.0
* Agressive +1.7

Results: Sharpe Ratio increase
* Conservative +.36
* Moderate +.55
* Agressive +.87 (1)

(Note: One unexpected result was that the sharpe ratio of an agressive digital belended portfolio was higher than moderate or conservative.
Prior to inspection of the data we expected the higher volatility of Aggressive portfolio would result in a lower Sharpe Ratio i.e risk adjusted return)

Conclusion:
After combining the digital assets with traditional investment porfolios we found that digital assets raised the average yearly returns as expected. The results of historirical returns as well as 1 year forward looking Monte Carlo simulation confimed our expectations. Based on the volitility metrics, the digital assets increased risk and volatility for conservative and moderate investors. Initial expectation is that the firm may have better traction in targeting an agressive investor, with a high risk tolerance, who is willing to take higher beta traditonal portfolio and combined with a higher allocation (10%) digital assets. Based on the Greater Philadelphia Market household income data our firm will be tageting indiviuals in the citys of Philadelphia, West Chester, Ardmore, and Wayne as they have the largest average hosuehold incomes.  The assumption being that households with higher incomes may have higher savings and as a result have a higher risk tolorence with a portion of their assets.

Implications: 
Digital assets are here to stay.  There may be an advantage for firms who are first to establish a foothold in the market by offering products suitable to the retail investor.  The modern investor is sophisticated and complex. They will not always follow the exact risk profilie identified in any one analysis.  Multiple funds with different risk and return profiles are needed to cater to the varying needs of the retail investors.  When presented with the outcomes of our analysis, some may decide that the increased risk is not worth the incremental return volatility; some however may find it a convenient vehicle to introduce crypto exposure in their investment portoflio. The higher Sharpe Ratio (albeit historical) of the Aggressive Portfolio is both an attractive marketing tool as well as an interesting investment criteria that some investors will seize upon. 
