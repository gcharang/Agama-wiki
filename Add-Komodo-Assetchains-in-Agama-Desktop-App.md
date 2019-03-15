# Easy steps to add Komodo asset chain to Agama Desktop

The Agama desktop code comprises of two parts. Backend and UI. This assetchain adding guide will cover both. All the files needs changing are linked. If you want to add Bitcoin compatible coins follow [this guide](https://github.com/KomodoPlatform/Agama/wiki/Add-a-Bitcoin-Compatible-coin-to-Agama-Desktop).

### Backend
- Add a default asset chain port [`https://github.com/KomodoPlatform/Agama/blob/dev/routes/ports.js`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/ports.js)
- Add an electrum server for your asset (optional) [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/electrum-servers.js#L1`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/electrum-servers.js#L1)
- Add a fixed fee for your asset (required if you submit electrum servers list) [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/fees.js#L1`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/fees.js#L1)
- Add an asset chain to the list of kmd assets [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/coin-helpers.js#L1`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/coin-helpers.js#L1)
- Add asset chain params to this file [`https://github.com/KomodoPlatform/Agama/blob/dev/routes/chainParams.js`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/chainParams.js)
- Submit a PR, use dev branch!

### Asset chains with block rewards (optional)
- Add `genproclimit: true` property to allow mining with multiple CPU threads. Default value is 0 (e.g. -gen -genproclimit=0) in case genproclimit option is not explicitly specified.
[`https://github.com/KomodoPlatform/Agama/blob/dev/routes/chainParams.js`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/chainParams.js)

### UI
- Drop a 100 x 100 px (better 200 x 200 px) logo into [`https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo/btc`](https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo/btc)
- Add an asset chain explorer [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/coin-helpers.js#L51`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/coin-helpers.js#L51)
- Add asset chain name to coins translation file [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/translate/coins.js`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/translate/coins.js), look for "ASSETCHAINS".
- Submit a PR to dev branch on each repo

Please make sure an asset chain is working in Agama before making a PR. Pull requests containing partial information or not working assets/servers will remain unmerged until all requirements are fulfilled.