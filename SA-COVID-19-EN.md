# Seasonal Adjustment of Time Series During COVID-19 Crisis

**Central Statistical Bureau of Latvia**

- *23 July 2020*
- *21 December 2020* (update)

## Introduction

The primary objectives of seasonal and calendar adjustment of time series are:

- to exclude calendar effects from the time series (working day or trading day effects, leap-year effect);
- to exclude from the time series known and observable seasonal fluctuations which are repeating each year.

The secondary objective is:

- estimate the trend of the time series.

The issue of time series adjustment during the crisis can be split into two parts: seasonal adjustment (here and then, including calendar adjustment) and trend assessment.

Although the crisis affects almost all economic and social processes, there are time series for which the impact of the crisis is not economically justified. Such time series during the crisis are adjusted according to standard procedures. The content of the document below only applies to time series for which the impact of the crisis is economically justified.

The Central Statistical Bureau of Latvia (CSB) currently performs seasonal and calendar adjustments with the [JDemetra+ 2.2.3](https://github.com/jdemetra/jdemetra-app/releases) using the [TRAMO-SEATS method](https://jdemetradocumentation.github.io/JDemetra-documentation/pages/theory/).


## Seasonal Adjustment of Time Series During Crisis

Typically, with each new data point (period), we receive new information about the time series. Accordingly, each new data point makes it possible to recalculate seasonal and calendar effects in the light of the new information. There are different practices for recalculating seasonal and calendar effects. The seasonal and calendar effects are recalculated with each additional data point at the CSB.

The crisis period is special with the fact that we do not receive any new information on seasonality (including calendar effects). That is because the crisis is not seasonal. Major crises (including the COVID-19 crisis) are rare phenomena which do not occur every year.

*It should be noted that there is a hypothesis that such an epidemic of virus may become seasonal. Under such  scenario, the effect of virus epidemic will be adjusted as seasonal effect.*

During the crisis, we can only assess the seasonality of time series from data till the beginning of the crisis. To technically “freeze” seasonality and not to recalculate seasonality with data from the crisis period, the CSB uses two methods:

1. Primary method - all time series points affected by the crisis are defined as outliers. In this case, the outlier is added to the crisis period also if it is not statistically significant.
1. Secondary method - [fixed model](https://jdemetradocumentation.github.io/JDemetra-documentation/pages/case-studies/revision-fixed.html) (in guidelines and [JDemetra+](https://github.com/jdemetra) it is called *Current Adjustment* or *Fixed Model*). Using this method, the estimates of outliers and other regression coefficients are fixed. They are not recalculated with the new data. The procedure does not add new outliers. However, outliers can be added manually by the user.

In most cases, the primary method is used. In cases where, in addition to seasonal adjustment, a time series trend estimation is required, a secondary method is used. In both cases, we declare to the seasonal adjustment algorithm (in the [JDemetra+](https://github.com/jdemetra)) that the values of the crisis period of time series cannot be used to recalculate seasonality. Both methods are consistent with the crisis guidelines published by the Statistical Office of the European Union (*Eurostat*) and confirmed by the [ESS Seasonal Adjustment Helpdesk](https://ec.europa.eu/eurostat/cros/content/ess-seasonal-adjustment-helpdesk_en).

Review outliers for the crisis period according to the data and information provided by the statistical producers.


## Trend Estimation During Crisis

The crisis may have a dual impact on the time series trend:

- Transitory effect on the trend. There is an effect on trend during crisis. However, the effect immediately or gradually disappear after crises and trend returns to the level observed before crisis.
- Lasting effect on the trend. There is an impact on trend that is sustainable also after the end of the crisis.

During crisis (particularly at the beginning of the crisis), it is not possible to determine by mathematical methods which of two above mentioned scenarios is in force. It is therefore very important to use the assessment of economic experts on the impact of the crisis on the time series trend as an additional information.

It should be noted that trend estimation at the start and end points of the time series is not recommended. Trend estimates (especially during crisis) may be inaccurate and major revisions may occur.


## Summary

- The COVID-19 crisis in time series analysis is currently considered to be a non-seasonal event. Accordingly, the impact of the crisis is not excluded from the data by seasonal adjustment.
- We do not receive any new information about seasonal and calendar effects during the crisis, because the impact of the crisis prevents them from being observed. Therefore, seasonal and calendar effects are estimated using only pre-crisis data.
- Seasonal or calendar adjustments are applied also to the crises period with seasonal and calendar effects estimated using pre-crisis data.
- It should be noted that during crisis, both unadjusted and seasonal and calendar-adjusted data may be subject to higher data revisions than usually.
- Trend estimates (especially for crisis period) may be inaccurate and subject to major revisions.


## References

- ESS SA Helpdesk (2019) [A brief description of JDemetra+](https://jdemetradocumentation.github.io/JDemetra-documentation/)
- Eurostat (2015) [ESS guidelines on seasonal adjustment](https://ec.europa.eu/eurostat/web/products-manuals-and-guidelines/-/KS-RA-09-006), section *2.8. Treatment of outliers at the end of the series and at the beginning of a major economic change*
- Eurostat (2020) [Guidance on time series treatment](https://ec.europa.eu/eurostat/documents/10186/10693286/Time_series_treatment_guidance.pdf)
- Eurostat (2020) [Guidance on the EU-Labour Force Survey data collection](https://ec.europa.eu/eurostat/documents/10186/10693286/LFS_guidance.pdf)
- Statistics Norway (2020) [Season adjustment during the Corona crisis](https://github.com/statisticsnorway/SeasonalAdjustmentCorona)
