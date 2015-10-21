---
layout: home
---

# QuoteServer (PHP)

Lightweight server that can process queries for EOD and historical data.

## Scraper

The QuoteServer scraper runs every day and scrapes data from different sources for multiple exchanges.

Gets symbol listing from these sources:
* http://www.nasdaq.com/screening/companies-by-name.aspx?letter=0&exchange=nasdaq&render=download
* http://www.nasdaq.com/screening/companies-by-name.aspx?letter=0&exchange=nyse&render=download
* http://www.nasdaq.com/screening/companies-by-name.aspx?letter=0&exchange=amex&render=download

Gets EOD data from Yahoo! finance.

## API

Can output JSON or return a ZIP of CSV files.

`/?s={comma-separated symbols list}&e={exchange}&t={date or date range or number of days in the past}&f={json|zip}` If `e` is specified, `s` is ignored. If `t`is not specified, only the latest day of data is returned. If `f` is not specified, JSON is the default.
`/?stats` returns statistics in JSON format about the contents of the database.
`/?dump` returns a ZIP file containing all of the historical data for every stock in the database.

## Technical

Lightweight (doesn't use a framework).
Easy to spawn (no configuration, no installation required: deploy and run, it takes care of creating the database tables).
To gain the most out of this component, it makes sense to deploy it on a server with high bandwidth and low disk latency (lots of database querying, returns huge chunks of data).
