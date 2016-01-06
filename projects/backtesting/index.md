---
layout: home
---

## Backtesting

The backtesting framework allows to test strategies using historical data.

### How it works

There is an example CLI project included to help you understand how to use the backtesting framework.

The backtest needs a [Portfolio](https://github.com/leboeuf/TradeHub-csharp/blob/master/TradeHub.Core.Model/Portfolio.cs) objects to work with (can be an empty portfolio or a portfolio that already has an history). Then it needs the stock to backtest and the strategy to run each tick.

### Strategy

A strategy is a C# file that implements the ITradingStrategy interface. It contains a single public method Run that gets executed on each tick.

### Step by step

The simulation can be run all at once or step by step. In the latter, it is possible to observe the simulation's behaviour after each tick and organically tweak the strategy to better perform.
