We already have guide explaining [how to add Komodo assetchians in Agama Desktop](https://github.com/KomodoPlatform/Agama/wiki/Add-Komodo-Assetchains-in-Agama-Desktop-App). This guide will help you to add Bitcoin compatible coins into Agama desktop wallet. You have to edit the backend part and the UI part to add. Follow the guide carefully.

### Backend
- Add coin specific params to networks file [`https://github.com/KomodoPlatform/Agama/blob/dev/routes/electrumjs/electrumjs.networks.js`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/electrumjs/electrumjs.networks.js)
- Depending on a coin type you might need to add a coin to `isPoS` or `isZcash` helpers here [`https://github.com/KomodoPlatform/Agama/blob/dev/routes/shepherd/electrum/network.js`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/shepherd/electrum/network.js)
- Add an electrum server [`https://github.com/KomodoPlatform/Agama/blob/dev/routes/electrumjs/electrumServers.js`](https://github.com/KomodoPlatform/Agama/blob/dev/routes/electrumjs/electrumServers.js)
- Submit a PR

### UI:
- Add a coin to UI coin helper file [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/coinHelper.js#L9`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/coinHelper.js#L9)
- Add an asset chain to Add Coin component render [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/components/addcoin/addcoinOptionsCrypto.js#L19`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/components/addcoin/addcoinOptionsCrypto.js#L19)
- Drop a 100 x 100 px (better 200 x 200 px) logo into [`https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo`](https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo)
- Add an explorer [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/explorerList.js#L4`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/explorerList.js#L4)
- Submit a PR to dev branch on each repo

Please make sure an asset chain is working in Agama before making a commit. Pull requests containing partial information or not working assets/servers will remain unmerged until all requirements are fulfilled.