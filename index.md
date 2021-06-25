## Embedded Components Documentation

Embedded components are custom built web components, that integrate with your Navexa portfolio 

## Embedded Component Types

We currently provide 3 types of Components.

* A Portfolio Component
<img src="/assets/images/portfolio-expanded.png" alt="drawing" width="200"/>
<!-- ![Portfolio](/assets/images/portfolio-expanded.png) -->

* A Chart component
![A Chart](/assets/images/chart-tooltip.png)

Each component has several configuration and customisation properties, which shall be discussed in detail for the rest of this document.


# The portfolio component
## Regular

Settings:
* Include Trades
* Columns:
    * Total Performance Bar:
        * Capital Gain %
        * Dividend Return %
        * Currency Gain %
        * Total Performance %

* Date Preset: (all-time | today | last-7-days | last-30-days | this-month | past year | year-to-date | last-two-years | last-3-years)
* From date: _performance will be calculated with this as the start date_
    * if not set, defaults to first trade date
* To date: _performance will be calculated with this as the end date_
    * if not set, it will default to the current date
* Include Closed Positions: this one needs a blog link and a help page.

## Publisher

# 

## Chart
Settings:
* Include Benchmark: Plots your configured benchmark against your portfolio
    * **note**: Professional feature
* Date Preset: (all-time | today | last-7-days | last-30-days | this-month | past year | year-to-date | last-two-years | last-3-years)
* From date: _performance will be calculated with this as the start date_
    * if not set, defaults to first trade date
* To date: _performance will be calculated with this as the end date_
    * if not set, it will default to the current date
* Include Closed Positions: this one needs a blog link and a help page.
