# Easy steps to add Komodo asset chain to Agama Desktop

The Agama desktop code comprises of two parts. Backend and UI. This assetchain adding guide will cover both. All the files needs changing are linked. If you want to add Bitcoin compatible coins follow [this guide](https://github.com/KomodoPlatform/Agama/wiki/Add-a-Bitcoin-Compatible-coin-to-Agama-Desktop).

### Backend
- Add a default asset chain port [`https://github.com/KomodoPlatform/Agama/blob/dev/routes/ports.js`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/ports.js)
- Add an electrum server for your asset (optional) [`https://github.com/KomodoPlatform/Agama/blob/dev/routes/electrumjs/electrumServers.js`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/electrumjs/electrumServers.js)
- Add an asset chain to the list of kmd assets [`https://github.com/KomodoPlatform/Agama/blob/dev/routes/shepherd/electrum/network.js#L6`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/shepherd/electrum/network.js#L6)
- Submit a PR

### UI
- Add asset chain entries to this file https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/components/addcoin/payload.js#L45
- If you have your own seed server ip add it here https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/actions/actions/addCoin.js#L156
- Add an asset chain to UI coin helper file [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/coinHelper.js#L9`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/coinHelper.js#L9)
- Add an asset chain to Add Coin component render [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/components/addcoin/addcoinOptionsAC.js#L28`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/components/addcoin/addcoinOptionsAC.js#L28)
- Drop a 100 x 100 px (better 200 x 200 px) logo into [`https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo`](https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo)
- Add an asset chain explorer [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/explorerList.js#L4`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/explorerList.js#L4)
- Submit a PR

Please make sure an asset chain is working in Agama before making a commit. Pull requests containing partial information or not working assets/servers will remain unmerged until all requirements are fulfilled.