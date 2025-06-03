# XTF - Trading Log Analyzer
**VUT FIT 2023/24 - IOS Project 1**

A bash script for analyzing cryptocurrency trading logs from log files.  
There are 3 examples of what the log files can look like in files cryptoexchange-*.

## Usage

```bash
./xtf [FILTERS] [COMMAND] [USERNAME] [FILES...]
```

## Commands

- `list` - Show user's trading logs
- `list-currency` - List currencies used by user
- `status` - Show account balance by currency
- `profit` - Show balance with fictional profit applied

## Filters

- `-a DATETIME` - Show logs after date (YYYY-MM-DD HH:MM:SS)
- `-b DATETIME` - Show logs before date
- `-c CURRENCY` - Filter by specific currency
- `-h, --help` - Show help

## Examples

```bash
# Show all trades for user john
./xtf list john trades.log

# Show Bitcoin trades after specific date
./xtf -a "2023-01-01 00:00:00" -c BTC list john trades.log

# Show account status with 25% profit
XTF_PROFIT=25 ./xtf profit john trades.log
```

## Environment

- `XTF_PROFIT` - Profit percentage (default: 20%)  


Total points: 12/15
