Personal desktop application for my own shopping on eBay.

It uses the Browse API to search for newly listed Xbox Series S consoles that match filters I set (price range, condition, keyword). When a matching listing appears, it notifies me so I can open the listing and decide whether to buy as a normal buyer.

Technical flow:
- Application OAuth token (client credentials)
- Browse API item_summary/search with filters
- Occasional getItem when shipping details are needed
- Local deduplication so the same listing is not alerted repeatedly
- Manual purchase only (no automated bidding or checkout)

Single-user, personal use only. No public website, no multi-user access, no selling of eBay data. I do not store eBay user personal information beyond item IDs needed to avoid duplicate alerts.

I am requesting a higher Browse API daily call limit because continuous search while the application is running approaches the default 5,000 calls/day.
