# awsome-keep-network
A curated list of keep-network related resources. Made by a community member tian7.eth#5457

## Official site
- [Keep-network official site](https://keep.network)
- [tBTC official site](https://tbtc.network/)
- [tBTC dapp](https://dapp.tbtc.network/)
- [Dashboard for staking](https://dashboard.keep.network)
- [Keep-network whitepaper](https://backend.keep.network/whitepaper).[Source code](https://github.com/keep-network/whitepaper).
- [tbtc whitepaper](https://docs.keep.network/tbtc/index.html).

## Mainnet Contracts
Excerpt from [Mainnet v1.1.0 release](https://github.com/keep-network/tbtc/releases/tag/solidity%2Fv1.1.0).

- [TBTCSystem](https://etherscan.io/address/0xe20a5c79b39bc8c363f0f49adcfa82c2a01ab64a) is the tBTC system contract. It captures the current governable parameters, like collateralization thresholds, available lot sizes, and Keep configurations, and mediates access to Maker's ETHBTC Medianizer for the remainder of the system. All events related to tBTC are
- [VendingMachine](https://etherscan.io/address/0x526c08E5532A9308b3fb33b7968eF78a5005d2AC) is the tBTC contract responsible for taking ownership of deposits and minting the TBTC token in exchange, as well as making those deposits available for withdrawal by anyone who can pay back the requisite TBTC. Deposits owned by the vending machine (indicated by the vending machine's ownership of their associated tBTC Deposit Token)
- [DepositFactory](https://etherscan.io/address/0x87EFFeF56C7fF13E2463b5d4dCE81bE2340FAf8b) is the factory contract that creates new deposits. Its createDeposit function is the only way to create new deposits.
- [Deposit](https://etherscan.io/address/0xCffDCB12b74bE900e2020B9D96D256F1fEA96342) is the base contract for new deposit contracts. DepositFactory clones this contract for each new deposit, pulling the current parameters from TBTCSystem. Once a deposit is created, all of its parameters except for ETHBTC price are fixed forever.
- [TBTCDepositToken](https://etherscan.io/address/0x10B66Bd1e3b5a936B7f8Dbc5976004311037Cdf0) is an ERC721 non-fungible token, each instance of which is uniquely associated with a deposit. Ownership of this token indicates ownership of the associated deposit, which provides an exclusive right to redeem the underlying deposit's Bitcoin UTXO until the deposit reaches its 6-month term.
- [FeeRebateToken](https://etherscan.io/address/0xaf3fFF06b75f99352d8C2a3C4beF1339a2f94789) is an ERC721 non-fungible token that represents a claim to a rebate on the signing fee for depositors who exchange their deposit to mint fungible TBTC tokens. These depositors have the signing fee for their deposit escrowed at minting time, but if the deposit is redeemed before the end of its 6 month term, they are reimbursed that escrowed amount.
- [TBTCToken](https://etherscan.io/address/0x8dAEBADE922dF735c38C80C7eBD708Af50815fAa) is the ERC20 TBTC token. 18 decimals of precision packed into a beautiful 1-to-1 BTC backed token.

## Program
### PFK
- [September pfk announcement](https://blog.keep.network/what-james-prestwich-is-looking-for-in-septembers-playing-for-keeps-7a980d9520b0 )
- [pfk awards winners every month](https://pfkawards.com/). Made by Gregory#6997
- [August pfk record with google excel](https://docs.google.com/spreadsheets/d/1zZHukNvJJxAqwWcRqU4qq2uBaRjVfdCTsfqt2G-33mQ/edit#gid=0). Mady by mrHat#5983

### Stakedrop
- [Keep network stakedrop](https://medium.com/@chdru/keep-network-stakedrop-3e63355a18ec). Made by chandru#2037

## Staking
- [Official staking documents](https://keep-network.gitbook.io/staking-documentation/). Including stake KEEP at keepnetwork and stake ETH at tBTC.
- [tBTC risk - liquidation and slashing details](https://hackmd.io/OzIeyWcfTVO69zIF67XCkg). Made by ssh#4098
- [KeepStakedropRisks](https://hackmd.io/@LayerState/KeepStakedropRisks). Made by state#5254

## Run random beacon nodes and ecdsa nodes
- [Official tutorial about running random beacon](https://github.com/keep-network/keep-core/blob/master/docs/run-random-beacon.adoc)
- [A tool](https://keeptools.org/) about how to run nodes and some github repositories.[Source code](https://github.com/kferretcrypto/keep-tools). Made by kferret#5310
- A [detailed guide](https://medium.com/@nickgrego/step-by-step-guide-for-installing-both-ecdsa-beacon-nodes-on-vps-with-100-voucher-db930ab2a667) using Vultr as a vps. Made by Besides using infura ethereum nodes mentioned at step 5, you can also use a public nodes running by community members(Danil Ushakov #5735 and whataday2day #1271).
```
URL = "wss://ropsten.pfk2020.top/wss"
URLRPC = "https://ropsten.pfk2020.top/rpc"
```
## FAQ
- [About staking](https://keep-network.gitbook.io/staking-documentation/help/faq)
- [tBTC question](https://tbtc.network/faq)

## Statics of keep-network
- [tBTC and KEEP token dashborad made with duneanalytics](https://explore.duneanalytics.com/dashboard/tbtc)
- [A website of KEEP token dashboard](https://keepexplorer.com/), the data comes from [thegraph](https://thegraph.com/explorer/subgraph/suntzu93/keepnetwork).
- [Another website of KEEP token dashboard](https://keep-explorer.herokuapp.com/keep/blocks). It shows more metrics about keep token such as grants data.

## Competitor
- [wBTC](https://wbtc.network/)
- [renBTC](https://bridge.renproject.io/)
- [tBTC vs wBTC](https://medium.com/@yurataro2055/btc-on-ethereum-tbtc-vs-wbtc-317edf1da79f)
- [tBTC vs renBTC](https://telegra.ph/High-level-differences-between-renBTC-and-tBTC-05-26)

## Community
- [discord](https://discordapp.com/invite/wYezN7v)
