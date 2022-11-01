# Optimism Infrastructure Project Ideas

You want to get involved in the fantastic world of blockchain/rollup
development, but you do not know how to get started? Fear not, this list of
projects is for you!

These projects are meant to develop the rollup itself (or its supporting
infrastructure), not decentralized apps on top of the rollup. For ideas on
those, please see [the main project idea list].

[the main project idea list]: /README.md

If you want to undertake any project on this list, or just want more information
feel free to reach out to @norswap (on Telegram, Twitter, or @optimism.io) for
extra details and guidance.

At OP Labs, we consider the following projects as extremely interesting, and
might be interested in [hiring] folks that demonstrate the ability to tackle
them!

[hiring]: https://boards.greenhouse.io/oplabs

We *might* also be interested to fund work on some of these projects, either
[retroactively] (preferably) or maybe even upfront if you can demonstrate
expertise and commitment. Please reach out for more details.

[retroactively]: https://medium.com/ethereum-optimism/retropgf-experiment-1-1-million-dollars-for-public-goods-f7e455cbdca

### Mini-Rollup

Pick your language of choice and create a MVP rollup. We recommend reading the
[Bedrock whitepaper][bedrock-wp] (work in progress!) to get familiar with rollup
architecture, and to peek at the [Bedrock specifications][bedrock-specs] for
details.

Try to simplify your rollup as much as possible — the goal is not to be
production ready. For instance, your rollup node may just post every single L2
transaction separately to L1 (which would be very wasteful in a real rollup).
You could also eschew the many complexity of fee logic and just charge a flat
fee for every transaction.

[bedrock-wp]: https://oplabs.notion.site/Whitepaper-WIP-v0-3-0d37e5c8a2ab45519b039d86e56d39e1
[bedrock-specs]: https://github.com/ethereum-optimism/optimism/tree/develop/specs

### Optimistic Data Feeds with Cannon

Our fault proof system [Cannon] allows a sequencer to make a claim about a
rollup's state root, and for other people to challenge this claim by playing a
*challenge game* which can result in a *fault proof* that the claimed state root
is incorrect (i.e. it does not result of the correct application of the state
transition function).

The same principle can be extended to many other use cases, allowing in general
*provable computation*: some people can make a claim about the output of a
program, and some other people can contest this claim and show that correct
execution of the program does not result in the claimed output.

Cannon is under development — its current state is a proof of concept that shows
how one can contest blocks of an EVM-based blockchain on the blockchain itself.

However, the principle can easily be extended to any computation that can be
compiled to the MIPS instruction set and does not make use of system calls. Many
useful such programs can be written in low level languages like Go, C and Rust.

This has already been done twice:

- [Zipline] — an Ethereum proof-of-stake light client proven using Cannon
  - The authors even made [a template][cannon-rust] for proving Rust programs
    with Cannon!
- Optimistic Gameboy (TBA) — a hack by [Nalin] that proves execution of a game
  boy emulator.

[Cannon]: https://github.com/ethereum-optimism/cannon
[Zipline]: https://github.com/willemolding/Zipline
[cannon-rust]: https://github.com/willemolding/rust-cannon-template
[Nalin]: https://twitter.com/nibnalin

So this task is to go wild and prove other kinds of computation on chain.
Particularly valuable are:

- Offloading expensive but useful computations, that can be served as a data
  feed on-chain.
- Light clients for other chains, which can serve as the basis for bridging.

### Alternative Instruction Set for Cannon

We're also interested in getting a Cannon-like system working with other
instruction sets besides MIPS. Relevant candidates are WebAssembly, RISC V and
JVM bytecode.

### Adapt Alternative Execution Clients for Bedrock

One of OP stack's components is the *execution engine*. In Bedrock, this is
implemented as a minimally modified Ethereum execution client. Currently, we
have modified versions of [go-ethereum][op-geth] and [erigon][op-erigon].

It shouldn't be too hard to adapt our changes to other execution clients!

[op-geth]: https://github.com/ethereum-optimism/op-geth
[op-erigon]: https://github.com/protolambda/erigon/tree/optimism

### Alternative Virtual Machine for the OP Stack

Not only can the OP stack accomodate alternative execution clients, it could
accomodate completely different execution engines, or different ways to run
transactions.

What if rollup smart contracts could be written in MIPS, WASM, RISC V, the JVM,
... ? Let's find out!

### Rollup Node Port in a Different Language

The main component of the OP stack is the *rollup node*, which is responsible
for deriving the L2 chain from the L1 source. The rollup node is currently
[implemented in Go][op-node], but we'd love to have alternative,
[spec-compliant][bedrock-specs] implementations — if possible written in other
languages.

This task is pretty heavy in scope, but if you're really proficient in your
language of choice and want to get really deep into the OP stack's
implementation, you might want to give it a shot.

[op-node]: https://github.com/ethereum-optimism/optimism/tree/develop/op-node

### Atomic Cross-Rollup Transactions

At Devcon VI, Norswap [presented][devcon-atomic] a vision / outline for how atomic
cross-shard/cross-rollup transactions could work in the future.

[devcon-atomic]: https://twitter.com/norswap/status/1584222557800366084

We're interested in prototyping and trying out the idea. Reach out if interested!

### Round-Robin Sequencing

Decentralizing the sequencer is an important endeavour in the quest for full
decentralization. This will done progressively, and one of our first step will
likely be to adopt a permissioned set of sequencers which will sequence the L2
chain in a round-robin fashion (i.e. one at a time).

We'd love your help in prototyping this change, which involves both Go and
Solidity work.

Beware that this is a time-sensitive opportunity however, as we might want to
move forward with sequencer decentralization relatively soon!

### Optimism MEV Explorer

While Optimism has at present a private mempool which prevents a lot of the MEV
extraction that we see on other chains, there is undibitably a lot of MEV
extraction going on. Arbitrages and liquidations don't disappear beause people
can't peer into the mempool.

We'd love to know more about the MEV activity on Optimism. If you have the
skills necessary to develop a MEV dashboard in the style of [MEV explore] and [Metablock],
please get in touch with us.

Also note that Flashbots has [expressed interest][flashbots-l2] in funding such
efforts.

[MEV explore]: https://explore.flashbots.net/
[Metablock]: https://mev.metablock.dev
[flashbots-l2]: https://collective.flashbots.net/t/quantifying-mev-on-l2s/450/7

### Alternative Solidity Compiler

It's no secret that the existing Solidity compiler, while receiving a lot of
work and love from a great team of volunteers, isn't exactly ideal. The compiler
has a lot of tech debt that it's hard to get rid of while pushing the language
forward.

We'd love to see efforts to create a competing solidity compilers, using new
greenfield designs!
