---
layout: page
title: the tape
permalink: /tape/
description: Live charts and market data.
nav: true
nav_order: 5
---

<div class="markets-container">

  <div class="tradingview-widget-container" style="height: 500px; margin-bottom: 2rem;">
    <div id="tradingview_spy"></div>
  </div>

</div>

<script type="text/javascript" src="https://s3.tradingview.com/tv.js"></script>
<script type="text/javascript">
  document.addEventListener("DOMContentLoaded", function () {
    var isDark = document.documentElement.getAttribute("data-theme") === "dark" ||
                 (window.matchMedia && window.matchMedia("(prefers-color-scheme: dark)").matches &&
                  document.documentElement.getAttribute("data-theme") !== "light");

    new TradingView.widget({
      "width": "100%",
      "height": 500,
      "symbol": "AMEX:SPY",
      "interval": "60",
      "timezone": "America/Chicago",
      "theme": isDark ? "dark" : "light",
      "style": "1",
      "locale": "en",
      "enable_publishing": false,
      "hide_side_toolbar": false,
      "allow_symbol_change": true,
      "container_id": "tradingview_spy"
    });
  });
</script>
