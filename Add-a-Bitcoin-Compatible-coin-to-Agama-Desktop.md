We already have guide explaining [how to add Komodo assetchians in Agama Desktop](https://github.com/KomodoPlatform/Agama/wiki/Add-Komodo-Assetchains-in-Agama-Desktop-App). This guide will help you to add Bitcoin compatible coins into Agama desktop wallet. You have to edit the backend part and the UI part to add. Follow the guide carefully.

### Backend
- Add network params [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/bitcoinjs-networks.js`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/bitcoinjs-networks.js). Make use of isPoS or isZcash flags if applicable in your case.
- Add an electrum server [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/electrum-servers.js#L1`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/electrum-servers.js#L1)
- Add a safe fixed fee (per transaction) [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/fees.js#L1`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/fees.js#L1).
- Add an explorer [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/coin-helpers.js#L62`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/coin-helpers.js#L62)
- Submit a PR

### UI
- Drop a 100 x 100 px (better 200 x 200 px) logo into [`https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo`](https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo)
- Add your coin name to EN translation file [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/translate/en.js`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/translate/en.js), look for "CRYPTO".
- Add your coin to coins helper file [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/coinHelper.js#L300`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/util/coinHelper.js#L300).
- Submit a PR to dev branch on each repo

### How to get network params
- pubKeyHash: https://github.com/KomodoPlatform/komodo/blob/fbb3b3e9a0c432173a8d733ebbcbd7b0324d58df/src/chainparams.cpp#L169
- scriptHash: https://github.com/KomodoPlatform/komodo/blob/fbb3b3e9a0c432173a8d733ebbcbd7b0324d58df/src/chainparams.cpp#L170
- wif: https://github.com/KomodoPlatform/komodo/blob/fbb3b3e9a0c432173a8d733ebbcbd7b0324d58df/src/chainparams.cpp#L171
- bip32 public: https://github.com/KomodoPlatform/komodo/blob/fbb3b3e9a0c432173a8d733ebbcbd7b0324d58df/src/chainparams.cpp#L172
- bip32 private: https://github.com/KomodoPlatform/komodo/blob/fbb3b3e9a0c432173a8d733ebbcbd7b0324d58df/src/chainparams.cpp#L173

If you can't find chainparams.cpp in your code base try checking one of these files https://docs.komodoplatform.com/barterDEX/get-listed-barterDEX.html#search-for-the-information-on-github.

Please make sure an asset chain is working in Agama before making a commit. Pull requests containing partial information or not working assets/servers will remain unmerged until all requirements are fulfilled.