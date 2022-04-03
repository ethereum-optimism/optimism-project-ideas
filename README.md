# Optimism Project Ideas

Ideas for project to be deployed on Optimism. I'll try to support you as best I can!

Feel also free to contribute to existing projects (or even to fork them, if stalled).

Join our little Telegram community ([Optimism Skunk Works](https://t.me/+Cb7q0a1YqItkZTRk)) to keep up to date with the latest developments and be part of the fun.

## Ongoing Projects

- [Optimistic CFD](https://github.com/2xic/optimistic-cfd)  
  A synth protocol that somewhat ressembles [CFDs](https://www.investopedia.com/articles/stocks/09/trade-a-cfd.asp). The innovation lies in the fact that the protocol comes in to compensate imbalances between the longs and the shorts, while incentivizing the imbalance to correct itself. See [the design notes](https://github.com/2xic/optimistic-cfd/issues/1) for more information.

- [Space NFT Game](https://github.com/JFF-Danno/SpaceNFTGame)  
  A OGame-like planet-building space-conquesting game.
  
## Ideas

- ___Permissionless NFT Bridge___  
  There are other people working on similar ideas, but there is space for competition. It would be good to have a protocol that would enable permissionless bridging of any NFT from mainnet onto Optimism. One particular problem of interest to be solved is that of fast withdrawal (as it stands, secure withdrawals must wait until the end of the 7-day challenge window). I think this issue could be solved with on-chain signatures and liquidity pools to guarantee payments (similar to insurance protocols).

- [Implement Unicrawl](https://twitter.com/dhof/status/1475246745399476235)  
  The idea by Dom is a bit rough — meaning you have plenty of creative license to experiment with. Basically the game includes a roguelike aventure side and a "Dungeon Keeper" side. Figuring out the mechanics that make this work is the challenge!

- [Automated Trading Bot](https://optionalpha.com/podcast/build-a-fully-automated-options-portfolio-with-3000-in-1-click)  
  A web app that lets users create automated trading bots, in the fashion of [Option Alpha](https://optionalpha.com/podcast/build-a-fully-automated-options-portfolio-with-3000-in-1-click). This requires frontend, backend, contract and bot development!

- ___Loans Against Yield-Bearing Instruments___  
  The only loan protocol on Optimism is Aave, which is fairly conservative in its design. Something that would particularly interesting it the ability to loan against collateral that is yield-bearing (since that collateral doesn't have any other possible use). It would also be great to be able to loan against Optimism-native tokens and instruments (Lyra, Perp, ...). On other networks, [Abracadabra Money](https://abracadabra.money/) is a project that does this (although in their case, they emit their own stablecoins). Multiple variations on the design are possible: isolated & permissionless lending pools (like [Rari Capital](https://rari.capital/)), own stablecoin (like Abracadabra), self-repaying loans (capture the yield for loan repayment, like [Alchemix](https://alchemix.fi/)).

- ___Your Idea?___  
  Open up a pull request and get your own idea included here!
