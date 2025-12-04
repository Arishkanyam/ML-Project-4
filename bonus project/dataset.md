# Dataset description for KOSPI prediction

## Data source
- **Provider**: Yahoo Finance (downloaded via yfinance Python library)
- **Description**: historical daily price and volume data for the KOSPI(South Korean index) index (^KS11), with duration of previous 5 years starting from December 4th of 2019 to December 4th of 2024. This includes open, high, low, close, adjusted close, and volume data.
- **Collection Method**: downloaded automatically via existing yfinance API (given follows Yahoo Finance's Terms of Service, limits, etc.). Data is fetched programmatically and cached locally.
- **License/Terms of Service**: Yahoo Finance data is free for collecting for non-commercial and personal use. Redistribution is prohibited; comply with their ToS (no excessive API calls). We do not struggle with any copyright issues as data is available for public analysis.
- **Data Volume**: approximately 1200 trading days excluding days with not stated data (calculated from amount of working days in a year).

## Column Definitions
- **Date**: trading date (datetime, YYYY-MM-DD);
- **Open/High/Low/Close/Adj Close**: daily price levels (float, KRW);
- **Volume**: daily trading volume (int);
- **returns**: daily percentage change in Close price (float, 0.01)
- **excess_returns**: daily returns minus assumed risk-free rate (float, 0% to not make it complex);
- **target_excess_ret**: 3 day-ahead excess returns (float);
- **ret_5d**: 5 day cumulative return (float);
- **vol_5d**: 5 day rolling standard deviation of returns (float, volatility proxy);
- **vol_ratio**: volume relative to its 5 day rolling mean (float, liquidity proxy);
- **momentum**: momentum proxy, calculated as: ret_5d/vol_5d + epsilon(float, trade-driven indicator).

## Ethical Considerations
- Data collection respects API limits to avoid overloading servers.
- No personal or sensitive data; all financial data is public.