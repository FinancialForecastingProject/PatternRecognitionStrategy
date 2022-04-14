<!-- markdownlint-disable no-inline-html first-line-h1 -->

<div align="center">
  <a href="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/" target="_blank">
    <img width="200" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/Logo.svg?sanitize=true">
  </a>

  <h1><b>Pattern Recognition Strategy</h1>

  [![ProgressionLink][progress]][ProgressionLink] [![license][license]][license] [![twitterLink][twitter]][twitterLink]

</div>

[Documentation](https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/wiki) | [Discord community](https://discord.gg/PHrywfC6Ze)


**Table of content**
- [Pattern Recognition Strategy](#pattern-recognition-strategy)
  - [Other way to identify patterns](#other-way-to-identify-patterns)
  - [How to predict](#how-to-predict)
- [Contributors](#contributors)
<div align="justify">
Pattern Recognition Strategy is a prediction strategy we established observing what happened on financial markets.
Through our experience in trading, we had the opportunity to learn technical analysis and market fundamentals.

In fact, markets are efficient by definition, and since traders try to follow the technical analysis it results in the predicability of the market and we are able to observe patterns.

However, since patterns might be difficult to identify we tried to analyze and categorize each and every pattern using a mathematical approach.</div>

## Pattern Recognition Strategy


<div align="center">
  <a>
    <img width="100%" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/PatternMatchingAnalysis.svg?sanitize=true">
  </a>
</div>
<div align="justify">
We developed an algorithm which calculates the sum of relative distances between two points.
The output is the average distance between two points, and the lower the output is the better the pattern matches to the reference curve.

### Other way to identify patterns

  We also compared this method to the Dynamic Time Warping method.</div>

<div align="center">
  <a>
    <img width="45%" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/dtw_AAPL_AMZN.png?sanitize=true">
  </a>
  <a>
    <img width="45%" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/dist_point_par_pointAAPL_AMZN.png?sanitize=true">
  </a>
</div>

```
Point to point AAPL / AMZN  Mean distance : 0.02
Dynamic time warping AAPL / AMZN Mean distance : 0.02
```
<div align="justify">
Concerning the result we concluded that the comparison with the point to point strategy was as relevent as the dynamic time warping one. 
Since we had to be as clear as possible concerning the strategy we decided to go for the point to point distance strategy.</div>

### How to predict
  <div align="justify">
  First of all we have searched for strategies to set up a prediction using the data we extracted from this pattern recognition, what came up first was a strategy inspired by Rolling Forecasts based on the continuous analysis of past data to know what would happen in the future. This is the starting point of our project and we will introduce it in the following points.</div>

1. Let's assume that we have a reference dataset : the 21 last days of daily close prices for AAPL
We want to predict what will happen in 21 days on the AAPL chart.

1. We go through a strong database of charts with daily close prices for a given list of assets (comparison assets).

1. Then we subdivide the database in list of 21 days (21 values) of close prices.

1. Now that we have a lot of charts (list of 21 values), we are able to compare them. Since they have the same length, we are able to use the point to point pattern matching analysis.

1. We put each and every 21 values charts in the algorithm to find the one which has the best pattern matching with our AAPL chart of 21 values.

1. Once we know which dataset (corresponding to a pattern) fits the best with our reference dataset, we look at what happened after the matching on the pattern.

![Prediction Illustration](https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/prediction_for_AAPL_using_PYPL.png?sanitize=true)]
  
###  Getting a forecast
<div align="justify">
To set up our forecast, we take the data from our curve of comparison which represents what happenned right after the data associated to the reference curve. We will divide these data by their mean in order to recentre these in a value that can be compared to the values extracted from the other curves, and then we multiply these data again by the reference curve mean (we are scalling up these curves). Once this is done, we just have to read the desired value, for example if you want a forecast on the 7th day, you will read the 7th value.</div>

###  The margin of error
<div align="justify">
Once we got our forecast, we will compare it with the actual value and then calculate the margin of error. We will use it to understand our forecast and it will show if it was right or not.</div>

###  Improve the result
<div align="justify">
With a curve of comparison we get a forecast. We looked at what would happen we took a large amount of curves and did multiple forecasts to get the mean of all of these. So we edited our algorithm to add a new curve each time we calculate a forecast. The point was then to compare with how many curves we could get the slightest margin of error.</div>


## Contributors
<a href = "https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/graphs/contributors">
  <img src = "https://contrib.rocks/image?repo=FinancialForecastingProject/PatternRecognitionStrategy" alt="contributors : Hugo DEMENEZ, Aksel MAHE, Benoît LUSSET"/>
</a>

[ProgressionLink]: https://app.clickup.com/20572724/v/x/kkuhm-648
[progress]: https://img.shields.io/badge/Progression-69.44%25-blue
[license]: https://img.shields.io/github/license/FinancialForecastingProject/PatternRecognitionStrategy
[twitter]:https://img.shields.io/twitter/url?url=https%3A%2F%2Fgithub.com%2FFinancialForecastingProject%2FPatternRecognitionStrategy%2F

[twitterLink]:https://twitter.com/intent/tweet?text=Wow:&url=https%3A%2F%2Fgithub.com%2FFinancialForecastingProject%2FPatternRecognitionStrategy%2F
