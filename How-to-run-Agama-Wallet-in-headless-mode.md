Start Agama Wallet with the following params `./agama nogui coins=kmd,chips userpass="1234" seed="some passphrase"`. This will start Agama in headless (no gui) mode, load 2 coins in spv mode and login with the seed "some passphrase". After that you can use curl or similar lib to interface with Agama's API.

**userpass** param is optional

Using similar command you can also enable gui `./agama nogui=1 coins=kmd,chips userpass="1234" seed="some passphrase"`