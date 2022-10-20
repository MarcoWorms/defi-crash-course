# Decentralized Finance Crash Course

![](https://i.imgur.com/Huayq6T.png)

This guide is a summarized version of the [Finematics Guide to Decentralized Finance](https://finematics.com/guide-to-decentralized-finance/). **I am not the author of the original guides and I took many images from it**. I also used the guide progression structure, but I've included some extra concepts in between to make sure readers can go from zero to enlightenment about DeFi.

Most of the concepts had their initial description generated from [GPT-3 AI](https://beta.openai.com/playground) after feeding it with the full article from [Finematics](https://twitter.com/finematics) and asking for "a summary in layman terms". I then reviewed the texts with the help of [Grammarly](https://app.grammarly.com/) and added any extra details that might help with understanding the concept. It was a fun ride to make this and I hope it makes for a fun read!

If you like this content follow the original creator of all guides used to produce this summary:

- https://twitter.com/finematics
- https://www.youtube.com/c/finematics

And also follow me on Twitter as I'm always exploring and writing about DeFi, and more frequently about the [yearn](https://twitter.com/iearnfinance) protocol as I'm a contributor there:

- https://twitter.com/MarcoWorms

# Introduction to Blockchain Basics

DeFi happens mostly in blockchains so it's important to understand the tech history and basics:

- The first popular use of blockchain tech emerged with Bitcoin in 2009
- Bitcoin used the blockchain to build "decentralized money + ledger"
- This is what I mean by ledger: a table that counts how much money enters and leaves for each account: 
![](https://i.imgur.com/KkL9UOo.png)
- "Decentralized" in this context means anyone can use this product and anyone can also help run its infrastructure
    - anyone can be a user: a user can send some BTC to another user (there is a fee for every transaction)
    - anyone can be a miner: a miner participates in the process of validating user transactions (and receive transaction fees for it)
- So Bitcoin:
    - created a new type of money (BTC)
    - attached a ledger that can't be manipulated when transactions are settled
    - set up an incentive flow to make sure that people that run the infrastructure receive money for doing it, guaranteeing the safety of the network for the future
- But Bitcoin did not allow for [Smart Contracts](#Smart-Contracts-source) to happen
- Ethereum was launched in 2015
    - it was a bitcoin clone but it had smart contracts
    - the money it created is called ETH
    - every transaction, including interacting with smart contracts, has a fee charged in ETH (much like BTC has transaction fees)
- Since then Ethereum has been a very successful venture, DeFi has over $55b circulating inside its protocols ([DefiLLama source](https://defillama.com/)), and the value of all cryptocurrencies combined has already reached the magnitude of trillions ([CMC source](https://coinmarketcap.com/charts/))

# DeFi Novice

This is our first level which is perfect for beginners. If you have heard about decentralized finance before, but all of the concepts and terminology seem a bit overwhelming – this is where you start.

## What is Decentralized Finance? ([source](https://finematics.com/guide-to-decentralized-finance/))

![](https://i.imgur.com/SrIyP2o.png)

DeFi is a movement that aims to create a new financial system that is open to everyone and doesn’t require trusting intermediaries like banks. To achieve that DeFi relies heavily on cryptography, blockchain, and smart contracts.

DeFi ecosystem consists of multiple pillars, the main ones being Lending and Borrowing, Stable Coins, Decentralized Exchanges, Derivatives, Margin Trading and Insurance.

## DeFi Wallets ([source](https://finematics.com/top-3-defi-wallets-for-2021/))

![](https://i.imgur.com/NoZEbGT.png)

Wallets allow for sending, receiving, and storing cryptocurrency.

There are many DeFi-friendly wallets available on the market, each with its own set of features and pros and cons. The most popular options are Metamask, Ledger, and Argent:

- [Ledger](https://www.ledger.com/) is a hardware wallet that provides a high degree of security for users' digital assets. However, it requires a separate hardware device and it is not as convenient to use as other wallets. You can connect Ledger wallets to Metamask to use them in the browser.
- [Metamask](https://metamask.io/) allows users to interact with DeFi apps. Good for creating new "hot wallets" that don't keep funds all the time but can be used to test things without exposing your main wallet.
- [Argent](https://www.argent.xyz/) is a non-custodial mobile wallet integrated with multiple DeFi protocols. It uses a social recovery model that doesn't require a recovery phrase. 

It's worth mentioning two apps that make managing a DeFi portfolio easy: [Zapper](https://zapper.fi/) and [Zerion](https://zerion.io/).

Technically, a wallet is a pair of:
- A **public** key, known as your public address
- A **private** key, which whoever posses can act as the owner of the public address

And a good concept to have in mind is that nothing is inside your wallet. You tag things in the blockchain with your **public** address, and after they are tagged as yours only you can change the address by using your **private** key. All market wallets mentioned help you keep your private key secure, but the most common-sense advice today for any DeFi average user is: **use hardware wallets**.

![](https://i.imgur.com/WaRuf18.png)

## Smart Contracts ([source](https://finematics.com/smart-contracts-explained/))

![](https://i.imgur.com/PPzHFll.png)

Smart contracts are pieces of code that can be executed automatically and deterministically. The smart contract code is usually stored and executed on the blockchain to make it trustless and secure. Smart contracts also have capabilities of receiving, storing, and sending funds and even calling other smart contracts.

Smart contracts aim at removing the human factor from decision-making. The human factor is often proven to be the most error-prone and unreliable element of the standard, traditional contracts.

[Ethereum](https://ethereum.org/en/) is a good example of a blockchain that supports smart contracts and enables programmers to implement them. Smart contracts can be written in a programming language called Solidity which was created specifically for that purpose. In Ethereum, all the deployed smart contracts are immutable. This means that once deployed they cannot be modified. Smart contracts on Ethereum are also decentralized which means there is no single machine controlling the contract. Besides Solidity programmers can use other languages to make smart contracts in Ethereum like [Vyper](https://github.com/vyperlang/vyper) or [Huff](https://huff.sh/).

A smart contract in Ethereum is a wallet with built-in functions:

<img src="https://i.imgur.com/6qH5Wto.png" width="400"/>

Although Ethereum is currently the most popular general-purpose smart contract platform, it is not the only one with a few competitors. Some of them are [Solana](https://solana.com/), [Tezos](https://tezos.com/), [Tron](https://tron.network/), but not all share the same characteristics.

## ERCs ([source](https://ethereum.org/en/eips/))

Ethereum Request for Comments ([ERC](https://eips.ethereum.org/erc)) is a formal process for proposing improvements to the Ethereum network. It allows anyone to submit a proposal for how the network should be improved and then gives the community a chance to discuss the merits of the proposal and vote on whether or not to implement it. If an Improvement Proposal (EIP) gets enough support from the community it becomes an ERC.

### ERC20

The [ERC20](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/) standard defines a set of rules for how tokens on the Ethereum blockchain should be built. These rules include how the tokens can be transferred, how they are approved, and how data about the tokens is stored on the blockchain. The standard also defines how tokens interact with each other on the Ethereum blockchain. The ERC20 standard is used by most popular tokens, like USDC, USDT, DAI, CRV, YFI, UNI, SUSHI, and many others.

## Uniswap (Decentralized Exchanges) ([source](https://finematics.com/uniswap-uni-token-explained/))

![](https://i.imgur.com/JnvmANj.png)

[Uniswap](https://app.uniswap.org/#/swap) is a protocol for the decentralized exchange of tokens on the Ethereum blockchain. The Uniswap protocol is deployed as a set of smart contracts and it’s completely decentralized, permissionless, and censorship-resistant. Uniswap is built on the concept of [liquidity pools](#Liquidity-Pools-source) and automated market makers or, to be precise, a constant product market maker.

The first version of the protocol was launched on November 2, 2018. The protocol quickly gained a lot of traction which resulted in an initial seed investment that allowed Uniswap’s team to work on the second version of the protocol, which introduced the current implementation of liquidity pools used across many DeFi protocols.

## Lending and Borrowing ([source](https://finematics.com/lending-and-borrowing-in-defi-explained/))

![](https://i.imgur.com/QhLj9WZ.png)

Lending and borrowing can be done in DeFi completely decentralized and permissionless while maintaining full custody over your coins. In DeFi lending, operational fees are recalculated on every Ethereum blockchain state change, this provides variable interest rates that can change quite dramatically depending on the lending and borrowing demand for particular tokens. The amount that can be borrowed depends on 2 main factors:
- The first one is how much funds are available to be borrowed in a particular market
- The second one is what is the collateral factor of tokens supplied by the borrower

Collateral factor determines how much can be borrowed based on the quality of the collateral. If a user decides to borrow funds, the value of the borrowed amount must always stay lower than the value of their collateral provided times its collateral factor. If this condition holds there is no limit on how long a user can borrow funds. Two famous DeFi lending platforms are [AAVE](https://aave.com/) and [Compound](https://compound.finance/)

# DeFi Apprentice

At this level, you feel comfortable with all the concepts included at the DeFi Novice level and are ready to dive deeper into the future of finance!

## Stable Coins ([source](https://stablecoins.wtf/resources/the-relevance-of-stablecoins))

Stablecoins are tokens that claim to maintain 1:1 value with another one. Every stablecoin has to balance risks between:

- Decentralization (More centralized = More risk of frozen funds)
- Price stability (Unstable price defeats the purpose of the product and loses community trust)
- Expensiveness to mint (If it's too expensive all financial operations using this coin are more expensive)

There are roughly three types of stablecoins, each focusing more on some of the above problems:
- **Fiat-backed (Examples: [USDC](https://www.circle.com/en/usdc), [USDT](https://tether.to/), [BUSD](https://www.binance.com/en/busd)):** stablecoins are the most prominent and used form of stablecoins. They are backed 1:1 by real USD and require bank accounts to hold USD to back the stablecoin issuing. this operation can be replicated for any other asset, for example, wBTC is a stablecoin of BTC inside the Ethereum network so you can use BTC in DeFi operations. 
- **Crypto-backed (Example: [DAI](https://makerdao.com/en/), [MIM](https://abracadabra.money/), [LUSD](https://www.liquity.org/)):** stablecoins are backed by other digital assets such as BTC, ETH. Created through the [Lending and Borrowing](#Lending-and-Borrowing-source) operation
- **Algorithmic stablecoins (Example: [FRAX](https://frax.finance/)):** have implemented an algorithm balancing the supply and demand of the stablecoin to maintain price stability. 

## Liquidity Pools ([source](https://finematics.com/liquidity-pools-explained/))

<img src="https://i.imgur.com/FcfyOTW.png" width="600"/>

Liquidity Pools (LPs) are smart contracts that hold a certain amount of 2 different tokens and they enable users to exchange those tokens directly with each other. This process is completely decentralized, so there is no need for a centralized exchange that would normally hold the tokens and facilitate the trade.

Whenever a user wants to exchange one token for another, they simply go to a liquidity pool that holds those 2 tokens and perform a trade. The liquidity pool uses a special algorithm called an automated market maker (AMM) to determine the price of the tokens in the pool and facilitate trades. This whole process is usually pretty fast and it’s usually cheaper than using a centralized exchange.

Any user can become a liquidity provider by providing tokens to the pool in the same ratio as they currently exist, or they can also create a new LP by providing a new pair of tokens. If a pool has 10 ETH and 50,000 DAI for example it means that if I want to add 1 ETH I have also to add 5,000 DAI to become a provider for this pool. Providers receive part of the trading fees, another part goes to the [DEX](#Uniswap-Decentralized-Exchanges-source) protocol (for example [Uniswap](#Uniswap-Decentralized-Exchanges-source)) that allows liquidity providers to create the pools and users to search them to trade on.

Because liquidity pools are just smart contracts, they can be modified to hold more than 2 tokens or to have a different pricing algorithm that would work better with certain assets. This is what [Curve](https://curve.fi/) did, it optimized the LP algorithm for pools made of 2 stablecoins of the same asset, and so it became one of the most successful DeFi protocols.

## Impermanent Loss ([source](https://finematics.com/impermanent-loss-explained/))

Impermanent loss is a temporary loss of funds occurring when providing liquidity. It’s very often explained as a difference between holding an asset versus providing liquidity in that asset. Impermanent loss is usually observed in standard liquidity pools where the liquidity provider (LP) has to provide both assets in a correct ratio, and one of the assets is volatile in relation to the other, for example, in a Uniswap DAI/ETH 50/50 liquidity pool.

If ETH goes up in value, the pool has to rely on arbitrageurs (users that make profitable trades until the pool ratio matches the market prices) to continually ensure that the pool price reflects the real-world price to maintain the same value of both tokens in the pool. This leads to a situation where profit from the token that appreciated in value is taken away from the liquidity provider. At this point, if the LP decides to withdraw its liquidity, the impermanent loss becomes permanent.

![](https://i.imgur.com/bmUE5M4.png)

## Yield Farming ([source](https://finematics.com/yield-farming-explained/))

Yield Farming, in essence, is a way of trying to maximize a rate of return on capital by leveraging different DeFi protocols. Yield farmers try to chase the highest yield by switching between multiple different strategies. The most profitable strategies usually involve at least a few DeFi protocols like Compound, Curve, Synthetix, Uniswap, or Balancer. If the strategy doesn’t work or if there is a better strategy available the yield farmers move their funds around. They may, for example, move the funds between different protocols or swap some of their coins for other ones that are currently generating more yield. In the yield farming world, this procedure is sometimes called crop rotation.

![](https://i.imgur.com/lWroYNw.png)

## Yearn Finance and YFI Token ([source](https://finematics.com/yearn-finance-and-yfi-explained/))

[yearn.finance](https://yearn.finance/#/portfolio) is a [yield farming](https://hackmd.io/J7kGRZNDT7KHAhy0l2fh7Q#Yield-Farming-source) optimizer that automates the process of choosing the highest paying lending protocols for your stablecoins in version 1. The protocol allows you to deposit your stable coins into a pool and receive a yield-bearing version called yvToken. Today version 2 allows for multiple different yield strategies for each vault.

[YFI](https://etherscan.io/token/0x0bc529c00c6401aef6d220be8c6ea1667f6ad93e) is the governance token for the [yearn protocol](https://docs.yearn.finance/getting-started/intro). It was distributed to the users of the protocol it used to decide on the future of the protocol. Today yearn is maintained by a group of people worldwide with no centralized leadership, governed by the YFI token. 

![](https://i.imgur.com/xRwHpVU.png)

### Yearn Vaults: ETH Vault Explained ([source](https://finematics.com/yearn-vaults-eth-vault-explained/))

In summary, the Yearn ETH Vault generates yield by borrowing DAI from MakerDAO and using it to provide liquidity to the Curve Y pool. This results in getting rewarded with CRV tokens that are then sold for ETH. The ETH is then used to pay the gas fees and the interest on the DAI loan. The rest of the ETH is then reinvested into the Vault.

![](https://i.imgur.com/wTOC4EM.png)

# DeFi Master

Concepts included in DeFi Novice and DeFi Apprentice seem to be easy for you. Time to bring your skills to the next level.

## Flash Loans ([source](https://finematics.com/flash-loans-explained/))

![](https://i.imgur.com/Khhg1YW.png)

A flash loan is a feature that allows you to borrow any available amount of assets from a designated smart contract pool with no collateral. Flash loans are useful building blocks in DeFi as they can be used for arbitrage, swapping collateral, and self-liquidation.

Flash loans, although initially introduced by the Marble protocol, were popularised by [Aave](https://aave.com/) and [dYdX](https://dydx.exchange/). 

The most important part of executing a flash loan is to find a flash loan provider. Projects such as Aave or dYdX developed smart contracts that allow DeFi users to borrow different coins from a designated pool under the condition that they are repaid within the same Ethereum transaction. There is usually a fixed cost associated with using flash loans.

Once the amount is borrowed from the lending pool it can be used for any other arbitrary actions assuming that at the end of the chain of different steps, the initial flash loan is repaid.

There are 3 most common use cases for flash loans: arbitrage, collateral swap, and self-liquidation.

Flash loans, similar to crypto, can be used for both good and bad. Regarding the latter, flash loans were used in the most recent DeFi hacks and allowed hackers to magnify their potential profits as they do not require any upfront funds.

Although flash loans are predominantly used by developers, it is also possible to use them without doing any coding. Projects such as [Collateralswap](https://collateralswap.com/), [Defisaver](https://defisaver.com/) or [Furucombo](https://furucombo.app/) make it possible.

## Vampire Attacks: Sushi Case ([source](https://finematics.com/vampire-attack-sushiswap-explained/))

<img src="https://i.imgur.com/jtxhXLi.png" width="200"/>

Used by [SushiSwap](https://www.sushi.com/) to attract over $1B of liquidity in less than a week, a vampire attack is a way to incentivize liquidity providers of one platform to move their liquidity to another platform. This is done by offering high rewards for staking LP tokens to the new platform and migrating the staked tokens to the new platform.

Vampire attacks are a very powerful tool for launching a new project, especially a new DeFi project. They create strong incentives for liquidity providers to move their liquidity to a new platform. The concept is very simple yet very effective.

The problem with vampire attacks is that they are very aggressive and create a lot of FOMO, which can quickly lead to a loss of trust in the community.

## Ampleforth ([source](https://finematics.com/ampleforth-explained/))

Ampleforth is a cryptocurrency with a unique feature – its supply is elastic and can change daily while the ownership of the AMPL tokens is never diluted. To achieve this the Ampleforth protocol uses 2 price oracles and a set of algorithms that can automatically change the total supply of AMPL to seek price equilibrium.

![](https://i.imgur.com/ROaGFaZ.png)

Ampleforth aims at diversifying cryptocurrency portfolios by being less correlated to the price of Bitcoin compared to other cryptocurrencies. In the medium term, it aims at being used as collateral in DeFi protocols. The long-term goal for Ampleforth is to create an alternative to central-bank money that is adaptable to shocks.

## NFTs in Defi ([source](https://finematics.com/what-are-nfts-and-how-can-they-be-used-in-defi/))

NFTs are a type of cryptographic token that can represent ownership of digitally scarce goods such as pieces of art or collectibles like game items. They are non-fungible, which means each unit is not interchangeable and has different properties. NFTs are provably scarce and indivisible.

NFTs can be implemented on any blockchain that supports smart contract programming, but the most popular examples are [ERC-721](https://eips.ethereum.org/EIPS/eip-721) and [ERC-1155](https://eips.ethereum.org/EIPS/eip-1155) standards on Ethereum.

In economics, fungibility is the characteristic of goods or commodities where each unit is interchangeable and indistinguishable from each other.

![](https://i.imgur.com/iauRPTX.png)

- **Unique** – each NFT has different properties usually stored in the token’s metadata.
- **Provably Scarce** – there is usually a limited number of NFTs with an extreme example of having only 1 copy, the number of tokens can be verified on the blockchain, hence its provability.
- **Indivisible** – most NFTs cannot be split into smaller denominations, so you cannot buy or transfer a fraction of your NFT, but you can create a derivative asset that represents a fractionalized NFT.

In the world of DeFi, NFTs can be used as collateral for loans. However, this is not without its challenges, as the markets for particular NFTs can be very illiquid, making it difficult to accurately value the collateral.

## Layer 2 Scaling ([source](https://finematics.com/ethereum-layer-2-scaling-explained/))

<img src="https://i.imgur.com/uKGFGIb.png" width="400"/>

Layer 2 is a very broad concept and we can expect many new projects to pop up soon. As the adoption of Layer 2 solutions grows, we can expect to see many more new applications being built on Ethereum. One of the main reasons for that is the increased composability that Layer 2 solutions provide.

With the increased scalability, we can also expect the gas fees to go down. This is an important factor as it will allow Ethereum to be used by a wider audience and not just by the most wealthy members of the community.

There are different types of layer 2 solutions:

- **Channels** allow participants to exchange their transactions off-chain several times while only submitting two transactions to the base layer.
- **Plasma** is a Layer 2 scaling solution originally proposed by Joseph Poon and Vitalik Buterin. It allows for off-chain decentralized apps.
- **Sidechains** are Ethereum-compatible, independent blockchains with their consensus models and block parameters.
- **Rollups** provide scaling by bundling or “rolling up” sidechain transactions into a single transaction and generating a cryptographic proof, also known as a SNARK (succinct non-interactive argument of knowledge). Only this proof is submitted to the base layer.

| Solution | Interoperable with Ethereum | Can be used for general-purpose smart contracts? | Open participation* |
| :--- | :--- | :--- | :--- |
| **Channels** | Yes | No | No |
| **Plasma** | Yes | No | Yes |
| **Sidechains** | Yes | Yes | Yes |
| **Rollups** | Yes | Yes | Yes |

**Open participation means that anyone can join and use the network without having to be known upfront to the other participants.*

## Curve ([source](https://resources.curve.fi/))

<img src="https://i.imgur.com/19lxrJN.png" width="400"/><br/>

[Curve Finance](https://curve.fi/) is a decentralized exchange for cryptocurrency trading that focuses on efficient stablecoin trading. Curve’s focus on stablecoins allows investors to avoid more volatile crypto assets.

It is an automated market maker (AMM) that maintains low fees and slippage through the use of [liquidity pools](#Liquidity-Pools-source).

Like [Uniswap](#Uniswap-Decentralized-Exchanges-source), tokens can be swapped as long as there is liquidity. The main difference between Curve and other DEXes is that Curve focuses mainly on stable assets. Curve offers many stablecoins including DAI, USDT, USDC, BUSD, and TUSD.

The Curve Finance protocol also contains the Curve token known as CRV. It is mainly used to incentivize liquidity providers on their platform and to get as many users as possible involved in the protocol's governance.

The amount of liquidity Curve provides allows other DeFi applications to use Curve pools as part of their ecosystem. Applications like Yearn Finance and Compound use Curve as a farming solution in their ecosystem.

An advantage of using Curve is that it minimizes slippage. Slippage refers to the difference in the price of an asset between the time you submit the transaction and the time the transaction is validated on the blockchain.

Today Curve holds about $6b liquidity inside its contracts.

## Convex ([source](https://docs.convexfinance.com/convexfinance/))

<img src="https://i.imgur.com/L52LD2p.png" width="400"/><br/>

Convex Finance is a platform that allows users to optimize their liquidity on Curve Finance and earn boosted rewards in the form of CRV tokens.

Curve uses a governance mechanism that revolves around veCRV: a locked version of CRV, and to maximize yields users have to lock their CRV for 4 years. But many want to exit before and so the Convex solution was shortly like this: everyone deposits their CRV on convex, convex stakes everything together maximizing yields and boosts existing in the Curve protocol, and in exchange, users get cvxCRV which is like a tradeable version of veCRV.

Today Convex holds about $4b liquidity inside its contracts.

# The End?

Awesome! If you managed to complete all the levels – congrats! You are now a DeFi Master. There is not a lot of time to celebrate though. Decentralized finance moves fast and there are always new things to learn. 

To stay up to date and learn even more about decentralized finance, make sure you subscribe to the [Youtube (Finematics)](https://www.youtube.com/c/finematics) channel and follow on [Twitter @finematics.eth](https://twitter.com/finematics).

And also follow me on [Twitter @MarcoWorms](https://twitter.com/MarcoWorms) as I'm always exploring and writing about DeFi, and more frequently about the yearn protocol in the [Yearn Blog](https://medium.com/iearn) and [Yearn Docs](https://docs.yearn.finance/).

## Resources

Below are glossaries and other resources to help you navigate DeFi:

- [yearn defi glossary](https://docs.yearn.finance/resources/defi-glossary)
- [yearn defi strategies descriptions glossary](https://docs.yearn.finance/getting-started/guides/how-to-understand-strategies-descriptions)
- [pentacle.xyz collective web3 knowledge](http://pentacle.xyz/)
- [defillama wiki](https://wiki.defillama.com/wiki/Main_Page)
- [defi developer roadmap](https://github.com/OffcierCia/DeFi-Developer-Road-Map)
- [defi security basics](https://mirror.xyz/blorms.eth/LI0i-2v2Qs5UX2NV_L6zA8JMOteoOw0jWSm4e8ZR2oo)
- [how to study defi](https://0xth.notion.site/DeFi-Studies-c16a5b6fba254c719fed633bc6b3b990#45356bb2587844588c678b98644cbf8f)

## DeFi Timeline ([source](https://defieducation.substack.com/p/the-history-of-defi))

A brief DeFi timeline exctracted from this  using GPT-3:

- **2009:** Bitcoin genesis block mined
- **2014:** Ethereum whitepaper published by Vitalik Buterin
- **2015:** MakerDAO launches on Ethereum testnet with eDollar (later renamed to SAI and finally DAI)
- **2017:** Chainlink mainnet launch
- **2018:** Uniswap mainnet launch; Bancor raises $150M in ICO
- **2019:** Compound mainnet launch with COMP token airdrop in 2020 - yearn.finance launches as Andre Cronje’s personal yield farming dashboard
- **2020:** Sushiswap forks Uniswap and absorbs over $1B in liquidity; Curve launches with vote-escrowed CRV governance model to direct stablecoin liquidity mining rewards to strongest pegs; DeFi summer fueled by COMP incentives results in influx of new users and TVL hitting close to $15B by September 2020 despite the pandemic
- **2021:** Bull run fuels decentralization of exchanges (DEX) from Ethereum to BSC with pancakeswap leading the pack; ETH 2.0 delay spurs move towards alt-L1 chains such as Avalanche, Cosmos & Solana; vote-escrowed tokenomics (veTokens) become popularized by Curve & Frax; Uniswap launches UNI governance token airdrop to incentivize migration away from Sushiswap
- **2022:** Cross-chain liquidity and interoperability becomes more important than ever with ETH 2.0 not on track to fix congestion issues in the near term
