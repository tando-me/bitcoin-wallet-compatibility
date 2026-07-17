# URI Schemes
A collection of known URIs that Bitcoin Wallet apps register within mobile OS's as Launch Services.

> **Try it:** Open [uri-test.html](uri-test.html) on a mobile device to tap through every scheme below and verify which wallets open.

Early Bitcoin adopters tend to install and test many different bitcoin apps on their smartphones. On iOS this can become a problem as there is no *easy* way to choose a default app to handle requests from other apps for payments. For example App X presents the user with a button to "Pay Lightning Invoice" and when you click on it, it opens a default wallet that is associated within the OS to handle the ```lightning:``` URL. There is currently no way to change the default app on iOS. The user is stuck using whichever app most recently hijacked the URI handler for ```lightning:```.

MoneyBadger (fka CryptoConvert) figured out a solution for iOS to give users the ability to choose an installed app to handle clicking a specific URI (```lightning:```). See their working app: https://apps.apple.com/in/app/cryptoqr-pay/id1617778619

Apparently each app can register not just as a handler for ```lightning:``` but can also register domain specific URI for their wallet, so an app could register to handle a ```walletofsatoshi:lightning:``` URI as an example.

If you as an app developer know to look for these domain-specific URI's, you could give your users the ability to choose a default app when handling ```lightning:``` URIs. The only problem is that there is no known repository of all the domain-specific URI's that are in use by all of the different wallet apps, and so everyone is left guessing. This repo is an attempt to collect all known URIs for all wallets to that you can give your (iOS) users choices on which app they want to associate with lightning payments.

