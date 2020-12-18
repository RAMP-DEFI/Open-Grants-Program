# RAMPDEFI Grant Proposal
![](https://rampdefi.com/assets/Ramplogoblack.png)

# Open Grant Proposal

* **Project Name:** RAMP DEFI
* **Team Name:** RAMP DEFI
* **Payment Address:** 1DQNr9EyYmoS5hbwRzQkfNrw5DS247cpF8

### Project Overview

**Overview**
RAMP DEFI is a global decentralized finance solution that focuses on unlocking liquid capital from staked digital assets. Using the RAMP solution, users with staked assets can continue to receive staking rewards, retain capital appreciation potential on their staked portfolio, and unlock liquid capital to invest in new opportunities at the same time.

RAMP DEFI was created to solve problems that we as users faced with locked staked assets. As with traditional markets, capital should be free to flow even as yield is being generated in order to maximise capital efficiency.

The addressable market for staked assets today is upwards of USD25bn, and as the industry-leading solution, RAMP DEFI has a vision of unlocking USD1bn or more in "Total Value Unlocked (TVU)" for users by end 2021.

The RAMP vaults and rStake has launched with major blockchains IOST and Tomochain and has total first phase TVL of 2.8 Million USDT worth of assets.

We intend for RAMP DEFI to run on its own Parachain on the Polkadot network. If the bond cannot be funded, the protocol will run on Parathreads or possibly as a series of smart contracts and API integrations. Our initial testnet and protocol configuration will be built on Kusama and ported onto Polkadot for the mainnet launch.

In order to fulfil RAMP DEFI's vision of unlocking liquid capital for frozen assets, it is imperative to establish a robust network of partners and a strong community who aligns with this vision. We strongly believe that the Polkadot eco-system and community is well suited as a major component of RAMP DEFI's vision. 

Please provide the following:
  * A brief description of the project.
  RAMP DEFI unlocks liquid capital from staked assets.
  * An indication of how you will integrate this project into Substrate / Polkadot / Kusama.
  - rStake on Polkadot and  collatoralization of Polkadot into Native DOTUSD
  - launching Polkadot versions of rUSD and RAMP
  * An indication of why your team is interested in creating this project.
We're solving this problem to unlock the liquidity across chains.

### Project Details 
![](https://rampdefi.com/assets/03442414724cd1fd5c0b68fa0b808125.png)

We expect the teams to already have a solid idea about the project's expected final state.

Therefore, we ask the teams to submit (where relevant):
* Mockups/designs of any UI components: 
https://app.rampdefi.com
![](https://rampdefi.com/assets/app_dashboard_front.png)
![](https://rampdefi.com/assets/app_dashboard.png)
![](https://rampdefi.com/assets/app_dashboard_stake.png)

* API specifications of the core functionality [TBA]
* An overview of the technology stack to be used: Moonbeam EVM, AWS, Chainlink [To be added]
* Documentation of core components, protocols, architecture etc. to be deployed

rStake is an aggregator of staking nodes on the participating native blockchains, to earn staking rewards.

rMint takes in non-ERC20 digital assets as collateral and mints rUSD against this collateral with a safe liquidation buffer. 


* PoC/MVP or other relevant prior work or research on the topic: https://app.rampdefi.com/#/stake

### Ecosystem Fit 
Are there any other projects similar to yours? If so, how is your project different?
Cross-chain functionality is one of the core tenets of Polkadot and would open additional legos to be built on top of the RAMP infrastructure. There's some similarity in Stafi though we create assets on the native blockchain instead of just wrapping the assets.

## Team :busts_in_silhouette:

### Team members
* Name of team leader
Lawrence Lim (CEO, Project Lead, Co-founder)
* Names of team members	
Loh Zheng Rong (COO/CMO, Marketing Lead, Co-founder)
Caspar Oostendorp (Technical Lead)
Anu Nair (Blockchain Lead)
Jeannette Zhang (Operations Lead)

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
* Lawrence Lim https://www.linkedin.com/in/lawrencelimhz/
* Loh Zheng Rong https://www.linkedin.com/in/lohzhengrong/
* Caspar Oostendorp https://www.linkedin.com/in/caspar-oostendorp-7bb82873/
* Anu Nair https://www.linkedin.com/in/anu-b-nair-0551763a/
* Jeanette Zhang https://www.linkedin.com/in/jeanettez/

## Development Roadmap :nut_and_bolt: 

This section should break out the development roadmap into a number of milestones. Since the milestones will appear in the grant contract, it helps to describe the functionality we should expect, plus how we can check that such functionality exists in the product. Whenever milestones are delivered, we refer to the contract to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**. In the descriptions it should be clear how the project is related to Substrate and/or Polkadot. We recommend that the scope of the work can fit within a 3 month period and that teams structure their roadmap as 1 month = 1 milestone. 

For each milestone:
* Please be sure to include a specification of your software. Treat it as a contract - the level of detail must be enough to later verify that the software meets the specification.
To assist you in defining it, we created a document with examples for some grant categories [here](../src/grant_guidelines_per_category.md).
* Please include total amount of funding requested per milestone.
* Please note that we require documentation (e.g. tutorials, API specifications, architecture details) in each milestone. This ensures that the code can be widely used by the community.
* Please provide a test suite, comprising unit and integration tests, along with a guide on how to run these.
* Please commit to providing a dockerfiles for the delivery of your project. 
* Please indicate the milestone duration, as well as number of Full-Time Employees working on each milestone, and include the number of days along with their cost per day.
* Deliverables 0a-0d are mandatory and should not be removed, unless you explicitly specify a reason within the PR's `Additional Notes` section (e.g. Milestone X is research oriented and as such there is no code to test)

Q4 2020
• eMint development.
• eFarm development.
• rPool development.
• RAMP farming structure to be released.
• RAMP alpha and beta pool farming to begin.
Q1 2021
• rFinance development.
• RAMP delta pool farming to begin.
• RAMP governance structure.
• Decentralization of RAMP governance.

### Overview
* **Total Estimated Duration:** 3 Months / POC
* **Full-time equivalent (FTE):**  20.25
* **Total Costs:** 1.55 BTC

### Milestone 1 Summary

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0a. | License | Apache 2.0 / MIT / Unlicense |
| 0b. | Documentation | We will provide both inline documentation of the code and a full tutorial that explains how to interact and communicate with the testnet protocol |
| 0c. | Testing Guide | The code will have unit-test coverage (min. 90%) to ensure functionality and robustness. In the guide we will describe how to run these tests | 
| 0d. | Medium Article | We will publish a medium article that announces all deliveries and a step by step tutorial to the community once evaluation is passed.
| 1. | Testing | We will conduct testing of the developed functionalities on Westnet testnet. |  
| 2. | Substrate module: A | Staking/unstaking of DOT |  
| 3. | Substrate module: B | Creation of wDOT|  
| 4. | Substrate module: C | Collatoralization of wDOT into DOTUSD |  
| 5. | Substrate module: D | Minting of rUSD on Polkadot |
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

Incentive programs for alliance partners
Bug bounties
Hackathon
Community grants to develop new products under the RAMP DEFI Eco-system

## Additional Information :heavy_plus_sign: 
Any additional information that you think is relevant to this application that hasn't already been included.

**What work has been done so far?** We've live with 2 RAMP Vaults (TVL 2.8 Mil USDT at time of writing) and 2 rStake across 2 major blockchains (IOST and TomoChain). Intergrated Chainlink for price feed and have accomplished industry first cross-chain stake farming. 
Integrated with major partners such as Solana, Elrond, IOST, NULs, Tomochain, Injective, Moonstake & Crust.
**Are there are any teams who have already contributed (financially) to the project?** Our expenses have been covered thus far via investments from world class investors who took part in our private sale round such as Alameda Research, Mechanism Capital, Arrington XRP, Parafi Capital, among others. We have further investment interest for follow-on investment should the need arise between the use of this grant and our next source of funding, whether that be the General Grants program or another VC-led investment.
**Have you applied for other grants so far?** Yes.


> This document is referenced in the terms and conditions and therefore needs to contain all the required information. Don't remove any of the mandatory parts presented in bold letters or as headlines! See the [Open Grants Program Process](https://github.com/w3f/Open-Grants-Program/blob/master/README_2.md) on how to submit a proposal.

*The above combination of your GitHub account submitting the application and payment address will be your unique identifier during the program. Please keep them safe.*


## Project Overview :page_facing_up: 
If this application in response to an RFP then please indicate this on the first line of this section.

### Milestone 2 Example — Additional features
* **Estimated Duration:** 1 month
* **FTE:**  1
* **Costs:** 0.75 BTC
...
