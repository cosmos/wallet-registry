# Cosmos Wallet Registry

The wallet registry for the Cosmos Blockchain Ecosystem

## Wallet Data

Wallet data contains information needed to allow dApps to associate wallets with chains.
For example, here is the schema for Keplr Wallet's browser extension:

```
{
  "$schema": "../wallet.schema.json",
  "wallet_name": "keplr mobile",
  "pretty_name": "Keplr",
  "website": "https://www.keplr.app/",
  "git_repo": "https://github.com/chainapsis/keplr-wallet",
  "supported_chains": [
    "cosmoshub",
    "osmosis"
  ],
  "features": [
    "suggest_chain",
    "get_supported_chains"
  ],
  "platforms": [
    {
      "device": "mobile",
      "type": "application",
      "platform": "ios",
      "install_link": "apple/app-store.com/cryptowallet",
    },
    {
      "device": "mobile",
      "type": "application",
      "platform": "android",
      "install_link": "google/play-store.com/cryptowallet",
    }
  ]
}
```
