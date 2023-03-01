![Frame 1 (10) copy](https://user-images.githubusercontent.com/1016190/176318619-852ebfb8-7972-4c30-8c47-06e6ca3d5493.png)




The Optimism ecosystem is overflowing with opportunity for builders. With OP Stack, Optimism Mainnet, and AttestationStation at your disposal, here is an always-growing list of Big Ideas for you to build.

These ideas range from “the community really wishes this tool existed” all the way to “might change the course of human history.” We draw inspiration from sources like [Vitalik’s blog](https://vitalik.ca/), community suggestions, and late-night brainstorms at conferences. Whether you’re hacking, shipping, or scaling, there’s something on the list where you can make your mark.

## Getting Started

- Pick an idea – any idea – and start building.
- Use the [Optimism Starter Kit](https://github.com/ethereum-optimism/optimism-starter), our [Getting Started tutorial](https://github.com/ethereum-optimism/optimism-tutorial/tree/main/getting-started), or [the AttestationStation guide](https://github.com/ethereum-optimism/optimism-tutorial/tree/main/ecosystem/attestation-station).
- If you’re the run-your-own-rollup type, [get started with OP Stack](https://stack.optimism.io/docs/build/getting-started/).
- Join us on [Discord](https://discord-gateway.optimism.io/) or [Telegram](https://t.me/+Cb7q0a1YqItkZTRk) to chat with other Optimism devs, find other builders working on ideas, and tell us what you’re working on.

---


# Ideas

## New: Build These Identity Ideas

| ATTN ETHDenver Hackers: consider ideas from here to get started hacking. Many of these qualify for [Optimism’s official BUIDLathon bounties](https://oplabs.notion.site/Optimism-in-Denver-5f3f32a7469b4bbb94c11cf71ada8529). Note that whether something is on this list does not impact judging. However, these ideas have been identified as exciting by our community and may be rewarded with traction, which is a strong qualifier for RetroPGF and other rewards. |
| :- |

Optimism’s ***AttestationStation (ATST)*** is a data primitive that allows people to start building their identity onchain. This smart contract provides a permissionless, accessible data source that enables anyone to make reputation-based applications. The following ideas make use of AttestationStation to create new identity primitives, reputation products, and even some competitors to real-world IDs.


### Tools and Resources

- What is [AttestationStation](https://community.optimism.io/docs/governance/attestation-station/)?
- AttestationStation [Tutorial (GitHub)](https://github.com/ethereum-optimism/optimism-tutorial/tree/main/ecosystem/attestation-station).
- AttestationStation [web-based user interface](https://attestationstation.xyz/)
- Optimism [Getting Started Guides](https://community.optimism.io/docs/guides/)
- [Optimist Score Queries & Data](https://app.flipsidecrypto.com/dashboard/optimist-score-queries-data-Jp7kIN) (Flipside)
- [Dune Dashboard - AttestationStation](https://dune.com/oplabspbc/optimism-attestationstation)

### Juicy Identity Products

- **Auth Everywhere:** Create an authentication system that uses AttestationStation to improve signin on wallet-connected dapps. Bonus points for forward-compatibility with Account Abstraction, such as EIP-4337. Sign into everything, everywhere, all at once. (Fun fact: in OP Labs’ internal brainstorms, this came up literally over a dozen different ways.)

- **Decentralized PGP Keyserver:** Use attestations to create a decentralized key server for PGP keys. For instance, make it easy for users to attest that a public key is genuine, and display a trust score for that key’s genuine-ness.

  - [Cryptographic Key Servers](https://en.wikipedia.org/wiki/Key_server_(cryptographic)); consider the [Problems with keyservers](https://en.wikipedia.org/wiki/Key_server_(cryptographic)#Problems_with_keyservers) section
  - [Public key infrastructure](https://en.wikipedia.org/wiki/Public_key_infrastructure)
  - [Web of trust](https://en.wikipedia.org/wiki/Web_of_trust)

- **Anti-Sybil Protocol / API:** Imagine an open, permissionless anti-Sybil API that any project can use to block fake accounts who do nothing but engagement farm.

- **Global Passport NFT:** Create an NFT that acts as a global passport, which can receive “stamps” to signal where you’ve visited. 

- **Decentralized Financial Regulator / Project Reputation:** Free, open source, on-chain star ratings of crypto projects, eventually adopted by US states and foreign states in lieu of SEC. (h/t [Balaji](https://twitter.com/balajis/status/1625723092537573376?s=46&t=t1EPp982MOOLNfuJTYeRlA))


### Identity Use Cases

- **Deep Fake Protection:** Create a tool for creators to attest that a livestream, video, image, or clip is from their real account(s). (h/t Livepeer)

- **Onchain Gaming Achievement System:** Create a decentralized achievement system as a public good that other games can build with.
  Features could include:
  - Traditional achievement system that activates an achievement-attestation when you accomplish something in-game.
  - “Props” system that you can say a teammate was good at healing, DPS, etc, to help with finding pickup groups in other games.
  - Onchain multi-game achievement rewards for being good at multiple titles.  
  - User-created achievements and voting system.
  - API for parsing achievement data to display in-game.

### AttestationStation Tooling

- **“Lazy Attestations”:** Off-Chain program that aggregates not-yet-committed attestations, then  handles committing them all in one go or using them as call data.

- **ATST Indexer/Subgraph:** The indexer tracks attestations via the AttestationStation by user account. The ATST Explorer then uses this data to populate attestation history. Indexer should include an API server, which serves data to web browsers. Try using ponder.sh or The Graph to start.

 - **ATST Explorer:**  Build Etherscan-for-Attestations. No-code interface used to view, create, update, explore, and contextualize attestations.

  - Search for attestations by attester address, receiver address, and transaction hash
  - See the latest attestations and all attestations
  - See the transaction hash, status, block, timestamp, raw data, referenced attestations, referencing attestations, author, receiver, key, and value for each attestation
  - An interface that allows user to read / view attestations
  - An interface that allows users to make / update batch or single attestations

- **TokenList.org-style AttestationList:**  Create a community-led initiative to improve discoverability, reputation and trust in attestations in a manner that is inclusive, transparent, and decentralized. Attestation Lists is a specification for lists of attestation metadata (e.g. address, decimals, ...) that can be used by any dapp interfaces that need one or more lists of attestations.

  - An instance of an attestation list following a standard JSON schema and can be hosted publicly on ENS, IPFS, or HTTPS.
  - Context on what attestation lists are
  - Directions on how to validate that a schemas follow the proposed standard
  - Directions on how to author a attestation list
    - List data
      - List URL
      - List Name
      - List version
      - Link to the official homepage of the list manager
    - Attestation data
      - Attestation name
      - Attestation author
      - Attestation key
      - Attestation value
      - Attestation image
      - Attestation description
  - Directions on how to deploy an attestation list
  - Examples of what a attestation list looks like

- **ATST Schemas:** Upgrade the ATST contract to enable schemas. A schema is a way for a client of the AttestationStation to understand the content of a given attestation.

- **ATST Relayer:** Make attestations on Optimism accessible on L1 Ethereum. This should have decent liveness (i.e not fall more than a few hours behind OP mainnet). It should be accessible from a smart contract. And, data should be well indexed and relatively easy to retrieve against the attested address.

- **WORM ATST:**  Upgrade the ATST contract to write once, read many. Do not allow attestors to modify a previously written attestation.

### Identity Quick Hits

- **Events Ticketing:** Create an application that lets creators create an event ticketing flow using attestations.

- **ATST Friending:** Create an application that lets people meet and connect through consensual attestations, such as exchanging info at a conference.

- **ATST Ratings:** Allow users to “rate” dapps that they have interacted with. Bonus points for making this cross-chain, enabling ratings for apps on OP Stack chains, Ethereum, or more.

- **Next Level Token Gating:** Instead of using tokens to lock access to something, instead have access unlock after getting specific attestations, or a certain threshold of multiple attestations. 

- **Walletless Onboarding:** Create a “low security zone”, similar to “free” users in a free-to-play game, where users can access features that don’t require signatures. 




### 🛠 **`Dev Tools`**

**Meta Faucet**  
An alternative to a traditional faucet: the user uploads their contract + params/bytecode and the relayer deploys it for free and sends the user ~2 OP Goerli ETH for testing. Could require users to scan a QR code to use during events.

**SDK Contributions**  
Anything from improving documentation, adding a feature to creating a tutorial! Our SDK is still in it’s early stages, so all contributions are welcome and encouraged!  
[SDK Docs](https://sdk.optimism.io/), [Repo](https://github.com/ethereum-optimism/optimism/tree/develop/packages/sdk)

**ethgasstation for Optimism**  
Create a version of https://ethgasstation.info/ that tracks and reports on gas fees and more for Optimism.  

**Blockchain & infrastructure projects**  
For more ideas on how to develop the rollup itself or its supporting infrastructure, checkout the [Infrastructure Project Ideas][infra] page. These projects tend to be beefier, and cater to aspiring blockchain devs.
<br>

[infra]: infrastructure.md

### 🌱 **`Public Goods`**

**RetroPGF dashboard**   
Help make RetroPGF approachable. Show data from the previous rounds, include links to articles (our article, Vitaliks).

**Tokenized GitHub repo**  
High level objective: Influence developers to reflect their work in tokens so we can fund them with RetroPGF. Rough idea: Make it easy to tokenize a GH repo. The owner can choose an initial allocation, automatic rewards for merged PRs, etc. They are then responsible for distributing the tokens to contributors, etc.

**Token-gated GitHub repos**  
Write a GitHub app that invites users to a repo if they connect their wallet and own a particular token.  
<br>

### 🪩 **`Bridging`**
**Full Wallet Migration**  
Bridge multiple / all tokens (ERC20 & ERC721) from your L1 wallet to Optimism in one transaction. 

**Embedded gateway**  
Open source component that devs can embed in their own project provide in-app bridging.

**Bridge Lottery**  
Slot machine extension for bridge that rewards random users with an NFT or other token.

**Bridge Snap for MetaMask**  
An extension for MetaMask that allows bridging from within the wallet.  
*See:* [MetaMask Snaps documentation](https://docs.metamask.io/guide/snaps-development-guide.html)

**Referral incentives**  
Sybil resistant referral system where each new address a user gets to use OP is rewarded.  
<br>

### 🔰 **`NFTs`**

**Composable Allowlists**
Create a way for projects to allowlist certain addresses and make those allowlists shareable using the [AttestationStation](optimism.io/reputation)

**L2 Gift Cards**  
An L1 NFT that sends ETH or OP to your L2 address when bridged over.  
*See also:* [Bridge Pass](https://d.mirror.xyz/Sjpxa2r_wxkQUGXUr8oO2PhBlyfIRgLBx2YevoXXwyY)

**Nested NFTs**  
Create a new standard or implementation for NFTs that can own NFTs. Think: item inventory, accessories, composable art.  
<br>

### 🎪 **`Social`**

**Onchain Activity Feed**  
A simple app that allows a user to connect a wallet and see what the addresses they've previously interacted with are up to now. Bonus points for categorizing contracts or rendering transactions with rich metadata.  

**Notification service**  
A protocol and UI for address-to-address messaging.   
*See also*: [Pearl](https://showcase.ethglobal.com/ethnewyork2022/pearl-fpatq), [EPNS](https://epns.io/)  
<br>

### 📊 **`DeFi`**  
[**Optimistic CFD**](https://github.com/2xic/optimistic-cfd) `👀 LOOKING FOR CONTRIBUTORS`  
A synth protocol that somewhat ressembles CFDs. The innovation lies in the fact that the protocol comes in to compensate imbalances between the longs and the shorts, while incentivizing the imbalance to correct itself. See the design notes for more information.

**Automated Trading Bot**  
A web app that lets users create automated trading bots, in the fashion of Option Alpha. This requires frontend, backend, contract and bot development!  
*See*: [Podcast](https://optionalpha.com/podcast/build-a-fully-automated-options-portfolio-with-3000-in-1-click)  
<br>

# Past Hackathon Winners
|Project | Description |Hackathon|
|:--|:--|:--|
| [**Retr0x**](https://showcase.ethglobal.com/ethamsterdam/retr0x-2p73o) | Fully on-chain retro-generative public goods funding app deployed with Optimism. Our implementation includes funding initiation with a curated whitelist, a smart contract that executes quadratic voting and fund disbursement logic and a dashboard to access on-chain data. | ETHAmsterdam |
 [**Stargaze**](https://ethglobal.com/showcase/stargaze-igmkq) | Today, open source projects are based on voluntary contributions. While these contributors do not seek financial gain for their contributions, the donations made to these projects rarely reach many of the downstream developers and contributors that have created and maintain them. <br><br>We aim to solve that problem by distributing funds to contributors when donations to projects are made by supporters. In this current implementation, Stargaze uses a basic metric to value contributions and calculate an impact score representing a contributor’s share of the total value created. He or she receives donations proportionately to his or her share.| ETHNewYork |
 [**ETHdos**](https://ethglobal.com/showcase/ethdos-yyj28) | ETHdos numbers measure degrees of separation of people (akin to Bacon/Erdos numbers) while hiding individual friendships entirely. This is the first of its kind social experiment using the composability of recursive zk snarks. | ETHNewYork | 
<br>

# Other Resources
* [Developer documentation](https://community.optimism.io/)  
* [Get in touch](https://optimismpbc.typeform.com/get-in-touch)  
* [Apps on Optimism](https://www.optimism.io/apps/all)

