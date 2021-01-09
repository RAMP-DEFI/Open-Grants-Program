# RAMPDEFI Grant Proposal
![](https://rampdefi.com/assets/Rampdefilogoblack200.png)

# Open Grant Proposal

* **Project Name:** RAMP DEFI
* **Team Name:** RAMP DEFI
* **BTC Payment Address:** 1DQNr9EyYmoS5hbwRzQkfNrw5DS247cpF8

## Project Overview

**Overview**
RAMP DEFI is a global decentralized finance solution that focuses on unlocking liquid capital from staked digital assets. Using the RAMP solution, users with staked assets can continue to receive staking rewards, retain capital appreciation potential on their staked portfolio, and unlock liquid capital to invest in new opportunities at the same time.

RAMP DEFI was created to solve problems that we as users faced with locked staked assets. As with traditional markets, capital should be free to flow even as yield is being generated in order to maximise capital efficiency.

The addressable market for staked assets today is upwards of USD25bn, and as the industry-leading solution, RAMP DEFI has a vision of unlocking USD1bn or more in "Total Value Unlocked (TVU)" for users by end 2021.

The RAMP vaults and rStake have launched with major blockchains IOST, Tomochain and Tezos has total first phase TVL of 2.8 Million USDT worth of assets.

rMint is the collateralization of these staked assets and in turn enable for liquid capital to be extracted. This is done by an over-collateralization process which mitigates risks on a few levels.
1) Over-collateralization of assets give the buffer required in cases of wide volatility
2) Liquidation triggers are placed at adequate levels to ensure that risk is not transferred to the overall RAMP eco-system
3) On and Off-chain Keepers that bite triggered stake assets

As a natural component of the RAMP eco-system, the liquidation framework takes high priority in order of importance. Whilst developing such functions on other major blockchains, it became intuitive that such a keeper system is both required and well suited within Polkadot. Hence, POLKAKEEPER would be the native Keeper extension of RAMP DEFI built on Polkadot. 

We intend for PolkaKeeper to run on its own Parachain on the Polkadot network to . If the bond cannot be funded, the protocol will run on Parathreads or possibly as a series of smart contracts and API integrations. Our initial testnet and protocol configuration will be built on Kusama and ported onto Polkadot for the mainnet launch.

Polka-Keeper protocol
- Substrate-based (Parachain or Parathread deployment)
- Native token issued, with DAO governance
- Keepers can be deployed as SmartContracts by anyone (WASM first, EVM later )
- Connectivity to other parachains and bridges natively supported and added
- Access to off-chain workers (Triggering of Smart Contracts)
- Deposit to KeeperPool and collaborate with Underwriters, Yielders
- Proof-of-concept: Moonbeam/Acala/Reef



## Project Details 

Overview of RAMP System built on Polkadot:
![](https://rampdefi.com/assets/PolkadotRAMP.jpg)

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






