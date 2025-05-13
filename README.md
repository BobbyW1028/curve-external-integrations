# Curve Integrations

This repository's configuration files contain all metadata for apps and tools listed on https://curve.finance/dex/ethereum/integrations/

**Definition:** A Curve integration is a project that builds on top of Curve, and as a result extends what Curve users can do. E.g. using Curve LP tokens as collateral for anything, stats or information about Curve and its ecosystem, third-party front-ends…

## Integration metadata structure

Each integration's metadata must have the following properties:

- `name`: Name of the app/tool
- `description`: One-sentence description, not too long
- `imageId`: Filename of the app/tool's logo in the [`curve-assets` repo](https://github.com/curvefi/curve-assets/tree/main/platforms)
- `appUrl`: Link to the app/tool's webpage, or `null`
- `twitterUrl`: Link to the app/tool's Twitter profile, or `null`
- `tags`: Array of relevant tags (any of the tags ids listed here: [`integrations-tags.json`](https://github.com/curvefi/curve-external-integrations/blob/main/integrations-tags.json))
- `networks`: Array of relevant networks

Example:

```json
{
  "name": "Curve Trading Bots",
  "description": "Decentralized Curve Trading Bots allows to create limit orders, stop losses, and automated traded on Curve AMMs",
  "imageId": "curve-trading-bots.png",
  "appUrl": null,
  "twitterUrl": null,
  "tags": ["bots"],
  "networks": ["ethereum"]
}
```

## Adding an integration to the list

Conditions the project must meet in order to be added to the list of integrations:

1. It must fit the ["Curve integration" definition](https://github.com/curvefi/curve-external-integrations/tree/main#curve-integrations)
2. It must be live

Easy two-step process for your app/tool to appear on Curve's websites:

1. You'll need to upload the app/tool's logo to the [`curve-assets` repo](https://github.com/curvefi/curve-assets/tree/main/platforms) (submit a PR there, we'll be notified and will review and merge it). Either an SVG image, or a PNG/JPG of at least 200x200 and at most 500x500 px.
2. Submit a PR in this very repository, adding the app/tool's metadata as described above in the [`integrations-list.json`](https://github.com/curvefi/curve-external-integrations/blob/main/integrations-list.json) file. You don't have to wait for (1) to be merged to do this. We'll also be notified and will review and merge your PR. *Please provide a very short explanation of how the submitted project fits into the ["Curve integration" definition](https://github.com/curvefi/curve-external-integrations/tree/main#curve-integrations), if it isn't immediately obvious from the project's metadata in your PR.*
