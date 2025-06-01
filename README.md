# XSS Gauntlet

## Overview
This repository contains solutions to the three reflected XSS challenges from CSCI-UA.0480 (XSS Gauntlet). Each challenge’s payload exfiltrates the admin bot’s cookie to a Webhook.site request bin, yielding a unique flag. 

## Tech Stack
- **Browser** (Chrome/Firefox) for JavaScript console and HTML input  
- **Webhook.site** (request bin) to collect exfiltrated cookies  
- **Standard HTML tags & attributes** (e.g., `<script>`, `<body onload>`, `<svg onload>`)


## Key Takeaways

- **Reflected XSS:** Injecting payloads directly into HTML allows execution of arbitrary JavaScript in the victim’s context.
- **Bypassing Filters:** Event handlers (e.g., `onload`) can be used when `<script>` is blocked—simply attach JavaScript to any element that supports an event.
- **Avoiding Quote Restrictions:** Template literals (backticks) enable string construction without single or double quotes, permitting payloads even under strict filtering.

