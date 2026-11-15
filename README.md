# TA Chart

A technical-analysis chart for Vietnamese stocks and indices, world indices, commodities, FX and crypto.
One HTML file, no build step, no server: the page fetches data straight from the browser.

## Links

Open a chart directly with URL parameters:

| Parameter | Example | Meaning |
| :--- | :--- | :--- |
| `symbol` | `HOSE:HPG`, `VNINDEX`, `DAX`, `BINANCE:BTCUSDT` | What to chart. The prefix before `:` is optional. |
| `interval` | `1` `5` `15` `30` `60` `120` `240` `D` `W` `M` `Q` `Y` | Candle size (`1D`, `1W` also work). World series and crypto are daily only. |
| `vs` | `VN30` | Benchmark for relative strength, beta and % compare. |
| `lang` | `en`, `vi` | Page language. |

The address bar follows the chart, so copying it shares exactly what is on screen.

## Data

- Vietnamese stocks, indices, flows, ratios, world indices, commodities and FX: VNDirect public APIs.
- Crypto: Binance public market data (`data-api.binance.vision`).
- Corporate events, company news, the screener's prices and P/E, P/B, market cap: VNDirect finfo API.
- Live streams: SSI FastConnect through a private relay (access code), VNDirect, Binance, OKX, Yahoo.

Charting library: [Lightweight Charts](https://github.com/tradingview/lightweight-charts) by TradingView (Apache 2.0), inlined.

## Update

The working copy lives in the desk folder (`others/website/ta_chart/TA.html`). To publish a new version:

```bash
cp ~/Desktop/broker_data/others/website/ta_chart/TA.html ~/Desktop/ta-chart/index.html
cd ~/Desktop/ta-chart && git commit -am "Update chart" && git push
```
