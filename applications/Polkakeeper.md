# Polkakeeper Grant Proposal
![](https://rampdefi.com/polkakeeper/digitalassets/polkakeeperlogo.png)

# Open Grant Proposal

* **Project Name:** Polkakeeper
* **Team Name:** RAMP DEFI
* **BTC Payment Address:** 1DQNr9EyYmoS5hbwRzQkfNrw5DS247cpF8

## Polkakeeper - A Community-Led Value Assurance Protocol Empowering DeFi Markets Efficiency on Polkadot


**Project Overview**

Polkakeeper is a decentralized value assurance underwriter that empowers community creation of keeper strategies on the Polkadot network and bridged chains. On Polkakeeper, Strategists create Keepers (smart contracts), which can be executed by Finders who actively search for keeper execution opportunities. Backers are users who deposit their funds or assets into Vaults to back the deployment of keeper strategies. 

Keepers are automated on-chain value assurance strategies that increase overall DeFi market efficiencies, such as liquidating undercollateralized positions in lending / margin trading protocols, or smoothing asset prices through arbitrage strategies across exchanges. Uniquely, Keepers may deploy assets across chains, which give strategies new dimensions in identifying profit opportunities. A simple example of a Keeper strategy can be for Finders to monitor asset prices across multiple DeFi protocols such as Acala, Polkadex etc, and deploying assets from Vaults to close off pricing differences with no risks to the principal.

Upon successful Keeper execution, the protocol takes 3.5% of the profits, and the remaining is distributed among the Strategist, Finder and Vaults. Where funds or assets in Vaults are not utilized, they are deployed to lending protocols and optimized for the best yields across chains.

The vision for Polkakeeper is to become the leading value assurance protocol and through DAO governance, organizes the Polkadot developer and user communities towards optimizing and maintaining high level of market efficiencies for Polkadot DeFi protocols. Polkakeeper is designed to empower community collaboration for Strategists, Finders and users to act collectively, rather than individually.

Polkakeeper is designed as an independent, composable Substrate component that can be seamlessly integrated and deployed across Polkadot’s multi-chain network.


## Project Details 

Overview Diagram of how Polkakeeper works
![](https://rampdefi.com/polkakeeper/digitalassets/technical_diagram.jpg)


# Sample Scenario
A description of how Polkakeeper works, by walking through a typical scenario:
* Polkakeeper goes live, and publishes its SmartContract API
* A user (Strategist) writes a Smart Contract that implements a certain trade or action and deploys/registers it.
* Another user (Finder) finds a newly registered SmartContract on the Polkakeeper app and makes a NodeJS app that scans the relevant (para) chain for opportunities to apply the Keeper Strategy on.
* The Finder may choose to fund each execution of the Keeper herself, or leverage with extra funding from the Vault. In this case dividends will be paid on the results of the execution.
* Meanwhile, yet another user who is not technically savvy but wants to participate, deposits in the Vault as a Backer. This makes him eligible for dividends on results of the Keeper executions if the funds are used.
* The Finder (or an automated task) calls the PolkaKeeper chain to execute the chosen Keeper with the found parameters
* After all the actions are completed, results will be paid out to Finder and Backers.

# Components
* Native Token
  * A native token shall be issued to power the Polkakeeper ecosystem, rewarding developers, users and node operators who contribute to the growth and continued development of Polkakeeper.
  * Implementation: The built-in Currency trait from FRAME.

* Account
  * Accounts live on the Polkakeeper network, and identify the user. Depending on the security level needed to be Strategists or Finders, additional verification can be added
  * Implementation: The built-in account system from FRAME.

* Node
  * Polkakeeper will run several Collator and Full nodes to ensure functioning and reliability of the network, and to enable the features added by the off chain workers. 
  * The parachain will be implemented using  Substrate+Cumulus, initially for local development and later on the Rococo testnet. 
  * The nodes will run the Polkakeeper Runtime, which, among other features, includes the Contracts Pallet, enabling deployment of the KeeperManager and Keeper contracts. 
  * Eventually, Nodes will be set up in such a way that a direct connection with other Parachains is possible, without going through the Relay Network.

* KeeperManager (Runtime)
  * Extrinsic that enables viewing/adding/removing/changing/disabling Keepers by accounts in the chain.
  * Implementation: A Smart Contract that can be transacted with through the UI and programmatically. 
  * The Polkakeeper Runtime makes available Chain Extensions that allow the smart contracts to utilize relevant parts of the Polkadot ecosystem and connected parachains, bridges and off chain functionality.
  * Connectivity to other parachains is implemented with XCMP using the Xcm::Transact type (once available)

* Keeper (Smart Contract)
  * Logic that is designed to be applied on specific targets. For example, a function that executes a specific trade on another parachain such as Acala. The logic is predefined, but the input (the tokens and amounts) are parameterized.
  * Implemented as Smart Contracts to be deployed to the chain by the users. These still have to be registered in the KeeperManager.

* Strategist
  * A user who designs new Keepers (strategies), authors, deploys the Smart Contracts and registers these in the KeeperManager.

* Finder
  * A user who finds opportunities to execute a Keeper strategy against. The finding is done off-chain due to the required computing/network resources needed. The outcome is a transaction that invokes a Keeper with specific Parameters.

* Backer
  * A user who provides liquidity to the Vault. In exchange for this, executing Keepers can be done with larger leverage, and depending on the configuration set by the Strategist, profits are shared.

* Vaults
  * (Shared) Keepers can utilize a pool of user funds to enter profit opportunities. Profits may be shared with the pool participants.
  * The vault is implemented as a Smart Contract or directly in the Runtime, and will be available programmatically or through the User Interface. Functionality includes: deposit, withdrawal.

# Runtime Modules
* KeeperManager (Main runtime)
 * Events
  * KeeperDeployed, KeeperRemoved, KeeperRun, KeeperDisabled, KeeperEnabled
  * VaultDeposit, VaultWithdrawal
 * Storage
  * Keepers (StorageDoubleMap)
   * keeperOwners: (address => “owner” => address)
   * keeperEnabled: (address => “enabled” => address)
  * VaultBalances (StorageDoubleMap)
   * Balance: (address => “tokenID” => number)
  * Dividends (StorageDoubleMap)
   * Dividend: (address => “tokenID” => number)
 * Public Methods
  * registerKeeper(address)
  * listKeepers() -> Vec<Keeper>
  * removeKeeper(keeperAddress)
  * runKeeper(address) -> CallResult
  * disableKeeper(address)
  * enableKeeper(address)
  * claimDividend()
  * Custom dispatchable extrinsics (for calling from Chain Extension in Keepers)
   * Here we would implement predefined cross-parachain XCMP calls, dispatchable from inside the contract. For example executing a specific trade in Acala, for which all tokens and permissions are already in place.
   * Additionally, methods provided by the Contracts Pallet will be exposed as well. These allow for deployment and instantiation of the SmartContracts.
* Keeper (SmartContract)
 * All the usual Ink! Functionality is available.
 * We may enforce a 
 * Documented Chain Extensions from the Runtime
  * Cross-Parachain functionality
  * Offchain Worker functionality



Live UI designs:
https://app.rampdefi.com

Live rStake system:
https://app.rampdefi.com/#/stake

### Current rStake for IOST and Tomochain
![](https://rampdefi.com/assets/app_dashboard_front.png)
![](https://rampdefi.com/assets/app_dashboard.png)
![](https://rampdefi.com/assets/app_dashboard_stake.png)

## rStake
rStake allows for active rewards staking through nodes on the participating native blockchains, to simultaneously earn staking rewards while enabling collateralization for unlocking of additional liquid capital.

Users would be able to Stake their DOT to strengthen the Polkadot eco-system and earn staking rewards.

## rCollateralization and rMint

RAMP DEFI uses a “Collateralization Ratio” system to ensure that the rMinted DOTUSD/rDollar is always fully collateralized.

The “Minimum Collateralization Ratio (MCR)” for staked digital assets on each blockchain starts at a default 300%. This means that $300 worth of Token X can at most, mint $100 worth of DOTUSD/rDollar. The user may choose to issue at a higher Collateralization Ratio if a larger buffer is preferred (e.g. 600% collateralization: stake $300 of Token X to issue $50 of rDollar).


![](https://rampdefi.com/assets/Collateral.png)


The collateralization ratio at which liquidation is triggered, called the “Liquidation Ratio (LR)”, starts at a default 120% for each blockchain.


![](https://rampdefi.com/assets/Liquidate.png)


The Collateralization Ratio at which a re-collateralization request is triggered (“Re-Collateralization Ratio”) is the midpoint between the Minimum Collateralization Ratio and the Liquidation Ratio.


![](https://rampdefi.com/assets/recollateral.png)


In the event that a user receives a re-collateralization request, the user simply needs to send more Token X into the native staking contract to issue more Wrapped Token X and re-collateralize the position back to the MCR.

In the event that the Liquidation Ratio is triggered, the users’ tokens are considered “sold” to rPool, the universal liquidity pool that underpinned the RAMP ecosystem.

rPool liquidates these tokens on exchanges and deposit the liquidated value into rPool. At the same time, rPool uses the existing liquidity within the pool to repurchase the same amount of rDollar minted by the user from the open market. 

The difference in value between the liquidated assets and the repurchased rUSD accrue into rPool, to be distributed to RAMP token holders during the weekly value distribution.


* API specifications of the core functionality [TBA]
* An overview of the technology stack to be used: Moonbeam EVM, AWS, Chainlink [To be added]
* Documentation of core components, protocols, architecture etc. to be deployed



## Ecosystem Fit 
Cross-chain functionality is one of the core tenets of Polkadot and the capital efficiency that RAMP DEFI is building would be a core piece to enable further evolution of open finance and Defi within the blockchain space. 

We see some projects who seek to solve this similar issue, one such example is Makerdao where ETH is used as collateral to extract additional value from the asset and Kava which uses a wrapped solution. There are however, drawbacks as Makerdao and Kava are mainly only on Ethereum blockchain and have not ventured into cross blockchain flow of value.

### To solve this we intend to build holistically

With multiple components already built by RAMP DEFI on other blockchains, we are well poised to bring over massive value from other blockchains into the Polkadot eco-system. By building up the rStake and rMint port on polkadot, this provides a multi-pronged benefit of capital efficiency from staked assets on Polkadot whilst contributing to the security of the network and allow for the inflow of value capital from other blockchains.

## Team :busts_in_silhouette:

### Team members
* Lawrence Lim (CEO, Project Lead, Co-founder)
* Loh Zheng Rong (COO/CMO, Marketing Lead, Co-founder)
* Caspar Oostendorp (Technical Lead)
* Anu Nair (Blockchain Lead)
* Jeannette Zhang (Operations Lead)

### Contact
* **Contact Name:** LOH ZHENG RONG
* **Contact Email:** zr@rampdefi.com
* Website
https://app.rampdefi.com/#/
https://rampdefi.com/

### Legal Structure 
* **Registered Address:** 14 ROBINSON ROAD #08-01A FAR EAST FINANCE BUILDING S(048545)
* **Registered Legal Entity:** Ramp Protocol Pte Ltd

### Team's experience
Please describe the team's relevant experience.  If the project involves development work, then we'd appreciated if you can single out a few interesting code commits made by team members on their past projects. For research-related grants, references to past publications and projects in a related domain are helpful. 
Senior Blockchain (Cross-chain) engineers [TBA]

### Team Code Repos
* https://github.com/RAMP-DEFI
* https://github.com/RAMP-DEFI/RAMP_IOST
* https://github.com/RAMP-DEFI/RAMP_TOMOCHAIN
* https://github.com/RAMP-DEFI/RAMP_VERSION_TEZOS
* https://github.com/RAMP-DEFI/RAMP_REWARDS_MANAGER
* https://github.com/RAMP-DEFI/RAMP_API
* https://github.com/RAMP-DEFI/RAMP_WEB_MAIN
* https://github.com/RAMP-DEFI/RAMP_wRAMP
* https://github.com/RAMP-DEFI/RAMP_IOSTSWAP
* https://github.com/RAMP-DEFI/RAMP_Public_Sale
* https://github.com/RAMP-DEFI/RAMP_ERC_CLAIM_DAPP
* https://github.com/RAMP-DEFI/RAMP_SECURITY_AUDITS_REWARDS
* https://github.com/RAMP-DEFI/RAMP_SECURITY_AUDITS_IOST
* https://github.com/RAMP-DEFI/RAMP_SECURITY_AUDITS_TOMOCHAIN



### Team LinkedIn Profiles
* **Lawrence Lim** https://www.linkedin.com/in/lawrencelimhz/
* **Loh Zheng Rong** https://www.linkedin.com/in/lohzhengrong/
* **Caspar Oostendorp** https://www.linkedin.com/in/caspar-oostendorp-7bb82873/
* **Anu Nair** https://www.linkedin.com/in/anu-b-nair-0551763a/
* **Jeanette Zhang** https://www.linkedin.com/in/jeanettez/

## Development Roadmap :nut_and_bolt: 



### Overview
* **Total Estimated Duration:** 3 Months / POC
* **Full-time equivalent (FTE):**  2.75
* **Total Costs:** 1.25 BTC

### Milestone 1 Summary

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0a. | License | MIT |
| 0b. | Documentation | We will provide both inline documentation of the code and a full tutorial that explains how to interact and communicate with the testnet protocol |
| 0c. | Testing Guide | The code will have unit-test coverage (min. 90%) to ensure functionality and robustness. In the guide we will describe how to run these tests | 
| 0d. | Medium Article | We will publish a medium article that announces all deliveries and a step by step tutorial to the community once evaluation is passed.
| 1. | Testing | We will conduct testing of the developed functionalities on Westnet testnet. |  
| 2. | Substrate module: A | Staking/unstaking of DOT |  
| 3. | Substrate module: B | Creation of wDOT|  
| 4. | Substrate module: C | Collatoralization of wDOT into DOTUSD |  
| 5. | Substrate module: D | Minting of rDollar on Polkadot |
| 6. | Substrate module: E | Minting of RAMP on Polkadot |
| 7. | Repository | Repository including a README that describes the milestone and explains how to run, test and contribute |
| 8. | Docker | A docker container that will also run on CI to test the deliverables of the milestone |


## Community Engagement
We plan to write several articles and communication pieces about RAMP DEFI's integration and implementation on Polkadot. They include, but are not limited to:

Medium Articles on the integration and tutorials for users.
Twitter Threads and Posts covering our development and announcements
Community engagement by running a range of incentivised testnets to get more feedback from the existing end-users to improve our product and get TVL into TVU.


## Future Plans
Future Developments will focus on the following:

Incentive programs and multi-level collaboration for alliance partners
Bug bounties
Community developer grants to develop new products and derivative structures under the RAMP DEFI Eco-system


## Additional Information :heavy_plus_sign: 
Any additional information that you think is relevant to this application that hasn't already been included.

* **What work has been done so far?** 
We've live with 2 RAMP Vaults (TVL 2.6 Mil USDT at time of writing) and 2 rStake across 2 major blockchains (IOST and TomoChain) with integrations across existing lego pieces, Chainlink for price feed and VRF and have accomplished industry first cross-chain stake farming. 
Integrated with major partners such as Solana, Elrond, IOST, NULs, Tomochain, Injective, Moonstake & Crust.

* **Are there are any teams who have already contributed (financially) to the project?** Our expenses have been covered thus far via investments from world class investors who took part in our private sale round such as Alameda Research, Mechanism Capital, Arrington XRP, Parafi Capital, among others. We have further investment interest for follow-on investment should the need arise between the use of this grant and our next source of funding, whether that be the General Grants program or another VC-led investment.

* **Have you applied for other grants so far?** 
Yes.

* **How can I get involved?** 
Anyone looking to get involved with RAMP DEFI is welcomed to reach out to us through the following:
Email: team@rampdefi.com
Twitter: https://twitter.com/RampDefi
Telegram: https://t.me/rampdefiofficial
LinkedIn: https://www.linkedin.com/company/rampdefi
Discord: https://discord.gg/WY5TU7b
Medium: https://medium.com/rampdefi
