# Cosmos Wallet Registry

The wallet registry for the Cosmos Blockchain Ecosystem

## Wallet Data

Wallet data contains information needed to allow dApps to associate wallets with chains.

### Supported Chains

Supported chains must be registered to the [Cosmos Chain Registry](https://github.com/cosmos/chain-registry), and should be written exactly as defined in the Chain Registry (as folder name or `chain_name`). E.g., use `'cosmoshub'`, not `'Cosmos Hub'`.

A wallet provider only needs a single file if the list of supported chains is identicial on all platforms, but may instead need to create multiple files, one for each platform with a unique set of supported chains. E.g., since Keplr's browser extensions support a different set of chains than their mobile apps support, they instead have two files: _keplrextension.json_ and _keplrmobile.json_, each defining a different set of supported chains.

### Features

The 'features' array contains allows a limited set of features to be defined:
- suggest-chain:  referes to an experimental suggest chain feature. E.g., See Keplr's: https://docs.keplr.app/api/suggest-chain.html
- get-supported-chains: a feature that returns a list of chains supported by the wallet.

### Platforms

A platform object is defined by several properties:
- `device`: (desktop, mobile, tablet, other)
- `type`: (application vs extension)
- `platform` (the system on which the software runs): (ios, android, chrome, firefox, otherOS, otherBrowser)

The `install_link` is optional, but is a good way to confirm to users they've found the correct installation. Try to avoid language-specific url parameters in the URL.

### Example

Here is an example wallet entry:

```
{
  "$schema": "../wallet.schema.json",
  "wallet_name": "keplrmobile",
  "pretty_name": "Keplr",
  "website": "https://www.keplr.app/",
  "git_repo": "https://github.com/chainapsis/keplr-wallet",
  "supported_chains": [
    "cosmoshub",
    "osmosis"
  ],
  "features": [
    "suggest_chain",
    "icns"
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
*note: this is not Keplr mobile's actual entry*
