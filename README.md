## 2020 Insider trading study
* [General info](#general-info)
* [Methodology](#methodology)
* [SW & libraries](#sw-&-libraries)
* [Data](#data)
* [Seasonality Example](#seasonality-example)
* [Mid term study Example](#mid-term-study-example)
* [Short term study Example](#short-term-study-example)

## General info
The 2020 congressional insider trading scandal was a political scandal in the United States involving allegations that several members of the United States Senate violated the   STOCK Act by selling stock at the start of COVID-19 pandemic in the United States and just before a stock market crash on February 20, 2020, using knowledge given to them at a   closed Senate meeting. The Department of Justice initiated a probe into the stock transactions on March 30, 2020. No charges were brought against anyone and all investigations   into the matter are closed now. (source: wikipedia)
 
## Methodology
Starting point of analysis will be January 24 (Closed meeting held on January 24, 2020) and any seles made by senators up to February 26 is considered for analysis (start of the crash February 26). Focus will be on 4 senators that were investigated by Justice Department and the FBI following the trading scandal.
1) Richard Burr
2) Kelly Loeffler
3) James Mountain Inhofe
4) David Alfred Perdue Jr
* Interesting fact is that Congress Member are expected to report the transaction within 30 days and median delay in dataset was 28 days.
* There is no disclosure for exact amount of money invested only price ranges (e.g., $100K - $200K) so for calculations of $ amounts of trades I used average of the given range.

## SW & libraries
Project is created with:
* PyCharm 2021 (Community Edition)
* Python version: 3.8.5
* Python libraries: matplotlib, pandas, seaborn, numpy 

## Data
* https://efdsearch.senate.gov/search/home/

## Trades summary
* During the 33 day period most active David Perdue sold 44 times with combined value of almost $3.5M. James Inhofe sold only 8 time but value of shares he sold was $4.22M. Richar Burr is the only one that after the scandal step down from the intelligence committee. He sold only (compared to others) 29 times with a value of $1.1M. Kelly Loeffler made 41 transactions of $2.68M.

![Trades](https://github.com/vldmrmrv/2020-insider-trading-study/blob/master/charts/num%20of%20trades.png) 

![Amount](https://github.com/vldmrmrv/2020-insider-trading-study/blob/master/charts/amount%20of%20shares%20(M).png)

## Best trades (senator - ticker)
* 10 best trades by senators have a clear winner. David Perdue is presented 7 times in top 10 list and absolute best trade in (CZR) Ceasars Entertainment saved David Perdue -83% drop in stock prices. Interesting observation is that senators mainly sold stock releated to hospitality and entertainment industries or that Richard Burr reassured US public the USA is well prepeared for the pandemic and in next two weeks sold more than $1MM of stocks.
![Best](https://github.com/vldmrmrv/2020-insider-trading-study/blob/master/charts/best%20trades.png) 

## Money saved
* Finally last chart showing $ amount of money saved by well timed solds. David Perdue saved most of the four, approximately $2.2M in market crash. Kelly Loeffler +1.0M, James Inhofe +$874K and Richard Burr +$475K.
```python
sns.set_theme(style="whitegrid")
sns.barplot(x="Senator", y="Amount(Avg)", data=df2, ci=None, palette="YlGnBu")
plt.ylabel('$ Amount of shares sold (Millions)')
plt.show()
```
![Saved](https://github.com/vldmrmrv/2020-insider-trading-study/blob/master/charts/saved%20in%20millions.png)

## ---
Past performance is not indicative of future results. Data and information provided may be delayed. Data and information is provided for informational purposes only, and is not intended for trading purposes.
