![GZW Items List](https://i.ibb.co/k2L3fX7V/repo.png)

# Grayzone Warfare Items - List

A brief description of what this project does and who it's for

Community-maintained price and image overrides for [GZW Items](https://gzwitems.com).

Some items on the [official Fandom Wiki](https://gray-zone-warfare.fandom.com/wiki/Loot) are missing a sell price or image. This repo fills those gaps. Once the Wiki adds the data, our overrides are automatically ignored, so the **Wiki always takes priority**.

## How to contribute

1. **Fork** this repo
2. **Edit** `price-overrides.json` (see format below)
3. **Open a Pull Request** - we'll review and merge it

### JSON format

Each entry is keyed by the item's **slug** (lowercase, hyphens instead of spaces):

```json
{
  "azart-p1-radio": {
    "price": 1000,
    "imageUrl": ""
  },
  "some-other-item": {
    "price": 500,
    "imageUrl": "https://i.imgur.com/example.png"
  }
}
```

| Field      | Required | Description                                |
| ---------- | -------- | ------------------------------------------ |
| `price`    | Yes      | Sell price as a number (no `$` sign)       |
| `imageUrl` | No       | Direct link to a PNG/JPG (leave `""` if none) |

### How to find the item slug

1. Go to the [Loot page](https://gray-zone-warfare.fandom.com/wiki/Loot), [Medical page](https://gray-zone-warfare.fandom.com/wiki/Medical), or [Ammunition page](https://gray-zone-warfare.fandom.com/wiki/Ammunition) on the Wiki
2. Find the item and note its **name**
3. Convert to a slug: lowercase, replace spaces and special characters with hyphens
   - Example: `AZART-P1 Radio` -> `azart-p1-radio`
   - Example: `Bottle of Water` -> `bottle-of-water`

> **Tip:** On [gzwitems.com](https://gzwitems.com), items missing a price show as **$???** — those are the ones that need overrides.

### Uploading an image (optional)

If the Wiki is also missing the item image, upload a screenshot to a free image host and use the direct URL:

- [imgur.com](https://imgur.com/upload) — upload, then right-click the image and copy the direct link
- [imgbb.com](https://imgbb.com/) — upload, then copy the "Direct link"

## Rules

- Keep the JSON valid — use a [JSON validator](https://jsonlint.com/) if unsure
- One item per key, no duplicate keys
- Prices should be the **vendor sell price** (what you get when selling to a trader)
- Don't add items that already have a price on the Wiki — they'll be ignored anyway

## Questions?

Join our [Discord](https://discord.gg/qRsN6S6JVk) if you need help or want to discuss contributions.