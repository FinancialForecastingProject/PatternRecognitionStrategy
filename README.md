<!-- markdownlint-disable no-inline-html first-line-h1 -->

<div align="center">
  <a href="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/" target="_blank">
    <img width="200" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/Logo.svg?sanitize=true">
  </a>

  <h1><b>Pattern Recognition Strategy</h1>

  [![ProgressionLink][progress]][ProgressionLink] [![license][license]][license] [![twitterLink][twitter]][twitterLink]

</div>

[Documentation](https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/wiki) | [Discord community](https://discord.gg/PHrywfC6Ze)


Pattern Recognition Strategy is a prediction strategy we established observing what happened on financial markets.
Through our experience in trading, we had the opportunity to learn technical analysis and market fundamentals.

In fact, markets are efficient by definition, and since traders try to follow the technical analysis it results in the predicability of the market and we are able to observe patterns.

However, since patterns might be difficult to identify we tried to analyze and categorize each and every pattern using a mathematical approach.

## Pattern Recognition Strategy
<div align="center">
  <a>
    <img width="100%" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/PatternMatchingAnalysis.svg?sanitize=true">
  </a>
</div>

We developed an algorithm which calculates the sum of relative distances between two points.
The output is a score, and the lower the score is the better the pattern matches to the reference curve.

### Other way to analyze patterns

We also compared this method to the Dynamic Time Warping method.

<div align="center">
  <a>
    <img width="100%" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/dtw_AAPL_AMZN.png?sanitize=true">
  </a>
  <a>
    <img width="100%" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/dist_point_par_pointAAPL_AMZN.png?sanitize=true">
  </a>
  <a>
    <img width="100%" src="https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/raw/main/.github/distance_results.png?sanitize=true">
  </a>
</div>

Concerning the result we concluded that the comparison with the point to point strategy was as relevent as the dynamic time warping one. 

## Contributors
<a href = "https://github.com/FinancialForecastingProject/PatternRecognitionStrategy/graphs/contributors">
  <img src = "https://contrib.rocks/image?repo=FinancialForecastingProject/PatternRecognitionStrategy" alt="contributors : Hugo DEMENEZ, Aksel MAHE, Benoît LUSSET"/>
</a>

[ProgressionLink]: https://app.clickup.com/20572724/v/x/kkuhm-648
[progress]: https://img.shields.io/badge/Progression-69.44%25-blue
[license]: https://img.shields.io/github/license/FinancialForecastingProject/PatternRecognitionStrategy
[twitter]:https://img.shields.io/twitter/url?url=https%3A%2F%2Fgithub.com%2FFinancialForecastingProject%2FPatternRecognitionStrategy%2F

[twitterLink]:https://twitter.com/intent/tweet?text=Wow:&url=https%3A%2F%2Fgithub.com%2FFinancialForecastingProject%2FPatternRecognitionStrategy%2F
