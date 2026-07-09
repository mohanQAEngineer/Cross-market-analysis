# Cross-market-analysis
Cross Market Analysis — A Streamlit dashboard for exploring correlations between Bitcoin, crude oil, and major stock indices (S&amp;P 500, NIFTY, NASDAQ). Includes an interactive market overview, a SQL query runner with 30+ prebuilt queries, and price-trend analysis for top cryptocurrencies — all backed by SQLite.
**Data layer** — crypto_df, coins_data, oil_data, and stocks_data tables live in a single SQLite database (cross_market_analysis.db), pre-populated with historical price data for cryptocurrencies, crude oil, and major stock indices.
Application layer — A single-file Streamlit app (crossmarketanalysis.py) connects to the database and exposes three modules via a sidebar menu (streamlit_option_menu):

**Market Overview** — date-range filter that computes average prices for Bitcoin, oil, S&P 500, and NIFTY, then joins all four sources into one daily snapshot table.
SQL Query Runner — a dropdown of 30+ prebuilt SQL queries (crypto stats, coin trends, oil volatility, stock comparisons, and cross-asset joins) that users can select and execute on demand.
Top 3 Crypto Analysis — coin + date-range selector that renders a price trend line chart and a detailed price table for the chosen cryptocurrency.

**Presentation layer** — Streamlit renders all output (charts, dataframes, controls) directly in the browser; pandas.read_sql_query bridges SQL results into DataFrames for display.
