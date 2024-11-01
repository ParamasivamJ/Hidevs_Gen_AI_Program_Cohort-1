# Financial Market Analysis System

## Overview

The **Financial Market Analysis System** is designed to retrieve and analyze financial market data using Neo4j as a graph database. This system supports multi-query tasks that allow users to explore historical stock data, link companies to relevant market events, and visualize relationships between various financial entities.

## Data Stored in the Graph Database

The system stores information about various publicly traded companies, their stock prices, and related financial metrics. Below is a summary of the data structure and the relationships represented in the graph database.

### Database Information

- **Total Nodes:** 2,274
  - **Company Nodes:** Represents individual companies, each with properties such as name, symbol, industry, and sector.
  - **StockPrice Nodes:** Represents daily stock price data, including attributes for open, close, high, low prices, and volume.
  - **Date Nodes:** Represents specific dates for the stock price entries.

- **Total Relationships:** 4,531
  - **HAS_PRICE:** Links a company to its stock price information.
  - **HAS_STOCK_PRICE:** Connects stock price data to the respective date of that price.

### Property Keys

The following property keys are utilized within the nodes of the database:

- **Company Node Properties:**
  - `name`: The full name of the company.
  - `symbol`: The stock ticker symbol.
  - `industry`: The industry classification.
  - `sector`: The sector classification.

- **StockPrice Node Properties:**
  - `date`: The date of the stock price entry.
  - `open`: The opening price for the stock on that date.
  - `close`: The closing price for the stock on that date.
  - `high`: The highest price during the trading session.
  - `low`: The lowest price during the trading session.
  - `volume`: The total number of shares traded.

### Graph Visualization

The visualization of the graph provides insights into the connections between companies and their stock price data. Below are some images representing the data stored in the graph database.

#### Example Visualization of Company Nodes

![Company Nodes](path_to_image/company_nodes.png)

*This image shows the nodes representing various companies in the database.*

#### Example Visualization of Stock Price Relationships

![Stock Price Relationships](path_to_image/stock_price_relationships.png)

*This image illustrates the relationships between companies and their stock price data.*

### Conclusion

The Financial Market Analysis System enables users to interact with financial data in a meaningful way, offering insights through the use of graph databases. The system is scalable and can be extended to incorporate more complex queries and analyses as required.

## Getting Started

1. Clone the repository.
2. Ensure you have Neo4j set up and running.
3. Load the data into the Neo4j database.
4. Run the application and start exploring the financial market data.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

