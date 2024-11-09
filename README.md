# Stock Trading and News Alert System
![OptionSweepsTradeuiGIF](https://github.com/user-attachments/assets/7c518557-fcc5-41df-9e44-be62c65dd7c3)

This Python script monitors the stock price of a specified company (e.g., Tesla Inc.) and sends SMS notifications with recent news articles when there's a significant price change. It uses the Alpha Vantage API to check stock price changes, the News API to fetch relevant news articles, and Twilio to send SMS notifications. In this project we used Tesla Inc. Stock price and alert Message.

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup and Installation](#setup-and-installation)
- [How to Use](#how-to-use)
- [Disclaimer](#disclaimer)
- [Example Output](#example-output)

## Project Overview

The script checks if the stock price of the company (e.g., Tesla Inc.) has increased or decreased by more than 5% from the previous day. If so, it fetches the latest news articles related to the company and sends SMS notifications to a specified phone number. Each SMS includes the percentage change, a relevant news headline, and a brief summary of the article.

## Technologies Used

- **Python**: The main programming language for scripting and data handling.
- **Alpha Vantage API**: Provides stock market data and historical pricing information.
- **News API**: Fetches the latest news articles related to the specified company.
- **Twilio API**: Sends SMS notifications with stock updates and news information.

## Setup and Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/Stock_Trading_News_Alert_System
    cd Stock_Trading_News_Alert_System
    ```

2. **Install Dependencies**:
    Install the required packages with:
    ```bash
    pip install requests twilio
    ```

3. **Environment Variables**:
   - Obtain API keys and credentials:
     - **Alpha Vantage API Key**: Get from [Alpha Vantage](https://www.alphavantage.co/support/#api-key).
     - **News API Key**: Get from [News API](https://newsapi.org/).
     - **Twilio SID and Auth Token**: Get from [Twilio](https://www.twilio.com/).
   - Replace the placeholder values in the script (`STOCK_API_KEY`, `NEWS_API_KEY`, `TWILIO_SID`, and `TWILIO_AUTH_TOKEN`) with your actual keys.

4. **Modify the Phone Number**:
   Replace the `from_` and `to` fields in the `client.messages.create()` function with your Twilio and destination phone numbers.

## How to Use

Run the script with:
```bash
python main.py
```

## Example Output

If the stock price change exceeds 5%, the SMS notification would look something like this:

**Message 1:**
```
TSLA: 🔺5.2%
Headline: Tesla's stock soars as electric vehicle sales hit record high.
Brief: Tesla Inc. reported a significant increase in electric vehicle deliveries, leading to a surge in stock price.
```

### Disclaimer

This project is for educational purposes. Be mindful of API usage limitations and associated costs when using it in a live environment.

Here's an example of what an output SMS message would look like:
