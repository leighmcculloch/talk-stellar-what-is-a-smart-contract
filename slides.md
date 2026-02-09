---
title: Smart Contracts on Stellar
sub_title: A Lunch & Learn
author: Leigh McCulloch
---

<!--
speaker_note: |
  Welcome everyone to this lunch and learn. Today we're going to talk about
  smart contracts on Stellar. No programming experience needed. But first,
  let's talk about something you already know.
-->

<!-- end_slide -->

Let's Talk About Vending Machines
===

What does a vending machine do?

<!-- incremental_lists: true -->

- You put in money

- You make a selection

- The machine checks if you paid enough

- It gives you the item

- It gives you change

<!-- incremental_lists: false -->

<!-- pause -->

No cashier. No negotiation. The **rules enforce themselves**

<!--
speaker_note: |
  Before we talk about smart contracts, let's talk about vending machines.
  What does a vending machine actually do? You put in money. You make a
  selection. The machine checks if you paid enough. It gives you the item.
  It gives you change. No cashier involved. No negotiation. No trust
  required. The rules enforce themselves. You and the machine follow the
  same set of rules, and the transaction just happens. Okay, so why am I
  talking about vending machines at a talk about smart contracts?
-->

<!-- end_slide -->

Why Are We Talking About Vending Machines?
===

<!-- pause -->

A vending machine is an **agreement**

<!-- pause -->

_If you put in the right amount of money, you will get something out_

<!-- pause -->

<!-- incremental_lists: true -->

- First implemented in **hardware** -- gears, springs, coin slots

- Now most vending machines run **software** too

- The first swap program -- money in, item out

- No middleman. The machine **is** the agreement

<!--
speaker_note: |
  Because a vending machine is an agreement. Think about that. It's a
  promise: if you put in the right amount of money, you will get something
  out. That agreement was first implemented in hardware. Gears, springs,
  coin mechanisms. Purely mechanical. But today most vending machines also
  run software. The agreement went from hardware to code. And when you
  think about it this way, a vending machine is the first swap program that
  ever existed. Money in, item out. No middleman. The machine itself is
  the agreement. It enforces the terms automatically. That idea, that
  pattern, is older than you might think.
-->

<!-- end_slide -->

The Ancestor of Smart Contracts
===

<!-- incremental_lists: true -->

- Vending machines have been around since the **1880s**

- For over a century: automated agreements, no human in the middle

- In **1994**, a computer scientist named **Nick Szabo** saw the connection

- He called the vending machine the **ancestor of smart contracts**

- This was 14 years before Bitcoin

<!--
speaker_note: |
  Vending machines have been around since the 1880s. For over a century,
  they've been doing the same thing: enforcing agreements automatically,
  no human in the middle. In 1994, a computer scientist and legal scholar
  named Nick Szabo looked at vending machines and saw something most people
  miss. He called them the ancestor of smart contracts. He coined that
  term, "smart contract," 14 years before Bitcoin existed, before any
  blockchain. He was part of the cypherpunk movement, a mailing list of
  cryptographers and activists who believed cryptography could reshape
  society. Most of them were focused on encryption and privacy. But Szabo
  had a law background, so he was thinking about agreements. And he asked:
  what if we could take that vending machine pattern and put it everywhere?
-->

<!-- end_slide -->

What is a Smart Contract?
===

<!-- incremental_lists: true -->

- Take the vending machine pattern -- an agreement that enforces itself

- Remove the physical machine

- Put the logic on a network of computers that **nobody owns**

- Now anyone, anywhere, can use it

- The rules still enforce themselves -- no human in the middle

- That's a smart contract

<!--
speaker_note: |
  So what is a smart contract? Take the vending machine pattern. An
  agreement that enforces itself. Now remove the physical machine. No metal
  box, no glass front. Just the logic. Put that logic on a network of
  computers that nobody owns. Not one company's server, but a shared
  network. A blockchain. Now anyone in the world can walk up to this
  digital vending machine and use it. The rules still enforce themselves
  automatically. No middleman. That's a smart contract. An agreement that
  enforces itself, running on a computer nobody controls. And just like a
  real vending machine, it can do a lot more than sell snacks.
-->

<!-- end_slide -->

What Makes This Vending Machine Special?
===

A regular vending machine vs. a smart contract:

<!-- pause -->

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

**Regular Machine**

- The company owns it
- They set the prices
- They can change the rules
- You trust the operator
- One location

<!-- column: 1 -->

**Smart Contract**

- Nobody owns the computer
- Rules are transparent
- Code can't be secretly changed
- Trust the code, not a company
- Available to anyone, anywhere

<!-- reset_layout -->

<!--
speaker_note: |
  So what makes a smart contract different from a regular vending machine?
  A regular machine is owned by a company. They set the prices, they can
  change the rules, you trust the operator to keep the machine stocked and
  honest. And it's in one physical location.

  A smart contract flips all of that. Nobody owns the computer it runs on.
  The rules are transparent, anyone can inspect the code. Nobody can
  secretly change how it works after it's deployed. You trust the code
  itself, not a company. And it's available to anyone with an internet
  connection, anywhere in the world. Same basic pattern as the vending
  machine, but without the limitations of physical hardware and single
  owners. Now let's talk about a specific network where these digital
  vending machines run.
-->

<!-- end_slide -->

The Stellar Network
===

<!-- incremental_lists: true -->

- A blockchain network founded in 2014

- Focused on **payments** and **financial access**

- Transactions settle in ~5 seconds

- Fees are a fraction of a cent

- Think of it as a place where vending machines can be deployed

<!--
speaker_note: |
  Stellar is a blockchain network founded in 2014. From the start it's been
  focused on real-world financial use cases. Payments, cross-border
  transfers, making financial services accessible to people who don't have
  bank accounts. It's fast: transactions settle in about five seconds. And
  it's cheap: fractions of a cent per transaction. If we're sticking with
  our analogy, think of Stellar as a location where you can deploy vending
  machines. A big open plaza where anyone can set one up and anyone can
  walk up and use one. But for a long time, Stellar only had one kind of
  machine.
-->

<!-- end_slide -->

Stellar's Old Vending Machine
===

<!-- incremental_lists: true -->

- 26 built-in operations (send payments, create trade offers, manage trust)

- A built-in decentralized exchange

- Like a vending machine with **26 preset buttons**

- Useful -- but you couldn't add new buttons

- You couldn't change what it dispenses

- Want a machine that does something new? Not possible

<!--
speaker_note: |
  Before smart contracts, Stellar had 26 built-in operations. You could
  send payments, create trade offers on a built-in exchange, manage which
  assets you trust. It was like a vending machine with 26 preset buttons.
  Press button 1, send a payment. Press button 14, create a trade offer.
  Useful! But you couldn't add new buttons. You couldn't change what the
  machine dispenses. If you wanted something that wasn't one of those 26
  operations, like a lending protocol, or an automated market maker, or
  conditional escrow, you were stuck. You had to ask the network to add
  a new button, and that meant getting everyone to agree on a protocol
  upgrade. Then something changed.
-->

<!-- end_slide -->

Soroban: A Programmable Vending Machine
===

<!-- pause -->

**February 2024**: Smart contracts go live on Stellar

<!-- pause -->

<!-- incremental_lists: true -->

- **Soroban** is the name of Stellar's smart contract platform

- Written in **Rust**, compiled to **WebAssembly**

- Now anyone can build a **new vending machine** with custom rules

- Not just 26 buttons -- unlimited possibilities

- The old preset buttons still work too

<!--
speaker_note: |
  In February 2024, smart contracts went live on Stellar. The platform is
  called Soroban. Contracts are written in Rust, a modern programming
  language, and compiled to WebAssembly, a format that can run anywhere
  safely. Here's what changed: before Soroban, Stellar had one vending
  machine with 26 preset buttons. Now anyone can build a brand new vending
  machine with whatever buttons they want. Whatever rules they want.
  Whatever it dispenses. And the old preset buttons still work too. It's
  the difference between a fixed menu and a full kitchen. Let me show you
  what one of these custom machines looks like on the inside.
-->

<!-- end_slide -->

A Basic Swap
===

The simplest vending machine: put something in, get something out

<!-- pause -->

```
 ┌─────────────────────────┐
 │    SODA MACHINE          │
 │                          │
 │  Alice inserts $2.00     │
 │  Alice presses B4        │
 │  Machine dispenses Soda  │
 │  Machine returns $0.25   │
 │                          │
 └─────────────────────────┘
```

<!-- pause -->

The machine prints a receipt -- every event that happened:

```
Event: received $2.00 from Alice
Event: dispensed 1 Soda to Alice
Event: returned $0.25 to Alice
```

<!--
speaker_note: |
  Let's see what vending machines people are building. We'll start with
  the simplest one: a basic swap. This is the vending machine you already
  know. Alice puts in two dollars, presses a button, gets a soda, gets her
  change. And the machine prints a receipt. Every smart contract works the
  same way. Every time something happens, it emits events. Think of events
  as receipts. A log of exactly what happened, in order. Received two
  dollars from Alice. Dispensed one soda to Alice. Returned 25 cents to
  Alice. Anyone can read these receipts. They're public, permanent, and
  they tell the full story of what the machine did. Now, what if the swap
  involves two different machines?
-->

<!-- end_slide -->

Two Machines, One Swap
===

What if Alice wants to swap USDC for EUR?

<!-- pause -->

That takes **two** vending machines working together:

<!-- pause -->

```
 ┌──────────────┐          ┌──────────────┐
 │ USDC MACHINE │          │ EUR MACHINE  │
 │              │          │              │
 │  holds USDC  │◄────────►│  holds EUR   │
 │  balances    │  swap    │  balances    │
 │              │ contract │              │
 └──────────────┘          └──────────────┘
```

<!-- pause -->

Events from **three** contracts:

```
Swap:  swap 100 USDC for 92 EUR for Alice
USDC:  transferred 100 USDC from Alice to Pool
EUR:   transferred 92 EUR from Pool to Alice
```

<!--
speaker_note: |
  What if Alice doesn't want a soda? What if she wants to swap one
  currency for another? Say she has USDC, US dollars, and wants EUR, euros.
  Now we need two vending machines. One that holds USDC balances, and one
  that holds EUR balances. And a swap contract that coordinates between
  them. Alice walks up to the swap machine, puts in 100 USDC, and gets
  92 EUR back. But look at the receipts. There are events from three
  contracts now. The swap contract says: swapped 100 USDC for 92 EUR for
  Alice. The USDC machine says: transferred 100 USDC from Alice to the
  pool. The EUR machine says: transferred 92 EUR from the pool to Alice.
  Each machine keeps its own receipts, and together they tell the whole
  story. But where does that pool of USDC and EUR come from?
-->

<!-- end_slide -->

A Liquidity Pool
===

A machine where people **deposit** assets so others can **swap**

<!-- pause -->

```
 ┌──────────────────────────────────┐
 │         LIQUIDITY POOL           │
 │                                  │
 │  Contains: 10,000 USDC          │
 │            10,000 EUR            │
 │                                  │
 │  Depositors earn fees from       │
 │  every swap that happens         │
 └──────────────────────────────────┘
```

<!-- pause -->

Events tell the story:

```
Event: Alice deposited 1,000 USDC + 1,000 EUR
Event: Bob swapped 100 USDC for 92 EUR (fee: 0.3%)
Event: Carol swapped 50 EUR for 54 USDC (fee: 0.3%)
Event: Alice withdrew 1,002 USDC + 998 EUR + fees
```

<!--
speaker_note: |
  A liquidity pool. This is one of the most important vending machines in
  all of crypto. Here's how it works. People like Alice deposit assets into
  the machine. She puts in 1,000 USDC and 1,000 EUR. Now the machine has
  a pool of both currencies. When Bob comes along and wants to swap 100
  USDC for EUR, the machine can do that trade using the pool. Bob pays a
  small fee, say 0.3 percent. Carol comes along and swaps the other
  direction, EUR for USDC, also pays a fee. Those fees go to Alice and
  the other depositors. When Alice is ready, she withdraws her share plus
  the fees she earned. Look at the events. Each one is a receipt. Deposit,
  swap, swap, withdraw. The whole history of the machine, right there. On
  Stellar, this is what protocols like Soroswap do. Now let's look at one
  more kind of machine.
-->

<!-- end_slide -->

A Token Machine
===

A machine that **creates** tokens and tracks who holds them

<!-- pause -->

```
 ┌──────────────────────────────────┐
 │         TOKEN MACHINE            │
 │                                  │
 │  Token: LOYALTY                  │
 │  Total supply: 0 (so far)       │
 │                                  │
 │  Buttons: mint, transfer, redeem │
 └──────────────────────────────────┘
```

<!-- pause -->

Events:

```
Event: minted 1,000 LOYALTY to Alice
Event: Alice transferred 200 LOYALTY to Bob
Event: Bob redeemed 200 LOYALTY for a reward
```

<!-- pause -->

Tokens can represent anything: dollars, loyalty points, tickets, shares

<!--
speaker_note: |
  The last machine I want to show you is a token machine. This one doesn't
  hold a pool of assets. It creates them. It mints tokens. Think of a
  loyalty program. The machine has a mint button: press it, and new LOYALTY
  tokens are created and given to someone. Alice gets 1,000 LOYALTY tokens.
  She can hold them. She can transfer some to Bob. And Bob can come back
  to the machine and redeem them for a reward. Every step is an event. A
  receipt. Minted 1,000 to Alice. Alice transferred 200 to Bob. Bob
  redeemed 200 for a reward. The machine tracks every balance, every
  transfer, every redemption. And tokens can represent anything. Dollars
  like USDC. Loyalty points. Event tickets. Shares of a company. On
  Stellar, USDC works exactly like this. Circle mints USDC tokens, people
  hold them and transfer them, and you can redeem them for real dollars.
-->

<!-- end_slide -->

Stellar vs Ethereum
===

<!-- pause -->

|                  | **Stellar (Soroban)** | **Ethereum**          |
|------------------|-----------------------|-----------------------|
| **Speed**        | ~5 seconds            | ~12 seconds           |
| **Cost**         | Fractions of a cent   | $0.50 -- $50+         |
| **Language**     | Rust                  | Solidity              |
| **Philosophy**   | Practical, payments   | General purpose       |

<!-- pause -->

Different manufacturers, different strengths -- not better or worse

<!--
speaker_note: |
  People always ask how Stellar compares to Ethereum. Think of them as
  different vending machine manufacturers. Stellar is fast, about 5 seconds
  per transaction. Ethereum takes about 12. Stellar is cheap, fractions of
  a cent. Ethereum can cost anywhere from 50 cents to over 50 dollars when
  the network is busy. Stellar uses Rust, Ethereum uses a language called
  Solidity. And in terms of philosophy: Stellar has always focused on
  practical financial use cases, especially payments. Ethereum aims to be
  more general purpose.

  Neither is better or worse. Different manufacturers, different strengths.
  You pick the one that fits what you're building.
-->

<!-- end_slide -->

Vending Machines Everywhere
===

<!-- incremental_lists: true -->

- We started with a simple vending machine -- money in, soda out

- Then two machines working together to swap currencies

- Then a pool where people deposit assets and earn fees

- Then a machine that creates tokens from nothing

- Each one is just an **agreement that enforces itself**

- **Open, transparent, no gatekeepers** -- anyone can build one, anyone can use one

<!--
speaker_note: |
  Let's step back and look at what we covered. We started with a simple
  vending machine. Money in, soda out. Then we connected two machines to
  swap currencies. Then we built a pool where people deposit assets and
  others can trade against them, with depositors earning fees. Then we
  built a machine that creates tokens from nothing, tokens you can hold,
  transfer, or redeem. Each one is just an agreement that enforces itself.
  The same pattern Nick Szabo saw in a vending machine in 1994. And they're
  all open. Anyone can build a machine. Anyone can use one. Anyone can read
  the receipts. No gatekeepers. We're still early. People are still
  inventing new kinds of machines. And that's what makes this exciting.
-->

<!-- end_slide -->

<!-- jump_to_middle -->
<!-- alignment: center -->

Questions?

<!--
speaker_note: |
  That's the talk! Thank you for listening. I'd love to answer any questions.
  Nothing is too basic. If something didn't make sense, ask about it. If you
  want to go deeper on any topic, we can. And if you want to see a live demo
  of deploying a contract or interacting with one, I'm happy to do that too.
-->