| App Name | android:scheme | iOS CFBundleURLSchemes |
|----------|----------------|------------------------------|
| [Alby Go](https://getalby.com/products/alby-go) | [alby:](https://github.com/getAlby/go/blob/5a0f24c0bedceedc0514e4a81af50ba78859f4fb/lib/link.ts#L8) | [alby](https://github.com/getAlby/go/blob/5a0f24c0bedceedc0514e4a81af50ba78859f4fb/lib/link.ts#L8) |
| [Amber App](https://amber.app/amberwallet) |  |  |
| [Aqua](https://aqua.net/) |  |  |
| [Bipa](https://bipa.app/) |  |  |
| [Bitkit](https://bitkit.to/) | [bitkit:lightning:](https://github.com/synonymdev/bitkit-android/blob/38018018248c8100e6ad204cc62d5b844ad67723/app/src/main/AndroidManifest.xml#L94) | [bitkit](https://github.com/synonymdev/bitkit-ios/blob/11ac9870b989be4f9380a2c8ff92d235fb76ed2a/Bitkit/Info.plist#L13) |
| [Bitnob](https://bitnob.com/) |  |  |
| [Blink](https://www.blink.sv/) | [blink:lightning:](https://github.com/blinkbitcoin/blink-mobile/blob/7c198065471dca9e94209e4145a081933455adca/android/app/src/main/AndroidManifest.xml#L62) | [blink](https://github.com/blinkbitcoin/blink-mobile/blob/7c198065471dca9e94209e4145a081933455adca/ios/GaloyApp/Info.plist#L43) |
| [Blitz](https://blitz-wallet.com/) | [blitz-wallet:](https://github.com/BlitzWallet/BlitzWallet/blob/14f918b9f887dd5d850c1adaa4d3546d9e595490/android/app/src/main/AndroidManifest.xml#L79) | [blitz-wallet](https://github.com/BlitzWallet/BlitzWallet/blob/14f918b9f887dd5d850c1adaa4d3546d9e595490/ios/BlitzWallet/Info.plist#L36) |
| [Blixt](https://blixtwallet.github.io/) | [blixtwallet:](https://github.com/hsjoberg/blixt-wallet/blob/48d2e67c69bc1961425324bbbd1fb23a2aedc62f/android/app/src/main/AndroidManifest.xml#L59) | [blixtwallet](https://github.com/hsjoberg/blixt-wallet/blob/48d2e67c69bc1961425324bbbd1fb23a2aedc62f/ios/BlixtWallet/Info.plist#L32) |
| [Blockstream Green](https://blockstream.com/green/) | [blockstream:lightning:](https://github.com/Blockstream/green_android/blob/master/androidApp/src/main/AndroidManifest.xml#L111) | [lightning](https://github.com/Blockstream/green_ios/blob/master/gaios/Info.plist#L56) |
| [Blue Wallet](https://bluewallet.io/) | [bluewallet:lightning:](https://github.com/BlueWallet/BlueWallet/blob/a466ebca42a184d770ff9fcc61f370a54561f66b/android/app/src/main/AndroidManifest.xml#L150) | [bluewallet](https://github.com/BlueWallet/BlueWallet/blob/a466ebca42a184d770ff9fcc61f370a54561f66b/ios/BlueWallet/Info.plist#L116) |
| [Breez](https://breez.technology/) | [breez:](https://github.com/breez/breezmobile/blob/970272b63f2e4de4213df3320452a30675a7b724/android/app/src/main/AndroidManifest.xml#L100) | [breez](https://github.com/breez/breezmobile/blob/970272b63f2e4de4213df3320452a30675a7b724/ios/Runner/Info.plist#L70) |
| [Cake Wallet](https://cakewallet.com/) |  |  |
| [CashApp](https://cash.app/) |  |  |
| [Coinos](https://coinos.io/) | [lightning:](https://github.com/coinos/coinos-ui/blob/8af38f7f4736beadf23b4a2c68b0b918a6cfeb0d/android/app/src/main/AndroidManifest.xml#L42) |  |
| [Electrum](https://electrum.org/) | [lightning:](https://github.com/spesmilo/electrum/blob/28bbb4bdda6ee1c17577bd63b49ecddc0f076149/contrib/android/bitcoin_intent.xml#L7) |  |
| [Fedi](https://www.fedi.xyz/) | [fedi:](https://github.com/fedixyz/fedi/blob/e29f732ede5ad735ca05c5c2282bee5e1e774307/ui/native/android/app/src/main/AndroidManifest.xml#L57) | [fedi](https://github.com/fedixyz/fedi/blob/e29f732ede5ad735ca05c5c2282bee5e1e774307/ui/native/ios/FediReactNative/Info.plist#L28) |
| [Flash](https://getflash.io/) | flash: | [flash](https://github.com/lnflash/flash-mobile/blob/2d053ba553bd552cf5bfc7dd91c6deb646ec4546/ios/LNFlash/Info.plist#L46C13-L46C18) |
| [Lexe](https://lexe.app) | [lightning:](https://github.com/lexe-app/lexe-public/blob/master/app/android/app/src/main/AndroidManifest.xml#L53) | [lightning](https://github.com/lexe-app/lexe-public/blob/master/app/ios/Runner/Info.plist#L37) |
| [Machankura](https://8333.mobi/) |  |  |
| [Minibits](https://www.minibits.cash) | [lightning:](https://github.com/minibits-cash/minibits_wallet/blob/main/android/app/src/main/AndroidManifest.xml#L36) |  |
| [Muun](https://muun.com/) | [muun:lightning:](https://github.com/muun/apollo/blob/91449f0b970cc096f46c2b4fd27bdb014eebad35/android/apolloui/src/main/AndroidManifest.xml#L179) | [muun](https://github.com/muun/falcon/blob/88b3389acb9c955c0cc252bd9bab7c632e920253/falcon/app/falcon/Info.plist#L32) |
| [Phoenix](https://phoenix.acinq.co/) | [phoenix:lightning:](https://github.com/ACINQ/phoenix/blob/57faa66d7dcfdb84dd6a87efb7b81e4f1368d7d6/phoenix-android/src/main/AndroidManifest.xml#L58) | [phoenix](https://github.com/ACINQ/phoenix/blob/57faa66d7dcfdb84dd6a87efb7b81e4f1368d7d6/phoenix-ios/phoenix-ios/Info.plist#L32) |
| [Primal](https://primal.net/) | [nostrnwc+primal:](https://github.com/PrimalHQ/primal-android-app/blob/bb63e6c5b646137eea64ebf95c75b91fc4086314/app/src/main/AndroidManifest.xml#L284C39-L284C54) | [primal](https://github.com/PrimalHQ/primal-ios-app/blob/52257cfa77fd0f9b82875829de86b65f2b92a0bd/Primal/Info.plist#L14) |
| [River](https://river.com/) |  |  |
| [Satoshi](https://satoshi.money/) |  |  |
| [ShockWallet](https://shock.network) | [lightning:](https://github.com/shocknet/wallet2/blob/master/android/app/src/main/AndroidManifest.xml#L38) |  |
| [Speed](https://www.speed.app/) |  |  |
| [Strike](https://strike.me/) | strike: | strike |
| [Tether Wallet](https://wallet.tether.io/) |  |  |
| [Volt](https://volt.finance) | [lightning:](https://github.com/Zero-1729/volt/blob/main/android/app/src/main/AndroidManifest.xml#L40) | [lightning](https://github.com/Zero-1729/volt/blob/main/ios/volt/Info.plist#L42) |
| [Wallet of Satoshi](https://www.walletofsatoshi.com/) | walletofsatoshi:lightning: | walletofsatoshi |
| [ZBD](https://zbd.gg/) |  |  |
| [Zeus](https://zeusln.app/) | [zeusln:](https://github.com/ZeusLN/zeus/blob/8285c4e9b17e70ee5d78d4eee3a3adb963040130/android/app/src/main/AndroidManifest.xml#L78) | [zeusln](https://github.com/ZeusLN/zeus/blob/8285c4e9b17e70ee5d78d4eee3a3adb963040130/ios/zeus/Info.plist#L32) |




See also:

https://developer.apple.com/documentation/coreservices/launch_services

https://docs.lightning.engineering/the-lightning-network/payment-lifecycle/understanding-lightning-invoices#uri-scheme

List of Lightning Wallets compiled from the following sources:

https://stacker.news/items/733538

https://x.com/SDWouters/status/1894407675158372433

https://nwc.dev/
