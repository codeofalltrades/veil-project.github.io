---
layout: post
lang: en
title: Announcing the architecture of the future Veil privacy protocol
date: 2019-05-22
author: gabrielnergaard
permalink: /blog/new-veil-protocol/
categories: test
excerpt: 'The Veil Project is excited to present the architecture of the new Veil privacy protocol, and the steps we are taking to ensure the interim privacy of our early adopters.'
description: 'The Veil Project is excited to present the architecture of the new Veil privacy protocol, and the steps we are taking to ensure the interim privacy of our early adopters.'
---

As regular followers are aware, [a recent series of exploits](https://veil-project.com/blog/zerocoin-exploit/) targeting the core protocol implementation library upon which most Zerocoin protocol cryptocurrencies rely had the following two impacts on the Veil Project:

1. We had to issue an emergency wallet release that, while protecting our user's funds from the exploit, had the downside of removing the anonymity feature of Zerocoin.

2. In the interest of our long-term mission, it forced us to make the difficult decision to move away from Zerocoin as the foundation of our privacy protocol.

We have been humbled at the support for this decision and the implicit vote of confidence that our community has demonstrated. In the spirit of keeping you informed, we have some exciting news to share.

## Protocol requirements and an emphasis on simplicity

The research for a new core protocol took place around the following set of requirements:

- Full-time privacy
- Only private transactions, with one coin type
- Private mining via the X16RT algorithm
- Private staking
- IP privacy (Dandelion)
- Fast transaction validation
- Minimized transaction sizes
- No denominations

The second requirement in the list—i.e. only one coin type—came from a lesson learned from the current Veil protocol, and that is the importance of *simplicity*. In order to provide full-time anonymity, the current protocol involves Zerocoin, RingCT, and CT. This resulted in incidental complexity in the wallet user experience, and so the future privacy protocol will specifically target avoiding such complexity.

## Identification of our new core privacy protocol

Based on the above requirements, the Veil development team, along with a number of individuals who are in discussion to join Veil Labs, have conducted an intense investigation into possible replacements for Zerocoin.

This investigation concluded in a core architecture specification for our new privacy protocol that we are excited to share with you now:

- The foundation of the Veil privacy protocol will be based on the work done by the **Zerocash** project. Similar to Veil's original protocol, Zerocash leveraged the stability of Bitcoin and the base anonymity of Zerocoin. Whereas Veil complemented Zerocoin with RingCT, Zerocash achieved anonymity through “Zero-Knowledge Succinct Non-interactive Arguments of Knowledge”, or zk-SNARKS, and an associated "decentralized anonymous payment" (or DAP) scheme. You can read more about Zerocash in the project's [white paper](http://zerocash-project.org/media/pdf/zerocash-extended-20140518.pdf).

- Veil will improve on Zerocash by replacing the Zerocash proof system with the advanced work known as **Sonic** from cryptographer and long-time colleague, Mary Maller, and her associates. Sonic proofs are zk-SNARKS from linear-size universal and updatable structured reference strings. Key benefits of Sonic include a near trustless and updatable setup, as well as improvements in computational scalability. You can learn more about Sonic in the team's [academic publication](https://eprint.iacr.org/2019/099.pdf).

We realize that's a lot to digest. For the moment, we simply wanted to outline the exciting new architecture of the Veil core privacy protocol, but you can be sure we'll be posting additional details and information in the coming months.

## Fixing Zerocoin in the meantime

A full transition to our new protocol, that will include a full audit by Least Authority, will be a complex and time-consuming endeavor. As we mentioned in a previous article, we estimate a minimum of ten to twelve months.

Recognizing the importance of privacy to our original Veil investors and early adopters, the Veil development team has also identified an approach to fix the current Zerocoin attack vectors, and will be releasing an updated wallet soon that restores full anonymity to Veil's Zerocoin implementation. For the curious, the solution is found in "non-interactive zero-knowledge proofs for composite statements" as outlined in this [technical publication](https://eprint.iacr.org/2018/557.pdf).

Some might question our decision to expend additional time, effort and cost on Zerocoin, given that we'll be migrating away from it in the future. As mentioned above, this decision is to respect the privacy needs and intents of our early adopters during the interim period as we develop the new network.

## Onward and upward!

We couldn't be more excited about the architecture that's been identified for the future Veil core privacy protocol. While the Zerocoin exploits and their impact on the Veil roadmap have certainly represented a setback, we now believe that in the long-run the situation will prove to be a blessing in disguise, as the new architecture will provide equivalent anonymity and improved scalability — all within a far simpler user experience.

Be sure to keep your eye on this space, as we provide updates and additional technical insights, as well as details regarding the process of migration as they become available. And as always, if you have any questions or comments, don't hesitate to contact the team in [Discord](https://discord.veil-project.com) or [Telegram](https://telegram.veil-project.com).

