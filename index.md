## Navexa Embedded Components Documentation

Embedded components are custom built web components, that integrate with your Navexa portfolio to display your _True performance_ in the context of your blog or website.

## Component Types

Navexa currently provides 3 types of Components.
* Portfolio: Displays your portfolios total performance
* Chart: displays a chart of your portfolio's total performance %
* Trades: Displays a list of trades executed in your portfolio

Each component has several configuration and customisation properties, which shall be discussed in detail for the rest of this document.

# Portfolio Component

![Portfolio](/assets/images/portfolio-expanded.png)
## Settings:

> **Notes:**
> - Settings must be manually configured by Navexa. Reach out to your Navexa contact to tweak these settings! 
> - All Columns can be renamed, reordered or hidden.
>
> ** = Premium publisher feature. Only available upon special request

* __Include Trades **__ 
    - A list of each holdings trades are available in an expanded section. View screenshot.
* **Total Performance Columns**
    * Capital Gain %
    * Dividend Return %
    * Currency Gain %
    * Total Performance %
* **Date Preset:** 
    - **all-time (default)**
    - today
    - last-7-days
    - last-30-days
    - this-month
    - past-year
    - year-to-date
    - last-two-years
    - last-3-years
* **From date:**
    * Performance will be calculated with this as the start date
    * If not set, defaults to first trade date
* **To date:** 
    * Performance will be calculated with this as the end date
    * If not set, it will default to the current date
* **Include Closed Positions:** this one needs a blog link and a help page.
* **Holding Table Columns:**
    * Security: Symbol + Exchange
    * Capital Gain %
    * Dividend Return %
    * Currency Gain %
    * Total Return %
    * Buy Limit ** 
    * Current Recommendation ** 
        - buy, sell, hold
    * Stop loss limit ** 
    * Last Trade on Holding **


# Chart

![Chart](/assets/images/chart-tooltip.png)

## Settings:

> **Notes:**
> - Settings must be manually configured by Navexa. Reach out to your Navexa contact to tweak these settings! 
> - All Columns can be renamed, reordered or hidden.
>
> ** = Premium feature. Only available to paying customers

* __Include Benchmark **__: Plots your configured benchmark against your portfolio
* **Date Preset:** 
    - **all-time (default)**
    - today
    - last-7-days
    - last-30-days
    - this-month
    - past-year
    - year-to-date
    - last-two-years
    - last-3-years
* **From date:**
    * Performance will be calculated with this as the start date
    * If not set, defaults to first trade date
* **To date:** 
    * Performance will be calculated with this as the end date
    * If not set, it will default to the current date
* **Include Closed Positions:** this one needs a blog link and a help page.


# Trade Component

![Trade](/assets/images/trades-sell.png)

## Settings

> **Notes:**
> - Settings must be manually configured by Navexa. Reach out to your Navexa contact to tweak these settings! 
> - All Columns can be renamed, reordered or hidden.
>
> ** = Premium feature. Only available to paying customers

* **Trade Type Filter**: Trades types you wish to display
* **Columns:**
    * Security: symbol + exchange
    * Trade Date
    * Price
    * Return %: only available for sell trades
    * Notes
* **Date Preset:** 
    - **all-time (default)**
    - today
    - last-7-days
    - last-30-days
    - this-month
    - past-year
    - year-to-date
    - last-two-years
    - last-3-years
* **From date:**
    * Performance will be calculated with this as the start date
    * If not set, defaults to first trade date
* **To date:** 
    * Performance will be calculated with this as the end date
    * If not set, it will default to the current date
* **Include Closed Positions:** this one needs a blog link and a help page.


# Customizing Styles
You might want to make the Embedded Component's styling to match your blog or website. In that case, you are in luck! The components are extremely customisable.

> **Warning**: Although it possible to hide the Navexa logo, any attempts to modify, obstruct or restrict visibility or interactivity are prohibited. Violations of these terms will result in restriction and possible termination of components and other published mediums provided by Navexa.
> Ye have been warned.


## Wordpress Steps
1. Navigate to the page where you plan to embed your component
2. Create a HTML block
![wordpress html block](/assets/images/wordpress-steps.png)
3. Create a special style tag
    - Note: You should only need to create the style tag ONCE PER PAGE. Only the first will be used by each embedded component per page.
4. Enter your html embed code
5. Customize the styles according to the following per-component style-guide below.

Example:
```html
<style id="nvx-styles">
</style>
```

## HTML Steps
1. Navigate to the html document you plan to embed your component
2. Create a style tag at the head of your blog/ website, with a tag of `class="nvx-styles"`.
3. Embed your custom component
4. Customize the styles according to the following per-component style-guide below.

Example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>My Portfolio Blog</title>
    <style class="nvx-styles">
        <!-- my styles -->
    </style>
</head>
<body>
    <!-- my chart component -->
    <div id="xxxxxxxx-3A35-4F9B-8C6C-yyyyyyyyyyyy">
        <script async src="https://embd.navexa.io/nx-chart.js" charset="UTF-8"></script>
    </div>
</body>
</html>
```

## CSS Styles
Each component primarily uses css variables to customise the theme. Each of the variables following can be used to style and decorate the portfolio component:
The variables need to be defined in a `main` element to be correctly set.

```html
<style class="nvx-styles">
main {
    /* My styles */
}
</style>
```

## Portfolio Styles

```css
main {
    /* Changes the width of the component */
    --nx-width: 600px;
    /* Only used for special publisher components */
    --nx-publisher-max-width: 850px;
    /* Changes the maximum height of the holdings list table */
    --nx-holdings-height: 300px;
    /* Changes the font attributes */
    --nx-font-family: Arial, serif;
    --nx-font-size: 1rem;
    --nx-font-weight: normal;
    /* Changes the component border radius */
    --nx-border-radius: 5px;

    /* The various colour swatches used over the component */
    --nx-green: #22b922;
    --nx-red: #ff0319;
    --nx-grey: #7e8e9f;
    --nx-card: white;
    --nx-text: #333;
    --nx-background: #f4f8fb;
    --nx-border: #e7e7e7;
    --nx-detail: #fbfbfb;
}
```

## Chart Styles

```css
main {
    /* Changes various font attributes */
    --nx-font-family: Arial, serif;
    --nx-font-size: 0.875rem;
    --nx-font-weight: normal;
    --nx-border-radius: 5px;

    /* The various colour swatches used over the component */
    --nx-green: #22b922;
    --nx-red: #ff0319;
    --nx-grey: #7e8e9f;
    --nx-card: white;
    --nx-text: #333;
    --nx-background: #f4f8fb;
    --nx-border: #e7e7e7;
}
```

## Trades Styles

```css
main {
    /* Changes the width of the component */
    --nx-width: 600px;
    /* Changes font attributes */    
    --nx-font-family: Arial, serif;
    --nx-font-size: 0.875rem;
    --nx-font-weight: normal;
    --nx-border-radius: 5px;

    /* The various colour swatches used over the component */
    --nx-green: #22b922;
    --nx-red: #ff0319;
    --nx-grey: #7e8e9f;
    --nx-card: white;
    --nx-text: #333;
    --nx-background: #f4f8fb;
    --nx-border: #e7e7e7;
}
```