# Easy steps to add ERC20 token to Agama Desktop

The Agama desktop code comprises of two parts. Backend and UI. This ERC20 adding guide will cover both. All the files needs changing are linked.

### Backend
- Add a contract ID [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/eth-erc20-contract-id.js`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/eth-erc20-contract-id.js)
- Add token decimals (optional, only if it's different from default 18 value) [`https://github.com/pbca26/agama-wallet-lib/blob/dev/src/eth-erc20-decimals.js`](https://github.com/pbca26/agama-wallet-lib/blob/dev/src/eth-erc20-decimals.js)
- Submit a PR

### UI
- Drop a 100 x 100 px (better 200 x 200 px) logo into [`https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo/eth`](https://github.com/KomodoPlatform/EasyDEX-GUI/tree/dev/react/src/assets/images/cryptologo/eth)
- Add ERC20 token name to coins translation file [`https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/translate/coins.js#L183`](https://github.com/KomodoPlatform/EasyDEX-GUI/blob/dev/react/src/translate/coins.js#L183), look for "CRYPTO".
- Submit a PR to dev branch on each repo

### How to get required contract info
Search for your token on Etherscan.io or use a direct link with your contract ID

example: https://etherscan.io/token/0x5ca9a71b1d01849c0a95490cc00559717fcf0d1d

After you open the page you should see number of decimals used for a contract.

Please make sure an asset chain is working in Agama before making a commit. Pull requests containing partial information or not working assets/servers will remain unmerged until all requirements are fulfilled.