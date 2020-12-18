# RAMPDEFI Grant Proposal
![](https://rampdefi.com/assets/Ramplogoblack.png)

# Open Grant Proposal

> This document is referenced in the terms and conditions and therefore needs to contain all the required information. Don't remove any of the mandatory parts presented in bold letters or as headlines! See the [Open Grants Program Process](https://github.com/w3f/Open-Grants-Program/blob/master/README_2.md) on how to submit a proposal.

* **Project Name:** RAMP DEFI
* **Team Name:** RAMP DEFI
* **Payment Address:** BTC payment address. We don't accept payments for the program in other currencies at this stage. (e.g. 123mp123...)

*The above combination of your GitHub account submitting the application and payment address will be your unique identifier during the program. Please keep them safe.*

## Project Overview :page_facing_up: 
If this application in response to an RFP then please indicate this on the first line of this section.

### Overview

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
* Mockups/designs of any UI components: https://app.rampdefi.com/#/stake
* API specifications of the core functionality [TBA]
* An overview of the technology stack to be used: Moonbeam EVM, AWS, Chainlink [To be added]
* Documentation of core components, protocols, architecture etc. to be deployed
* PoC/MVP or other relevant prior work or research on the topic: https://app.rampdefi.com/#/stake

### Ecosystem Fit 
Are there any other projects similar to yours? If so, how is your project different?
Cross-chain functionality is one of the core tenets of Polkadot and would open additional legos to be built on top of the RAMP infrastructure. There's some similarity in Stafi. We create assets on the native blockchain instead of just wrapping the assets.

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
| 0d. | Medium Article | We will create a medium article or tutorial that sannounces all deliveries to the community once evaluation is passed.
| 1. | Testing | We will conduct testing of the developed functionalities on Westnet testnet. |  
| 2. | Substrate module: A | We will allow staking/unstaking of DOT |  
| 3. | Substrate module: B | We will allow creation of wDOT|  
| 4. | Substrate module: C | We will allow collatoralization of wDOT into DOTUSD |  
| 5. | Substrate module: D | We will allow minting of rUSD |  
| 6. | Repository | Repository including a README that describes the milestone and explains how to run, test and contribute |
| 7. | Docker | A docker container that will also run on CI to test the deliverables of the milestone |

### Milestone 2 Example — Additional features
* **Estimated Duration:** 1 month
* **FTE:**  1
* **Costs:** 0.75 BTC
...

## Community Engagement
We plan to write several pieces about RAMPDEFI implementation. They include, but are not limited to:

Weekly Medium Articles
Daily Twitter Threads and Posts
We also intend to engage community by running range of incentivised testnets to get more feedback from the existing end-users to improve our product.


## Future Plans
Future Developments will focus on the following:

Incentive programs for alliance partners
Bug bounties
Hackathon
Community grants to develop new products under the RAMP DEFI Eco-system

## Additional Information :heavy_plus_sign: 
Any additional information that you think is relevant to this application that hasn't already been included.

**What work has been done so far?** We've live with 2 RAMP Vaults (TVL 2.8 Mil USDT at time of writing) and 2 rStake across 2 major blockchains (IOST and TomoChain). Intergrated Chainlink for price feed and have accomplished industry first cross-chain stake farming.
**Are there are any teams who have already contributed (financially) to the project?** Our expenses have been covered thus far via investments from world class investors who took part in our private sale round such as Alameda Research, Mechanism Capital, Arrington XRP, Parafi Capital, among others. We have further investment interest for follow-on investment should the need arise between the use of this grant and our next source of funding, whether that be the General Grants program or another VC-led investment.
**Have you applied for other grants so far?** No.
