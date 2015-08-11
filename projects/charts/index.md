---
layout: home
---

## Charts

### Charts.StaticChart

A GDI+ library to generate static stock charts.

A [StaticChart](https://github.com/leboeuf/TradeHub-csharp/blob/master/TradeHub.Charts/StaticChart.cs) is composed of a list of [StaticChartModules](https://github.com/leboeuf/TradeHub-csharp/blob/master/TradeHub.Charts/StaticChartModule.cs), one of which is the price plot and the other ones are indicators.

[DrawingHelper](https://github.com/leboeuf/TradeHub-csharp/blob/master/TradeHub.Charts/GDI/DrawingHelper.cs) is a static wraper around the GDI+ drawing methods of the Graphics object. If the DEBUG constant is set to true, a PNG file will be saved to disk after each draw call. These images can then be combined into a GIF file that shows an animation of the chart's drawing process.

