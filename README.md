# Cosmos Wallet Registry

The wallet registry for the Cosmos Blockchain Ecosystem

## Wallet Data

Wallet data contains information needed to allow dApps to associate wallets with chains.
For example, here is the schema for Keplr Wallet's browser extension:

```
{
  "$schema": "../wallet.schema.json",
  "wallet_name": "keplrextension",
  "pretty_name": "Keplr Wallet (Browser Extension)",
  "website": "https://www.keplr.app/",
  "platforms": [
    "chrome",
    "firefox"
  ],
  "install_links": {
    "chrome": "https://chrome.google.com/webstore/detail/keplr/dmkamcknogkgcdfhhbddcghachkejeap?hl=en"
    "firefox": "https://addons.mozilla.org/en-US/firefox/addon/keplr/"
  },
  "has_suggest_feature": true,
  "supported_chains": [
    "cosmoshub",
    "osmosis"
  ]
}
```
