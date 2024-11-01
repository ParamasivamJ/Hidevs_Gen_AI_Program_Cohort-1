
# Financial Market Analysis System

## Overview

The **Financial Market Analysis System** aims to develop a robust solution for retrieving and analyzing financial market data using memory and knowledge graphs. This system facilitates multi-query tasks, empowering users to explore historical stock data and derive insights through a comprehensive dashboard interface.


## Data Stored in the Graph Database

The system stores detailed information about publicly traded companies, their stock prices, and related financial metrics. Below is a summary of the data structure and the relationships represented in the graph database.

### Database Information

- **Total Nodes:** 2,274
  - **Company Nodes**: Represents individual companies, each with properties such as name, symbol, industry, and sector.
  - **StockPrice Nodes**: Represents daily stock price data, including attributes for open, close, high, low prices, and volume.
  - **Date Nodes**: Represents specific dates for the stock price entries.

- **Total Relationships:** 4,531
  - **HAS_PRICE**: Links a company to its stock price information.
  - **HAS_STOCK_PRICE**: Connects stock price data to the respective date of that price.

#### Example Visualization of Company Nodes

![Company Nodes](Week-3\images\companies.jpg)

*This image shows the nodes representing various companies in the database.*

#### Example Visualization of Stock Price Relationships

![Stock Price Relationships](Week-3\images\Relationship.jpg)

*This image illustrates the relationships between  and their stock price data.*

### Conclusion

The Financial Market Analysis System is designed to offer users a powerful tool for interacting with financial data. By leveraging memory and knowledge graphs, the system not only provides insights into historical data but also enhances the analysis process, allowing for a deeper understanding of the financial landscape.

## Getting Started

1. Clone the repository.
2. Ensure you have Neo4j set up and running.
3. Load the data into the Neo4j database using the provided APIs.
4. Run the application and start exploring the financial market data.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
