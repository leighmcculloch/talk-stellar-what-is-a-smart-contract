---
title: Smart Contracts on Stellar
sub_title: A Lunch & Learn
author: Leigh McCulloch
---

<!--
speaker_note: |
  Welcome everyone to this lunch and learn. Today we're going to talk about
  smart contracts on Stellar. I want to make this accessible, so I'm going
  to start from the basics and build up. No programming experience needed.
  By the end you'll understand what smart contracts are, why they matter,
  and what people are building with them on Stellar. Let's jump in.
-->

<!-- end_slide -->

Software Programs Are Everywhere
===

<!-- incremental_lists: true -->

- You use software programs every day

- Your phone, your laptop, your TV, your car

- They all run software written by people

- A program is just a set of instructions that a computer follows

<!--
speaker_note: |
  Let's start with something familiar. Software programs are everywhere.
  Think about everything you used today that had a screen or a chip in it.
  Your phone, your laptop, your smart TV, even your car. They all run
  software. And at its core, a program is just a set of instructions. A
  human writes those instructions, and a computer follows them. That's it.
  Now let's look at some specific examples you already know.
-->

<!-- end_slide -->

Programs on Your Phone
===

<!-- incremental_lists: true -->

- Apps with buttons you tap

- They store your data (photos, messages, settings)

- They talk to other programs over the internet

- They run on **your** device

<!--
speaker_note: |
  The most familiar kind of software is the apps on your phone. You open
  an app, you see buttons, you tap them, things happen. These apps store
  data like your photos and messages. They communicate with other programs
  over the internet. And they run right there on your device, in your
  pocket. You own the phone, you control the apps, you can delete them.
  But not all programs run on your phone.
-->

<!-- end_slide -->

Programs on Servers
===

<!-- incremental_lists: true -->

- Your email runs on someone else's computer

- Banking apps talk to the bank's servers

- These server programs have **APIs** -- ways for other programs to talk to them

- You trust the company running the server

<!--
speaker_note: |
  A lot of the programs you rely on don't actually run on your phone.
  When you check your email, the real work happens on a server somewhere.
  When you use a banking app, it's calling out to the bank's computers.
  These server programs expose what we call APIs. Think of an API like a
  menu at a restaurant. It lists the things you can ask for. You don't go
  into the kitchen yourself, you pick from the menu. And here's the key
  thing: you trust the company running that server. You trust Google with
  your email, you trust your bank with your money. That trust is the
  foundation. Now, what if we could run programs on a computer that nobody
  owns?
-->

<!-- end_slide -->

Programs on a Blockchain
===

<!-- incremental_lists: true -->

- What if a program ran on a computer **nobody** owns?

- It has an API, just like a server program

- It has storage, just like a server program

- It can emit events, just like a server program

- But no single person or company controls it

<!--
speaker_note: |
  This is the big idea. What if you could run a program on a computer that
  nobody owns? Not Google, not a bank, not any single company. A blockchain
  is a network of many computers that all agree on what the program does.
  And the programs that run on it look a lot like those server programs. They
  have APIs, so other programs can call them. They have storage, so they can
  remember things. They can emit events, so you can watch what happens. The
  difference is that no single person controls the computer they run on.
  That's a blockchain program. But we don't usually call them programs.
  We call them smart contracts.
-->

<!-- end_slide -->

Why "Smart Contracts"?
===

<!-- pause -->

**Nick Szabo**, 1994: coined the term

<!-- pause -->

Think of a **vending machine**:

<!-- incremental_lists: true -->

- You put in money

- You make a selection

- The machine checks if you paid enough

- It gives you the item -- no human involved

<!-- incremental_lists: false -->

<!-- pause -->

A smart contract is like a vending machine for **any agreement**

<!--
speaker_note: |
  The term "smart contract" was coined by a computer scientist named Nick
  Szabo in 1994. And he used a really simple analogy: a vending machine.
  Think about what a vending machine does. You put in money, you make a
  selection, the machine checks if you paid enough, and if you did, it gives
  you the item. No cashier, no negotiation, no trust needed. The rules are
  built into the machine. A smart contract is the same idea, but for any kind
  of agreement. You encode the rules into a program, put it on a blockchain,
  and it executes automatically. No middleman needed. So what makes this
  actually special?
-->

<!-- end_slide -->

What Makes Them Special?
===

<!-- incremental_lists: true -->

- **Nobody owns the computer** -- no single company can shut it down or change the rules

- **Transparent rules** -- anyone can inspect what the program does

- **Tamper-proof** -- once deployed, the code runs exactly as written

- **Always available** -- the network runs 24/7, no downtime

- **Composable** -- programs can call other programs, like building blocks

<!--
speaker_note: |
  So why does this matter? Why not just use a normal server? A few reasons.
  First, nobody owns the computer. No single company can shut it down or
  change the rules on you. Second, the rules are transparent. Anyone can
  look at the code and see exactly what it does. Third, it's tamper-proof.
  Once a contract is deployed, it runs exactly as written. Nobody can
  secretly change it. Fourth, the network runs 24/7. And fifth, these
  programs can call each other, like Lego blocks you can snap together.
  Now let's talk about Stellar specifically.
-->

<!-- end_slide -->

The Stellar Network
===

<!-- incremental_lists: true -->

- Founded in 2014 by Jed McCaleb

- Focused on **payments** and **financial access**

- Transactions settle in ~5 seconds

- Fees are a fraction of a cent

- Used for cross-border payments, stablecoins, and asset tokenization

<!--
speaker_note: |
  Stellar is a blockchain network that was founded in 2014 by Jed McCaleb.
  From the start, Stellar has been focused on real-world financial use cases.
  Payments, cross-border transfers, making financial services accessible to
  people who don't have bank accounts. It's fast. Transactions settle in about
  five seconds. And it's cheap. We're talking fractions of a cent per
  transaction. Not dollars, not even cents. Fractions of a cent. It's been
  used for cross-border payments, stablecoins like USDC, and tokenizing
  real-world assets. But for a long time, Stellar didn't have smart
  contracts.
-->

<!-- end_slide -->

Stellar Before Smart Contracts
===

<!-- incremental_lists: true -->

- 26 built-in operations (send payments, create offers, manage trust)

- A built-in decentralized exchange (orderbook)

- You could do a lot -- but only what was pre-built

- Want custom logic? You couldn't

- Like a phone with only pre-installed apps and no app store

<!--
speaker_note: |
  Before smart contracts, Stellar had 26 built-in operations. You could
  send payments, create trade offers, manage which assets you trust,
  and more. There was even a built-in decentralized exchange, an orderbook
  where people could trade assets directly. You could do a lot with
  Stellar. But only what was pre-built into the network. If you wanted
  custom logic, like a lending protocol, or an automated market maker,
  or a complex escrow -- you couldn't do it. Think of it like a phone
  that only has pre-installed apps and no app store. Useful, but limited.
  Then Soroban arrived.
-->

<!-- end_slide -->

Soroban Arrives
===

<!-- pause -->

**February 2024**: Smart contracts go live on Stellar

<!-- pause -->

<!-- incremental_lists: true -->

- **Soroban** is the name of Stellar's smart contract platform

- Contracts are written in **Rust** (a modern, safe programming language)

- Compiled to **WebAssembly** (runs on any computer, safely)

- Designed to be developer-friendly and predictable

- Stellar now has an **app store**

<!--
speaker_note: |
  In February 2024, smart contracts went live on Stellar. The platform
  is called Soroban. Contracts are written in Rust, which is a modern
  programming language known for being fast and safe. The Rust code gets
  compiled to something called WebAssembly, which is a format that can
  run on any computer safely, like a universal app format. Soroban was
  designed from the ground up to be developer-friendly, with predictable
  costs and clear error messages. Going back to our phone analogy, Stellar
  now has an app store. Anyone can write and deploy a new program. Let me
  show you what one looks like.
-->

<!-- end_slide -->

What Does a Contract Look Like?
===

<!-- pause -->

A minimal contract in Rust:

```rust
#[contract]
pub struct HelloContract;

#[contractimpl]
impl HelloContract {
    pub fn hello(env: Env, to: String) -> Vec<String> {
        vec![
            &env,
            String::from_str(&env, "Hello"),
            to,
        ]
    }
}
```

<!-- pause -->

- `hello` is the **API** -- anyone can call it
- You send it a name, it returns a greeting

<!--
speaker_note: |
  Don't worry about understanding every line. Here's what matters.
  This is a real, working smart contract written in Rust. It has one
  function called hello. That function is the API. Anyone can call it.
  You send it a name, and it returns a greeting. That's it.
  It's small, it's simple, and it's a real program running on a
  blockchain that nobody owns. Of course, real contracts do more
  interesting things. But the structure is the same. Let's zoom out
  and connect this back to our earlier analogy.
-->

<!-- end_slide -->

Contracts Are Little Server Apps
===

Just like server programs, smart contracts have:

<!-- pause -->

<!-- column_layout: [1, 1, 1] -->

<!-- column: 0 -->

**APIs**

Functions that
other programs
can call

<!-- column: 1 -->

**Storage**

Data that persists
between calls

<!-- column: 2 -->

**Events**

Notifications when
something happens

<!-- reset_layout -->

<!-- pause -->

The difference: they run on a network **nobody controls**

<!--
speaker_note: |
  Let's bring it back to where we started. Smart contracts are like
  little server applications. They have APIs, functions that other
  programs can call. They have storage, data that sticks around between
  calls. And they have events, notifications that something happened.
  The only difference from a regular server app is where they run. They
  run on a blockchain network that nobody controls. Same building
  blocks, different trust model. Now let's look at a real-world example
  that makes this concrete.
-->

<!-- end_slide -->

Real Example: Tokens
===

<!-- incremental_lists: true -->

- A **token** is a smart contract that tracks who owns what

- Think of it like a spreadsheet: names in one column, balances in another

