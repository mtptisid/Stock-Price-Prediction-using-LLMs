
# LLM-based Finance Agent

This project is an AI-powered finance agent that leverages large language models (LLMs) to analyze stock market trends, predict future prices, and provide insights into stocks. It integrates data from various sources, including Yahoo Finance for stock data and NewsAPI for stock news articles. The agent uses this data to make predictions and assist in financial decision-making.

## Features

- **Stock Data Analysis**: Fetches stock data using the `yfinance` package.
- **Stock News Integration**: Fetches relevant news articles using NewsAPI to analyze market sentiment.
- **Backtesting**: The agent can perform backtesting to evaluate the accuracy of predictions over a historical period.
- **Prediction Model**: Uses machine learning techniques to predict future stock prices.

## Requirements

To run this project, you need to install the following dependencies:

- `yfinance`: For fetching historical stock data.
- `newsapi-python`: For fetching stock news articles.
- `pandas`: For handling and processing data.
- `streamlit`: For building a web interface (if applicable).
- `sklearn` (if you're using machine learning models for prediction).

You can install the required dependencies by running:

```bash
pip install -r requirements.txt
```

## Configuration

The configuration file (`config.json`) should include the following details:

- `stock_symbol`: The stock symbol (e.g., 'AAPL', 'MSFT').
- `news_api_key`: Your NewsAPI key to fetch news articles.
- Other configuration parameters as required by your specific use case.

Example of `config.json`:

```json
{
  "stock_symbol": "AAPL",
  "news_api_key": "your-news-api-key"
}
```

## Usage

1. **Initialize the News API client**: The `newsapi` object is initialized with your API key to fetch stock-related news.
2. **Fetch Stock Data**: Use `yfinance` to get stock data for the given symbol.
3. **Backtesting**: Use the agent's `backtesting` method to run historical performance analysis.
4. **Prediction**: The `predict` method uses the stock news and historical data to predict future prices.

### Example:

```python
from datetime import datetime
from agent import Agent

# Load configuration
config = {
    'stock_symbol': 'MSFT',
    'news_api_key': 'your-news-api-key'
}

# Initialize the agent
agent = Agent(config)

# Set the date for prediction
date = datetime(2024, 11, 28)

# Run backtesting
results_df = agent.backtesting(date, date)

# Print prediction results
print(results_df)
```

## Screenshots
---
<img width="1440" alt="Screenshot 2024-12-29 at 4 07 38 PM" src="https://github.com/user-attachments/assets/7134470d-dc18-4ac8-b0da-0fb46db0a01a" />

---

<img width="1440" alt="Screenshot 2024-12-29 at 4 07 49 PM" src="https://github.com/user-attachments/assets/2ac9fa11-0479-487e-a8d2-aa28f97c5408" />

---

<img width="1440" alt="Screenshot 2024-12-29 at 4 07 10 PM" src="https://github.com/user-attachments/assets/a3c69c5e-3e5f-4c52-a412-c0d954aa6de7" />

---
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



## Acknowledgments

- Yahoo Finance API for stock data.
- NewsAPI for fetching stock-related news articles.
- Streamlit for building the interactive interface (if applicable).

