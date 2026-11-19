---
name: wigoo
description: Help a traveler with Wigoo, the AI travel companion. Today the tools cover mobile data abroad (travel eSIMs for 190+ countries and regions: networks, data, validity, price in the traveler's currency and the link to buy). Use when the user is planning a trip abroad and asks about mobile data, roaming or an eSIM, or whether their phone will work there.
---

# Wigoo

Wigoo is an AI travel companion. Today its MCP server covers mobile data abroad with travel eSIMs; trip planning and more travel services will be added to the same server. Use the tools the server lists, not this page, to know what is available. The MCP server at `https://api.getwigoo.com/api/mcp` is a read-only catalog: it needs no account and no key, and it never places orders.

## How to help a traveler

1. `search_destinations` with the country or region they are going to.
2. `get_destination` for what it offers (networks, data sizes, validity, unlimited day passes, top ups), or `list_plans` for the plans on sale.
3. Pick the plan that fits the trip: days of travel, how much data they use, one country or several.
4. `get_quote` for that plan, in the traveler's currency. It returns the price and the link where they buy.

Give the link as it comes back. The page opens on that plan, and the traveler pays there: an email address is enough, no Wigoo account is needed.

## Things to keep in mind

- Prices are list prices. The amount charged is calculated at checkout, in the buyer's currency.
- A regional plan covers several countries with one eSIM: offer it when the trip crosses borders.
- The phone must support eSIM and be carrier unlocked.
- Do not ask for personal data. Nothing here needs it.

## Reference

- [Docs](https://docs.getwigoo.com/mcp)
- [Tools](https://docs.getwigoo.com/mcp/tools)