- The contract enforces the rules: you can only send what you have

- Tokens can represent anything: dollars, euros, loyalty points, event tickets

- This is the most common use of smart contracts

<!--
speaker_note: |
  The most common thing people build with smart contracts is tokens. A
  token is just a contract that keeps track of who owns what. Think of
  it like a spreadsheet. One column has names, another has balances. The
  contract enforces simple rules, like you can't send more than you have.
  Tokens can represent anything. Dollars, euros, loyalty points, shares
  of stock, event tickets. It's the most basic and most powerful building
  block. And on Stellar, tokens have an interesting story.
-->

<!-- end_slide -->

Tokens on Stellar: Two Flavors
===

<!-- pause -->

**Classic Tokens** (since 2014)

- Built into the network
- Fast, cheap, simple
- Used for USDC, anchored fiat, and more

<!-- pause -->

**Soroban Tokens** (since 2024)

- Smart contracts with custom logic
- More flexible and programmable

<!-- pause -->

**The Bridge**: The Stellar Asset Contract (SAC)

- Wraps any classic token so smart contracts can use it
- Best of both worlds

<!--
speaker_note: |
  On Stellar there are two flavors of tokens. Classic tokens have been
  around since 2014. They're built into the network. Fast, cheap, simple.
  This is how USDC and other assets work on Stellar today. Then there are
  Soroban tokens, smart contracts that can have custom logic. Maybe a
  token that only lets you transfer during certain hours, or one that
  automatically takes a small fee. And here's the clever part: there's a
  bridge called the Stellar Asset Contract, or SAC. It wraps any classic
  token so that smart contracts can interact with it. So you get the
  speed and simplicity of classic tokens with the programmability of
  smart contracts. Best of both worlds. So what are people actually
  building?
-->

<!-- end_slide -->

What People Are Building
===

<!-- incremental_lists: true -->

- **Blend** -- lending and borrowing (like a decentralized bank)

- **Soroswap** -- token exchange (swap one asset for another instantly)

- **Cross-chain bridges** -- move assets between Stellar and other blockchains

- **USDC on Stellar** -- Circle's dollar stablecoin, used globally

- **Custom tokens** -- loyalty programs, community currencies, tokenized assets

<!--
speaker_note: |
  People are already building real things on Soroban. Blend is a lending
  and borrowing protocol. Think of it like a decentralized bank. You can
  deposit assets and earn interest, or borrow against what you've deposited.
  All the rules are in the smart contract. Soroswap lets you swap one asset
  for another instantly, without needing a traditional exchange. There are
  cross-chain bridges being built that let you move assets between Stellar
  and other blockchains like Ethereum. USDC, Circle's dollar stablecoin, is
  live on Stellar and used for real payments around the world. And of course
  people are creating custom tokens for all kinds of things. This is just
  the beginning. Now, how does Stellar compare to the biggest smart contract
  platform out there?
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

Different tools for different jobs -- not better or worse

<!--
speaker_note: |
  People always ask how Stellar compares to Ethereum, so let's do a quick
  comparison. Speed: Stellar settles in about 5 seconds, Ethereum in about
  12. Cost: Stellar transactions cost fractions of a cent. Ethereum can
  cost anywhere from 50 cents to over 50 dollars depending on network
  demand. Language: Stellar uses Rust, Ethereum uses Solidity. And
  philosophy: Stellar has always been focused on practical financial use
  cases, especially payments. Ethereum is more general purpose, trying to
  be a world computer for everything. Neither is better or worse. They're
  different tools for different jobs. Now let's step back and think about
  why any of this matters.
-->

<!-- end_slide -->

Why This Matters
===

<!-- incremental_lists: true -->

- **Programmable money** -- money that can follow rules automatically

- **Open access** -- anyone can build on it, no permission needed

- **Lower barriers** -- financial services without the traditional gatekeepers

- **Transparency** -- rules everyone can verify

- **New possibilities** -- things we haven't imagined yet

<!--
speaker_note: |
  So why does any of this matter? Because smart contracts give us
  programmable money. Money that can follow rules automatically, without
  needing a middleman. Open access means anyone, anywhere in the world,
  can build on this platform. You don't need permission from a bank or
  a tech company. Lower barriers means financial services can reach people
  who have been locked out of the traditional system. Transparency means
  the rules are visible to everyone, not hidden in some company's
  internal systems. And maybe most exciting: new possibilities we haven't
  even imagined yet. When you give people new building blocks, they build
  things you never expected. The internet started as a way to send
  research papers, and now it's... everything. Smart contracts are early.
  We're still figuring out what's possible.
-->

<!-- end_slide -->

<!-- jump_to_middle -->
<!-- alignment: center -->

Questions?

<!--
speaker_note: |
  That's the talk! Thank you for listening. I'd love to answer any
  questions you have. Nothing is too basic. If something didn't make
  sense, ask about it. If you want to go deeper on any topic, we can.
  And if you want to see a live demo of deploying a contract or
  interacting with one, I'm happy to do that too.
-->
