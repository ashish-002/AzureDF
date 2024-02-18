AlphaETLPipeline

Overview:
AlphaETLPipeline is an Azure Data Factory pipeline designed to extract sentiment data for various tickers using the AlphaVantage API. This pipeline consists of activities to retrieve ticker data from a storage location, set up the AlphaVantage API call, iterate through each ticker, retrieve sentiment data from the API, and perform data processing using a data flow.

Activities:
Lookup Ticker: This activity retrieves ticker data from a specified storage location.

Alpha API Setup: This activity sets up the AlphaVantage API call with the necessary parameters, such as ticker symbol, API key, and time range.

ForEach Ticker Iteration: This activity iterates through each ticker retrieved from the Lookup Ticker activity.

a. Copy data from API: This activity retrieves sentiment data from the AlphaVantage API for each ticker and writes it to a destination dataset.

b. Data flow for JSON Output: This activity processes the JSON data output from the API call using a data flow.

Pipeline Annotations
Retries are disabled.

Note: This README provides an overview of the AlphaETLPipeline. For detailed information on each activity, including configurations and dependencies, refer to the pipeline definition file.
