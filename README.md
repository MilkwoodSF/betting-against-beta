# Betting Against Beta

This codebase is based on the paper: Frazzini, A. \& Pedersen, L. (2014).
*Betting Against Beta*, available online
[here](https://pages.stern.nyu.edu/~lpederse/papers/BettingAgainstBeta.pdf).  It seeks to implement the work discussed in the paper.

## Data
- `Data` folder stores the fetched data and `Data.py`.

- `Data.py` consists of 2 parts: save tickers, get data. Tickers are processed through website information, data are fetched using 'pandas-datareader'.


## Implementation
- `main.py` contains all the functions.

- `figure.py` is for drawing plots.


## Results

This strategy was back-tested on SP500 stocks and TSX (Toronto Stock Exchange) stocks and compared with two other similar factors presented in the Fama French 3-factor model: one is the SMB (small minus big), the other is the HML (high minus low).  SMB and HML data were obtained from [Ken French’s data library](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html)

![US](Output/US.png)

*Cumulative Return with $1 invested in the beginning in the SP500 (shown as US) equity market (in comparison with the SMB and HML factors)*

![CAN](Output/CAN.png)

*Cumulative Return with $1 invested in the beginning in the TSX (shown as CAN) equity market (in comparison with the SMB and HML factors)*


## Evaluation
- Portfolio construction
![US Equal W](Output/SP500EqualW.png)

- Hedging
![US Hedge](Output/SP500Hedge.png)

- Trading cost: Looking at the actual weights the strategy puts on stocks with different market cap, we find out small-cap stocks are overweighted, causing significant implementation issues because the smallest stocks usually have limited capacity and are expensive to trade.


## Further Development
- Set some threshold regarding the market capitalization when assigning weights

- Mitigate risk using diversification

- Explore the relationship between the strategy and market states, and refine it by incorporating the judgment of market trends into the
strategy



## Reference
1. Andrea Frazzini and Lasse Heje Pedersen. Betting against beta. Journal of Financial Economics, 111(1):1–25, 2014
