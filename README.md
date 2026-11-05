# Webhook

Official **PeltyCMS** `provisioning` WASM addon (`provisioning-webhook`).

## Install

1. Open Pelty Admin → Addons → Marketplace
2. Set registry URL to `https://market.mythicalsystems.org/api/pelty/addons/registry.json`
3. Download **Webhook**

Marketplace: https://market.mythicalsystems.org/marketplace/product/provisioning-webhook  
Product ID (CI): `81`

## Develop

This repository is a git submodule of [MythicalLTD/PeltyCMS](https://github.com/MythicalLTD/PeltyCMS) at `extensions/addons/prov-webhook`.

```bash
# from the PeltyCMS monorepo
cargo xtask addons prov-webhook
```

## Release (Mythic Marketplace)

Same flow as [featherpanel-com/PterodactylPanelApi](https://github.com/featherpanel-com/PterodactylPanelApi):

1. Repo secrets: `MYTHIC_PRODUCT_ID`, `MYTHIC_RELEASE_TOKEN`
2. Repo variable: `ADDON_DIR=prov-webhook`
3. Actions → **Release Addon** → Run workflow

Publishes the packed `provisioning-webhook.zip` via `MythicalLTD/.github/actions/publish-release@v1` and creates a GitHub Release.
