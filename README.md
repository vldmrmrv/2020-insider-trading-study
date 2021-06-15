## 2020 Insider trading study
* [General info](#general-info)
* [Methodology](#methodology)
* [SW & libraries](#sw-&-libraries)
* [Data](#data)
* [Seasonality Example](#seasonality-example)
* [Mid term study Example](#mid-term-study-example)
* [Short term study Example](#short-term-study-example)

## General info
* The 2020 congressional insider trading scandal was a political scandal in the United States involving allegations that several members of the United States Senate violated the   STOCK Act by selling stock at the start of COVID-19 pandemic in the United States and just before a stock market crash on February 20, 2020, using knowledge given to them at a   closed Senate meeting. The Department of Justice initiated a probe into the stock transactions on March 30, 2020. No charges were brought against anyone and all investigations   into the matter are closed. (source: wikipedia)
 
## Methodology
Starting point of analysis will be January 24 (Closed meeting held on January 24, 2020) and any seles made by senators up to February 26 is considered for analysis (start of the crash February 26). Focus will be on 4 senators that were investigated by Justice Department and the FBI following the trading scandal.
1) Richard Burr
2) Kelly Loeffler
3) James Mountain Inhofe
4) David Alfred Perdue Jr
* Interesting fact is that Congress Member are expected to report the transaction within 30 days and median delay in dataset was 28 days.

## SW & libraries
Project is created with:
* PyCharm 2021 (Community Edition)
* Python version: 3.8.5
* Python libraries: matplotlib, pandas, seaborn, numpy 

## Data
* https://efdsearch.senate.gov/search/home/

## Trades summary
* Seasonality is well calendar effect in markets worth investigating in case of planning trading/investing for longer period of time. Seasonal patterns are constructed by plotting daily data against calendar/trading days rather than simply averaging daily/weekly/monthly data. Such daily data has proven to be far more valuable when looking for consistent and precise entry and exit dates.
* The following chart reflect seasonal patterns for SPX index over the period of a calendar year. Long term studies tend to survive for decades and as we can see very little changes of long term seasonal patterns occured during last 60 years.
![Trades](https://github.com/vldmrmrv/2020-insider-trading-study/blob/master/charts/num%20of%20trades.png)
* Closer look on individual months will help with timeing entries and exists. For example: second half of October is usually good time to initiate long term LONG possition in SPX/ES/SPDR with a potential of holding till the end of the calendar year and catching historically strongest period of the year.
![Amount](https://github.com/vldmrmrv/2020-insider-trading-study/blob/master/charts/amount%20of%20shares%20(M).png)
## Mid term study Example
*  Study of weekly volatility during the year. Data for last 20 years indicates October is the most volatile month of the year.
![Best](https://github.com/vldmrmrv/2020-insider-trading-study/blob/master/charts/best%20trades.png) 

## Short term study Example
*  Releationship between RTH range and IB range for different opening types and days of the week. Useing Seaborn-Implot to fit regression models across conditional subsets of a dataset.
```python
sns.set_theme(style="whitegrid")
sns.barplot(x="Senator", y="Amount(Avg)", data=df2, ci=None, palette="YlGnBu")
plt.ylabel('$ Amount of shares sold (Millions)')
plt.show()
```
![Saved](https://github.com/vldmrmrv/2020-insider-trading-study/blob/master/charts/saved%20in%20millions.png)

## ---
Past performance is not indicative of future results. Data and information provided may be delayed. Data and information is provided for informational purposes only, and is not intended for trading purposes.
