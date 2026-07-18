# LUD-09 successAction `url` Tag - Wallet Support

Does the wallet display the `successAction` URL (description + clickable link) to the user after a successful LNURL-pay payment?

Spec: [LUD-09](https://github.com/lnurl/luds/blob/luds/09.md)

## Tested

| Wallet | Should Support | Tested | Notes |
|--------|:--------------:|:------:|-------|
| [Alby Go](https://getalby.com/products/alby-go) | YES | Pass | Description + "Open Link" button |
| [Aqua](https://aqua.net/) | YES | Pass | successAction URL & description display after transaction and persist in transaction history |
| [Blink](https://www.blink.sv/) | YES | Pass | |
| [Blitz](https://blitz-wallet.com/) | YES | Pass | Opens URL in in-app WebView, tested by Blitz team |
| [Breez](https://breez.technology/) | YES | Pass | Tested with Misty Breez |
| [Phoenix](https://phoenix.acinq.co/) | YES | Pass | |
| [Wallet of Satoshi](https://www.walletofsatoshi.com/) | Unknown | Pass | Closed source |
| [Zeus](https://zeusln.app/) | YES | Pass | Description + clickable URL via `Linking` |
| [Blockstream Green](https://blockstream.com/green/) | YES | N/A | Has SDK model but UI doesn't support sending to Lightning addresses |
| [Cake Wallet](https://cakewallet.com/) | NO | N/A | No UI rendering of successAction; amount bug prevents send |
| [Primal](https://primal.net/) | YES | N/A | Uses Breez SDK, but payment errored during test |
| [River](https://river.com/) | Unknown | N/A | Unable to pay a Lightning address |
| [Bitkit](https://bitkit.to/) | NO | Fail | No LNURL code found in repo |
| [Bitnob](https://bitnob.com/) | Unknown | Fail | Closed source |
| [Blue Wallet](https://bluewallet.io/) | YES | Fail | Code exists but doesn't display in practice (via LNDHub) |
| [Coinos](https://coinos.io/) | Unknown | Fail | Web-based |
| [Fedi](https://www.fedi.xyz/) | NO | Fail | Doesn't parse successAction from response at all |
| [Flash](https://getflash.io/) | YES | Fail | Has Breez SDK but doesn't surface URL in UI |
| [Minibits](https://www.minibits.cash) | NO | Fail | Has LNURL-pay but never processes successAction |
| [Lexe](https://lexe.app) | NO | Fail | No successAction rendering; also errors on strict enforcement of description hash |
| [Strike](https://strike.me/) | Unknown | Fail | Closed source |
| [Evento](https://evento.so/) | Unknown | Fail | Web-based |
| [Tether Wallet](https://wallet.tether.io/) | NO | Fail | No successAction code found in WDK repo |

## Untested

| Wallet | Should Support | Notes |
|--------|:--------------:|-------|
| [Blixt](https://blixtwallet.github.io/) | YES | Description + URL link + Copy/Open buttons in code |
| [Bey Wallet](https://github.com/Bey-Wallet/BeyWallet) | NO | Cashu wallet with narrow LN-melt support. [lnurlService.ts](https://github.com/Bey-Wallet/BeyWallet/blob/main/src/services/lnurlService.ts) reads only `data.pr` from the LNURL callback; zero occurrences of `successAction` in the repo. Bech32 `LNURL1...` strings also unsupported |
| [Electrum](https://electrum.org/) | NO | No successAction handling in code |
| [Muun](https://muun.com/) | NO | No LNURL-pay code found |
| [ShockWallet](https://shock.network) | NO | Passes data through but no UI rendering |
| [Amber](https://amber.app/amberwallet) | Unknown | Closed source |
| [Bipa](https://bipa.app/) | Unknown | Closed source |
| [CashApp](https://cash.app/) | Unknown | Closed source |
| [Machankura](https://8333.mobi/) | Unknown | USSD can't display URLs, but also has WhatsApp UI and mobile apps that could |
| [Satoshi](https://satoshi.money/) | Unknown | Closed source |
| [Speed](https://www.speed.app/) | Unknown | Closed source |
| [Volt](https://volt.finance) | Unknown | No code found |
| [ZBD](https://zbd.gg/) | Unknown | Closed source |

## Summary

- **Pass (8):** Alby Go, Aqua, Blink, Blitz, Breez, Phoenix, Wallet of Satoshi, Zeus
- **Fail (11):** Bitkit, Bitnob, Blue Wallet, Coinos, Evento, Fedi, Flash, Lexe, Minibits, Strike, Tether Wallet
- **N/A (4):** Blockstream Green, Cake Wallet, Primal, River
- **Should support, untested (1):** Blixt
- **Should NOT support (6):** Bey Wallet, Cake Wallet, Electrum, Lexe, Muun, ShockWallet
- **Unknown (8):** Remaining closed-source or no-code-found wallets (includes Machankura)

## Last updated

2026-07-17
