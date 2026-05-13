
# High-Frequency Trading Engine using C++

A high-performance limit order book and trade matching engine in C++ using STL and the chrono library.

## Features

- Limit order book with efficient tree-based structure
- Order matching and execution engine
- Single and multi-threaded implementations
- Order lifecycle management (pending, fulfilled, canceled)
- Real-time transaction logging

## Project Structure

```
├── include/TradingEngine/     # Header files
│   ├── order.h
│   ├── order_book.h
│   ├── order_tree.h
│   ├── limit_order.h
│   ├── order_status.h
│   ├── order_type.h
│   └── transactions.h
├── src/                        # Source files
│   ├── main.cpp
│   ├── order.cpp
│   ├── order_book.cpp
│   ├── order_tree.cpp
│   ├── limit_order.cpp
│   ├── single_threaded.cpp
│   ├── multi_threaded.cpp
│   └── Makefile.txt
└── output/                     # Generated output files
```

## Build

```bash
cd src
make
./trading_engine
```

## Key Components

| Component | Purpose |
|-----------|---------|
| **Order** | Represents individual trading orders |
| **OrderBook** | Manages buy/sell order trees |
| **OrderTree** | Tree structure for efficient order storage |
| **LimitOrder** | Limit order handling logic |
| **Transactions** | Transaction recording and logging |

## Usage

```cpp
// Create and process an order
Order buy_order("AAPL", 1001, OrderType::BUY, 150.25, 100);
order_book.processOrder(buy_order);

// Get results
std::string results = order_book.getResults();
```

## Performance

- Order insertion: O(log n)
- Order matching: O(log n)
- Order cancellation: O(log n)

## Requirements

- C++11 compatible compiler (g++ 4.8+)
- Make utility
- Linux, macOS, or Windows (MinGW)

## Output Files

- `output_buy_prices.txt` - Buy order prices
- `output_buy_sizes.txt` - Buy order volumes
- `output_sell_prices.txt` - Sell order prices
- `output_sell_sizes.txt` - Sell order volumes

## Author

Hemant Pratap Singh (@hemantps-prog)

## Repository

[GitHub - High-Frequency Trading Engine](https://github.com/hemantps-prog/High-Frequency-Trading-Engine-using-Cplusplus)
