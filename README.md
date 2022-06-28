![Frame 1 (10) copy](https://user-images.githubusercontent.com/1016190/176318619-852ebfb8-7972-4c30-8c47-06e6ca3d5493.png)


If you're looking for inspiration, you're in the right place :sparkles: 

The Optimism ecosystem is overflowing with opportunity for builders. The OP community has collected a few ideas that are ready to get started on.

**Want to build?**  
— Pick an idea from the list below.  
— Jump in to **[#dev-support](https://discord.com/channels/667044843901681675/887914409207414785)** or **[#l2-jobs](https://discord.com/channels/667044843901681675/955547725125005342)** on [Discord](https://discord-gateway.optimism.io/) to chat about what you want to build. You can also join the informal [Skunkworks chat](https://t.me/+Cb7q0a1YqItkZTRk) on Telegram.  
— Open a PR on this repo to move the project to "looking for contributors" and add your contact info.

**Have an idea?**  
Just start building! If you want help finding contributors, open a PR on this repository to add your idea to the list.

**Don't know where to start?**  
Come hang out in Discord! Share what you want to contribute, or look out for other team's asks. 

# Ideas

### 🛠 **`Dev Tools`**

**Meta Faucet**  
An alternative to a traditional faucet: the user uploads their contract + params/bytecode and the relayer deploys it for free and sends the user ~2 OP Kovan ETH for testing. Could require users to scan a QR code to use during events.

**SDK Contributions**  
Anything from improving documentation, adding a feature to creating a tutorial! Our SDK is still in it’s early stages, so all contributions are welcome and encouraged!  
[SDK Docs](https://sdk.optimism.io/), [Repo](https://github.com/ethereum-optimism/optimism/tree/develop/packages/sdk)

**Fix Hardhat Forking**  
Fix Hardhat forking for L1BlockNumber opcode. You will be a legend forever.  
<br>

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

**Referral incentives**  
Sybil resistant referral system where each new address a user gets to use OP is rewarded.

**Bridge Snap for MetaMask**  
An extension for MetaMask that allows bridging from within the wallet.

**Referral incentives**  
Sybil resistant referral system where each new address a user gets to use OP is rewarded.  
<br>

### 🔰 **`NFTs`**

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
