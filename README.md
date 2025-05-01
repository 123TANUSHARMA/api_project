# Crypto Market Explorer

Crypto Market Explorer is a web application that provides real-time data from the Blockchain API for cryptocurrencies. It allows users to view ticker information, order book data, and detailed symbol-specific information, making it an essential tool for those looking to explore and analyze cryptocurrency market trends.

## Features

- **Ticker Information**: Enter a cryptocurrency symbol to retrieve its price, trading volume, and last trade price.
- **Order Book**: Get detailed Level 3 (L3) order book data, including bid and ask prices, quantities, and order numbers.
- **Symbol Information**: View specific data about a cryptocurrency symbol, such as its base currency, minimum price increment, and auction details.
- **User-Friendly Interface**: Dynamic content rendered through EJS templates, providing an intuitive and responsive user experience.

## Tech Stack

- **Node.js** with **Express**: Backend framework for building the server and handling HTTP requests.
- **Axios**: HTTP client for fetching data from the Blockchain API.
- **EJS**: Template engine for rendering dynamic data into HTML pages.
- **HTML/CSS**: For building and styling the user interface.

## Installation

To run the Crypto Market Explorer locally, follow these steps:

### Prerequisites

Make sure you have the following installed:
- [Node.js](https://nodejs.org/) (v14 or above)
- npm (Node Package Manager)

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/crypto-market-explorer.git
   cd crypto-market-explorer
