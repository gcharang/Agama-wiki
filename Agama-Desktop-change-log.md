v0.36
- kv spv
- native -gen param
- spv watchonly address mode ui flag
- interest calc edge case fix
- improved seed encrypt, thanks to luke
- new ac chain
- tools -> get multiple kmd balances
- experimental support for custom asset chains, staking and mining

v0.35
- updated electrum servers
- spv 0 conf timestamp fix
- new coin bcbc
- new asset chain glxt
- spv shielded tx decoding fix
- seed storage pin rename/delete
- disable nn voting ui

v0.34
- load gui content from file instead of a remote url
- better seed gen (bip39)
- updated btc, dgb, zec spv servers

v0.33
- seed storage related bug fixes
- komodod update

v0.32
- bntn, eql asset chains
- custom seed entropy check
- send form multisig address validation bug fix
- encrypted seed storage

v0.31
- enabled mesh asset chain back
- login form native shortcut 32 bit check
- z key import
- multi wif import
- send form multisig address validation fix
- spv listtransactions bug fix causing app to freeze
- spv updated sng electrum servers
- oot ac native fix

v0.30c
- spv sng coin
- spv btc fees local fallback, atomicexplorer.com url fixes
- security: rce, session token fixes
- added oot asset chain

v0.30b
- elections spv sendmany fix

v0.30a
- minor elections modal fixes
- fixed vote2018 ac, added ninja ac
- new spv coin dnr
- a few minor bug fixes related to login and spv connections

v0.29c
- removed fiat asset chains
- interest claim modal kmd fee info
- spv empty login fix

v0.29b
- seed trim login fix
- spv send form will feature fees/totals for all coins and kmd interest to be claimed if applicable

v0.29a
- spv caching
- ltc tx fee bump to 0.001 (100000 sats)

v0.28c
- better spv tx history categorization
- terminate rogue electrum connections

v0.28b
- btc spv
- extended explorers list

v0.28a
- app menu debug -> reset settings item
- wif 2 wif fix
- pub address validation
- spv beer, pizza, vote, qtum, btx, btcz, hodlc

v0.27d
- voting
- better decode error wording
- watchonly spv

v0.27c
- tools merge/split utxo
- audo's create seed verification method
- fiat balance

v0.27b
- btch icon change
- pizza, beer test coins

v0.27a
- login/create seed qr code scan/gen
- native send subtract fee fix
- spv send "all balance", "send to self" shortcut buttons
- new section "tools", a bunch of handy functions to do wif to wif / seed to wif conversion, get utxo list etc

v0.26c-d
- btch spv, mgv spv
- better tooltips
- spv broadcast error info
- send value fix
- coin tile spv update fix
- util explorer link fix
- sn coins spv fees switched to static
- spv export keys eror fix
- start screen changed

v0.26b
- kmd logo update
- coin tile badge pos change
- coin tile stop action render cond fix
- zcparams modal broken styling fix
- all refs to barderdex are removed from about section
- online/offline detection
- 3 new asset chains AXO, BTCH, ETOMIC, native only
- 2 more spv coins XMY and ZCL
- spv send now should include the exact error message if "unable to broadcast"

v0.26a
- coin tile actions refactored as a dropdown menu
- receive coin validate address option in address menu
- rpc to cli passphru

v.025f-j
- 17 new spv coins *experimental*
- spv export keys fix
- language selector *experimental*
- wif login update
- send form false positive validation error fix
- top right menu icon style change
- settings support tab moved to a separate section

v0.25d-e
- settings app info daemon ports list
- native wallet info network data
- add coin modal spv mode desciption
- add coin modal new coins dropdown
- close modals on esc or overlay click
- spv uncompressed wif key support

v0.25a-c
- settings bip39 key search, target audience ledger wallet users
- 32 bit os detect, fallsback to spv mode only
- spv is enabled by default
- kmd passive is hidden under experimental option
- connection error icon is suppressed during wallet rescan
- native subtract fee error toaster fix
- spv supernet, dex, bots, crypto, hodl, pangea, bet, mshark are unlocked
- iguana menu fixes, renamed lock/logout to soft logout/complete logout
- spv auto reconnect if server is unreachable, sockets connect timeout is set to 10s
- claim interest spinner
- windows sync workaround threshold is changed from 0-80% range to 0-30% range
- settings debug.log reader asset chain support
- send native hide ismine:false addresses
- claim interest added native change description
- shark -> mshark change
- dump z address key fix
- hide address export in spv

v0.24g
- claim interest button address check

v0.24f
- native claim interest success toaster address fix
- spv claim interest auto close on success
- spv claim interest fee subtract fix
- native import key modal wif visibility toggle
- spv logout / remove coin cache cleanup fix

v0.24e
- jumblr pause/resume
- send form txid copy btn, link to explorer
- claim interest modal native address dropdown, spv
- tx history / balance refresh spinner
- claim interest not fully synced native coin warning sign

v0.24d
- agama modes explained on startup window
- receive ismine:false toggle
- send / claim interest balance calc fix, discard any ismine:false utxo
- display max available balance on send validation err
- clean gen* files
- settings clear komodo/chain data folder
- catch coind exit

v0.24c
- spv random server select on add coin
- spv listtransactions zeroconf timestamp fix
- improved coind down modal, less intrusive
- komodod prints piped out into log files
- settings native wallet.dat fetch keys
- receive coin wif key copy button
- disable missing zcash params check if spv only coins

v0.24a/b
- mnz and kmd spv should work now
- spv wif login fix
- spv seed login fix, affected seeds containing non-latin chars
- spv lock
- spv logout
- remove coin
- coind detached mode
- coind down modal configurable threshold, workaround for false positives