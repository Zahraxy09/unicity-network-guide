# unicity-network-guide
A complete guide to Unicity Network: off-chain execution infrastructure for the autonomous agentic internet, built by the team behind Guardtime's KSI blockchain (Estonia, NATO, DARPA, NHS) — covering the 5-layer architecture and SphereQuests testnet.
# Unicity Network — Infrastructure for the Autonomous Agentic Internet

> A complete educational guide to Unicity: the off-chain execution protocol built by the team behind Guardtime (Estonia, DARPA, NATO, NHS), how it replaces shared ledgers with peer-to-peer cryptographic objects, the five-layer architecture, and how to participate in the SphereQuests testnet campaign.

---

## Table of Contents

1. [What Is Unicity?](#what-is-unicity)
2. [The Team Behind It — Guardtime's Legacy](#the-team-behind-it--guardtimes-legacy)
3. [The Problem Unicity Solves](#the-problem-unicity-solves)
4. [Core Innovation — No Shared Ledger](#core-innovation--no-shared-ledger)
5. [The Five-Layer Architecture](#the-five-layer-architecture)
6. [How a Transaction Actually Works](#how-a-transaction-actually-works)
7. [Agent Execution — Built for AI, Not Just Humans](#agent-execution--built-for-ai-not-just-humans)
8. [Offline and Mobile Capabilities](#offline-and-mobile-capabilities)
9. [Working Demonstrations](#working-demonstrations)
10. [Funding and Backers](#funding-and-backers)
11. [SphereQuests — The Testnet Campaign](#spherequests--the-testnet-campaign)
12. [How to Participate — Step by Step](#how-to-participate--step-by-step)
13. [Unicity vs Traditional Blockchains](#unicity-vs-traditional-blockchains)
14. [Risks and Open Questions](#risks-and-open-questions)
15. [Conclusion](#conclusion)

---

## What Is Unicity?

**Unicity** is a blockchain-adjacent protocol designed for what its team calls the **"Autonomous Agentic Internet"** — a future where AI agents, not just humans, are the primary economic actors making payments, negotiating contracts, and coordinating transactions without human intervention.

Unicity is the first blockchain platform designed for the Autonomous Agentic Internet — a new digital paradigm where AI agents, not just humans, are the primary economic actors. In this new era, agents require more than just payment rails; they need a verifiable, trustless environment to execute complex logic, manage state, and interact with the world.

The core architectural bet is unusual: instead of building a faster shared ledger (the approach every blockchain since Bitcoin has taken), Unicity removes the shared ledger from the transaction path entirely.

> *"We're not building another marketplace or trading platform. We're building the infrastructure beneath them."* — Mike Gault, CEO of Unicity Labs

---

## The Team Behind It — Guardtime's Legacy

This is what makes Unicity stand out from most Web3 projects: a team with a genuine, verifiable track record in cryptographic infrastructure deployed at national and military scale.

### Guardtime — The Predecessor Company

The Unicity Labs team previously built and exited **Guardtime**, a cybersecurity infrastructure company. Guardtime created **KSI (Keyless Signature Infrastructure)** blockchain technology, which has real-world deployment history:

```
KSI Blockchain — Real Deployments:
  - Estonian government: securing the national digital registry
    (used by Estonia's e-Residency and digital state infrastructure)
  - NATO: adopted for network and data security
  - US Department of Defense: cybersecurity applications
  - NHS (UK National Health Service): healthcare data integrity
```

KSI is used for making networks, systems and data secured, fast and efficient, all while retaining total data privacy. The technology developed from KSI is even used by NATO and the US Department of Defense.

This is the "team behind Estonia, DARPA, NATO, and the NHS" referenced in Unicity's own marketing — and unlike many crypto projects that exaggerate credentials, this lineage is independently documented in government and defense procurement records.

### Leadership

**Mike Gault** — CEO and Founder of Unicity Labs, previously CEO of Guardtime. A recognized figure in applied cryptography with a track record of shipping infrastructure that governments and militaries actually deployed — a rare credential in the Web3 space.

The founding team includes PhD researchers in distributed systems, cryptography, and machine learning — continuing the same technical caliber that built KSI.

### Unicity Foundation

The company has established the **Unicity Foundation** in Zug, Switzerland — Crypto Valley — to oversee protocol governance, grant funding, and open-source development, separating commercial development (Unicity Labs) from protocol stewardship (the Foundation), a structure common among serious infrastructure projects.

---

## The Problem Unicity Solves

### The AI Agent Economy Is Coming

AI agents are making purchases, negotiating contracts, allocating resources, and coordinating economic activity, all without human intervention. The global agentic AI market is projected to exceed $100 billion by 2032.

But the infrastructure to support this doesn't exist yet:

```
PROBLEM 1: SCALE
  Existing infrastructure was built for humans clicking buttons,
  not agents executing millions of transactions per second.
  The architecture assumes human latency tolerance. Agents have none.

PROBLEM 2: THE CENTRALIZATION TRADE-OFF
  Option A: Centralize through big tech → fast, but you sacrifice
            trustlessness and create surveillance infrastructure
  Option B: Use traditional blockchains → trustless, but consensus
            delays throttle throughput when millions of agents
            need to transact simultaneously

PROBLEM 3: SHARED LEDGER BOTTLENECK
  Every blockchain since Bitcoin uses the same shared ledger design.
  Every transaction must be processed and recorded in a global state.
  This doesn't scale to machine-speed, machine-volume transactions.

PROBLEM 4: PLATFORM RISK
  Platforms that aggregate transactions become surveillance
  infrastructure. Every agent interaction flows through servers
  controlled by third parties who extract fees, impose rules,
  and could shut down access at will.
```

Satoshi's whitepaper was titled "Peer-to-Peer Electronic Cash." Seventeen years later, we still don't have true peer-to-peer or electronic cash — every transaction still routes through shared ledgers, introducing unnecessary bottlenecks.

---

## Core Innovation — No Shared Ledger

This is Unicity's central architectural departure from every other blockchain.

### Traditional Blockchain Model

```
Transaction occurs
        ↓
Broadcast to entire network
        ↓
Every node processes and validates
        ↓
Consensus mechanism orders all transactions globally
        ↓
Transaction recorded in shared, global ledger
        ↓
Every node stores a copy of the full history

Problem: Throughput is bounded by the slowest honest node
         and the consensus mechanism's speed
```

### Unicity's Model

Rather than broadcasting full transaction data to all network participants, Unicity maintains only a minimal aggregation layer. The system separates transactions from validation — a common constraint in shared-ledger systems is removed because the network confirms an asset's uniqueness rather than processing the full context of each transaction.

```
Transaction occurs (off-chain, between two parties)
        ↓
Execution happens entirely off-chain
   (peer-to-peer cryptographic state transition)
        ↓
A minimal proof is submitted to the Aggregation Layer
   ("this token state was spent, here's the proof")
        ↓
Aggregation Layer checks: has this exact state been spent before?
   (prevents double-spending — this is the ONLY global check needed)
        ↓
Inclusion proof returned — transaction is final

Result: The network's job per transaction shrinks dramatically.
        Adding more participants doesn't bottleneck throughput
        the way it does in shared-ledger systems.
```

### Off-Chain Execution, On-Chain Anchor

Unicity solves the scalability and privacy bottlenecks of traditional blockchains by shifting all execution off-chain, leaving the blockchain to serve as a pure trust anchor.

```
OFF-CHAIN EXECUTION:
  Agent logic runs entirely off-chain
  Ensures unlimited scalability and privacy
  Full transaction details stay between the parties involved

ON-CHAIN SECURITY:
  The blockchain anchors state transitions
  Prevents double-spending and ensures finality
  Does NOT execute the logic itself — just confirms uniqueness
```

---

## The Five-Layer Architecture

Unicity's modular architecture demonstrates how this vision translates into practical implementation. The system combines five distinct layers, each serving a specific purpose while maintaining interoperability with the others.

```
┌─────────────────────────────────────────────────┐
│  Layer 5: AGENT EXECUTION                        │
│  Verifiable computation environment for AI agents│
└─────────────────────────────────────────────────┘
┌─────────────────────────────────────────────────┐
│  Layer 4: STATE TRANSITION LAYER                 │
│  Off-chain asset management                      │
└─────────────────────────────────────────────────┘
┌─────────────────────────────────────────────────┐
│  Layer 3: SPARSE MERKLE TREES                    │
│  Trustless aggregation                            │
└─────────────────────────────────────────────────┘
┌─────────────────────────────────────────────────┐
│  Layer 2: BFT CONSENSUS                          │
│  Byzantine Fault Tolerant — rapid state commits  │
└─────────────────────────────────────────────────┘
┌─────────────────────────────────────────────────┐
│  Layer 1: PROOF OF WORK FOUNDATION               │
│  Bitcoin fork with RandomX hashing                │
└─────────────────────────────────────────────────┘
```

### Layer 1 — Proof of Work Foundation

The foundation of Unicity's security model rests on a Proof of Work consensus mechanism implemented as a Bitcoin fork. The system uses the RandomX hash function, which provides ASIC resistance and promotes decentralized mining participation. With a two-minute block time, the layer provides faster finality than Bitcoin while maintaining the security properties of Proof of Work consensus.

```
Why RandomX instead of SHA-256?
  SHA-256 (Bitcoin) → dominated by specialized ASIC hardware
                    → mining centralizes around a few large operations

  RandomX → designed to be efficiently mined on general-purpose CPUs
          → lowers barriers to mining participation
          → promotes decentralization
```

This layer serves as the ultimate trust anchor. New **Alpha tokens** are mined here and can be extracted for use in higher layers, particularly the Agent Execution environment.

### Layer 2 — BFT Consensus

A Byzantine Fault Tolerant consensus layer that provides rapid, deterministic finality on top of the PoW foundation — verifying the integrity of the Aggregation Layer's state transitions.

### Layer 3 — Sparse Merkle Trees (Aggregation Layer)

The Aggregation Layer implements the Unicity Service, maintaining a global append-only registry of spent token states. It provides inclusion and non-inclusion proofs, processes state certification requests, and allows the Execution Layer to avoid the risk of double-spending. The layer is sharded for scalability, clustered for high availability, and uses cryptographic consistency proofs to maintain trustless operation.

This is the layer that prevents double-spending — the one piece of global coordination the system actually needs.

### Layer 4 — State Transition Layer

The Execution Layer handles transaction processing, smart contract execution (implemented through programmable stateful spending conditions called "predicates"), and business logic. This layer operates off-chain and is managed by users and agents who are interested parties in transaction validation and ordering.

### Layer 5 — Agent Execution Environment

The newest and most distinctive layer — a verifiable computation environment specifically designed for autonomous AI agents to execute logic, manage state, and transact with other agents.

---

## How a Transaction Actually Works

Based on the formal protocol description, here's the technical flow when value moves between two parties:

```
Step 1: Sender has a token in state (pk, hst)
        (pk = public key, hst = hash of state)

Step 2: Sender wants to transfer to recipient's public key pk'

Step 3: Sender computes H(hst, htx) — a hash combining
        current state and the new transaction details

Step 4: Sender signs this hash and submits a certification
        request Q = (pk, hst, htx, σ) to the Unicity Service
        (this is the ONLY interaction with the network layer)

Step 5: Unicity Service checks: has H(pk, hst) been registered before?
        If NOT (meaning: this exact state hasn't been spent) →
        records the mapping and returns an inclusion proof

Step 6: This inclusion proof is cryptographic evidence that:
        "This specific token state was validly spent, once, here"

Step 7: Recipient now holds a token in a new state,
        with cryptographic proof of valid provenance

Result: No global broadcast. No mempool. No need for every
        node to process this transaction. Just one minimal
        check against the Aggregation Layer.
```

The mechanism ensures that each token state can be spent at most once — solving double-spending with minimal global coordination rather than full transaction broadcast.

---

## Agent Execution — Built for AI, Not Just Humans

This is Unicity's defining use case, and what distinguishes it from general-purpose blockchains retrofitting "AI features."

### What Agents Need That Humans Don't

```
Human transacting:                Agent transacting:
  Tolerates 10-second waits         Needs sub-second finality
  Makes 1-10 transactions/day       May make millions/day
  Reviews each transaction          Acts autonomously, no review
  Uses a wallet UI                  Needs programmatic API/SDK
  Trusts based on reputation        Needs cryptographic verification
```

### The Agent Assembly / Sphere SDK

Unicity provides an SDK for autonomous economic agents: give an agent an identity, a wallet, and the ability to find, negotiate with, and settle with other agents — peer-to-peer, with perfect privacy and ultra-fast finality.

```python
# Conceptual illustration of the agent capability model
# (illustrative — actual SDK syntax may differ)

class UnicityAgent:
    """
    An autonomous economic agent on the Unicity network
    """
    def __init__(self, identity, wallet):
        self.identity = identity      # Cryptographic identity
        self.wallet = wallet          # Off-chain managed funds

    def discover_services(self, query):
        """Find other agents offering relevant services"""
        pass

    def negotiate(self, counterparty_agent, terms):
        """Peer-to-peer negotiation, no intermediary"""
        pass

    def settle(self, counterparty, amount):
        """
        Execute off-chain state transition
        Submit minimal proof to Aggregation Layer
        Achieve finality without broadcasting full transaction
        """
        pass
```

### AI Marketplace Demo

The AI Marketplace demo illustrates how the platform can support massive scale micropayments for agent-to-agent transactions. This application would be impractical on traditional blockchain networks due to transaction costs and throughput limitations, but operates efficiently in Unicity's off-chain environment.

This is the key practical claim: **micropayments between AI agents at scale** — something that gas fees and global consensus make economically impossible on Ethereum-style blockchains.

---

## Offline and Mobile Capabilities

A surprising and practical feature set: Unicity tokens can move without internet connectivity.

### Bluetooth Mesh and NFC

Mobile payment capabilities extend Unicity's reach into everyday transactions through NFC and Bluetooth mesh networking. These features enable offline token transfers using JSON-based protocols, allowing payments to occur even without internet connectivity.

```
BitChat Mobile Payment System:
  Uses Bluetooth mesh networks
  Creates resilient payment networks
  Functions independently of traditional internet infrastructure

Use cases:
  - Disaster zones with no connectivity
  - Remote areas without internet access
  - Privacy-conscious peer-to-peer payments (no ISP visibility)
  - Crowd events with overloaded cellular networks
```

This connects directly to Unicity's off-chain execution model — since transactions don't require broadcasting to a global network in real time, the cryptographic state transition can happen locally (via Bluetooth/NFC) and be settled with the Aggregation Layer whenever connectivity is restored.

---

## Working Demonstrations

Unicity has shipped several proof-of-concept applications that validate the architecture beyond whitepaper claims:

### Gaming — Quake on Unicity Agents

The Quake demonstration running on Unicity agents proves the architecture can support real-time, interactive applications. Everything in these games exists as tokens — from characters to items to game state — while maintaining native performance without centralized servers.

This is a meaningful technical demonstration: real-time gaming requires extremely low latency, which is historically impossible on shared-ledger blockchains. Demonstrating it on Unicity validates the off-chain execution claim.

### Cross-Chain Bridging

Cross-chain bridging allows tokens from other blockchain networks to be moved into Unicity's off-chain execution environment. This bridging mechanism differs fundamentally from traditional approaches by actually moving assets rather than creating wrapped representations, eliminating many security risks associated with conventional bridge designs.

```
Traditional bridges:        Unicity's approach:
  Lock asset on Chain A        Actually move the asset
  Mint wrapped asset on B      No wrapped representation
  Risk: bridge hack drains     Risk: reduced (no synthetic asset
        locked collateral            backed by a vulnerable contract)
```

### Digital Product Passports

The DigiPass integration demonstrates supply chain and authentication use cases requiring both digital verification and offline functionality — enabling offline verification of product authenticity and provenance.

---

## Funding and Backers

### Seed Round — $3 Million (February 2026)

```
Lead investor:    Blockchange Ventures
                   (NY-based VC, exclusively early-stage blockchain)

Participants:      Tawasal — Middle East communications super app
                   Outlier Ventures — leading Web3 early-stage investor
```

"The industry has spent a decade optimizing shared ledgers. Unicity asked a different question entirely: what if agents don't need a shared ledger at all? That architectural shift is what makes massive scale agent-to-agent commerce possible." — Dimitrios Chatzianagnostou, CIO of Outlier Ventures

### Why This Round Matters

A $3M seed round is modest by crypto infrastructure standards — but the signal is in **who** is backing it and **why**. Outlier Ventures has a long track record specifically in Web3 infrastructure plays (not speculative tokens), and the explicit framing around agentic AI infrastructure — rather than generic "blockchain platform" — reflects a thesis-driven investment rather than hype-chasing.

---

## SphereQuests — The Testnet Campaign

**SphereQuests** (quest.unicity.network) is Unicity's incentivized testnet campaign.

SphereQuests is Unicity's incentivised testnet campaign. Complete quests, test real infrastructure built on the Unicity Protocol, and earn XP toward a future token allocation. Built by the team behind Estonia, DARPA, NATO, and the NHS.

### What the Campaign Asks You to Do

```
TEST:        Interact with real Unicity testnet infrastructure
              (not a simulation — actual protocol functionality)

TRANSACT:    Perform real token transfers, agent interactions,
              and state transitions on testnet

EARN:        Accumulate XP for each completed quest
              XP is expected to factor into future token allocation
```

### Why "Test. Transact. Earn." Matters

This framing differs from pure "click for points" airdrop farms common in crypto. Because Unicity's value proposition is specifically about transaction mechanics (off-chain execution, agent settlement, offline payments), the testnet quests likely require genuinely using these features — not just social media tasks. This produces a stronger signal about real usage, similar to how Concrete's Phase 2 vault deposits are a stronger signal than Phase 1 social tasks (see our [Concrete XYZ guide](../concrete-xyz-defi-guide/README.md)).

---

## How to Participate — Step by Step

### Getting Started

```
Step 1: Go to quest.unicity.network
Step 2: Connect a wallet (or create a new Unicity wallet
        via sphere.unicity.network if required)
Step 3: Complete onboarding quests to understand the interface
Step 4: Explore available quest categories
```

### Setting Up a Unicity Wallet (via AgentSphere)

```
Visit: sphere.unicity.network/home
Options:
  "Create New Wallet" — generates a new secure wallet
  "Restore Wallet"    — recover an existing wallet via seed phrase

This wallet:
  - Holds your Unicity-native assets
  - Enables agent marketplace interaction
  - Supports P2P functionality (DMs, group chat per the
    Unicity Sphere Web3 wallet description)
```

### Quest Categories (Typical for This Type of Campaign)

While specific quests change over time, incentivized testnets in this category typically include:

```
ONBOARDING QUESTS:
  - Create/connect wallet
  - Complete profile setup
  - Join Discord community

TRANSACTION QUESTS:
  - Send a test token transfer
  - Receive a token from another testnet user
  - Use offline transfer (Bluetooth/NFC) if mobile app available

AGENT QUESTS:
  - Interact with a demo agent in the marketplace
  - Test agent-to-agent micropayment functionality
  - Explore the AI Marketplace demo

COMMUNITY QUESTS:
  - Social media engagement
  - Referrals
  - Educational content creation
```

### Best Practices

```
✅ Use the OFFICIAL domain: quest.unicity.network (avoid phishing clones)
✅ Engage genuinely with testnet features — quality over quantity
✅ Join the official Discord: discord.gg/BGuqUtwZp3
✅ Follow official X: @unicity_labs
✅ Read the whitepaper for deeper understanding:
   github.com/unicitynetwork/whitepaper
✅ Explore the live network explorer: unicity.network
```

---

## Unicity vs Traditional Blockchains

| Aspect | Traditional Blockchain (Ethereum-style) | Unicity |
|---|---|---|
| **Execution** | On-chain, every node processes every tx | Off-chain, peer-to-peer |
| **Global state** | Full ledger replicated everywhere | Minimal — only spent-state registry |
| **Throughput limit** | Bounded by consensus + block size | Scales with off-chain capacity |
| **Privacy** | Transaction details public by default | Transaction details stay private between parties |
| **Offline capability** | None — requires network connectivity | Yes — Bluetooth/NFC mesh transfers |
| **Designed for** | Human-paced transactions | Machine-speed agent transactions |
| **Bridge model** | Wrapped/synthetic assets | Actual asset movement |
| **Consensus base** | Varies (PoW, PoS, etc.) | PoW (RandomX) + BFT hybrid |

---

## Risks and Open Questions

### Early-Stage Project

Despite the strong team pedigree, Unicity is an early-stage protocol. The $3M seed round (February 2026) is small relative to many Layer 1 launches, and the testnet phase means the architecture is still being battle-tested.

### Novel Architecture = Unproven at Scale

The "no shared ledger" approach is architecturally elegant but has not been proven at the scale Unicity targets (millions of agent transactions per second). Working demos (Quake, AI Marketplace) are promising but are not the same as sustained mainnet load.

### Agentic AI Market Timing

The thesis depends heavily on AI agents becoming genuine, autonomous economic actors at scale. While the trend is real and growing, the timeline for "millions of agents transacting autonomously" remains uncertain — this is as much a bet on AI agent adoption as it is on blockchain architecture.

### Token Mechanics Not Fully Public

As with most pre-TGE projects, the full tokenomics (Alpha token distribution, SphereQuests XP-to-token conversion, vesting) are not yet fully disclosed. The whitepaper provides the technical foundation, but economic parameters typically come closer to token generation.

### Competitive Landscape

Unicity is not alone in targeting "AI agent infrastructure" — this has become a crowded narrative in 2025-2026, with multiple projects (some discussed in our [AI Agents and Web3 guide](../ai-agents-web3-guide/README.md)) competing for the same thesis. Technical differentiation (off-chain execution vs. on-chain agent frameworks) is real, but market attention is fragmented.

---

## Conclusion

Unicity represents a genuinely different architectural bet in the blockchain space: instead of optimizing the shared-ledger model that every chain since Bitcoin has used, it removes the shared ledger from the critical path entirely — keeping only a minimal aggregation layer to prevent double-spending.

**What makes Unicity worth following:**

- **Team pedigree is unusually strong** — Guardtime's KSI technology has real deployment history with Estonia, NATO, DARPA, and the NHS, not just claims
- **Architectural thesis is clear and specific** — built for agent-to-agent micropayments at machine speed, not retrofitted from a general-purpose chain
- **Five-layer modular design** — PoW foundation (RandomX), BFT consensus, Sparse Merkle aggregation, off-chain state transition, and agent execution
- **Working demonstrations exist** — real-time gaming (Quake), AI marketplace micropayments, offline Bluetooth/NFC transfers, genuine cross-chain bridging
- **Backed by credible Web3-focused VCs** — Blockchange Ventures, Outlier Ventures, Tawasal
- **SphereQuests testnet is live** — genuine "test, transact, earn" model tied to actual protocol usage, not just social tasks

**For participants:** SphereQuests offers a way to engage with genuinely novel blockchain architecture before mainnet — and given the team's track record, it's one of the more credible early-stage infrastructure plays in the current AI-agent-meets-blockchain narrative.

---

## Quick Reference

```
Website:           unicity.ai
Network explorer:  unicity.network
Testnet quests:    quest.unicity.network
Wallet/Sphere:      sphere.unicity.network
GitHub:             github.com/unicitynetwork
Whitepaper:         github.com/unicitynetwork/whitepaper
Discord:            discord.gg/BGuqUtwZp3
Twitter/X:          @unicity_labs
Company:            Unicity Labs (Zug, Switzerland)
Foundation:         Unicity Foundation (Zug, Switzerland)
CEO:                Mike Gault (ex-Guardtime CEO)
Predecessor:        Guardtime (KSI blockchain — Estonia, NATO, DARPA, NHS)
Seed funding:       $3M (Feb 2026) — Blockchange Ventures, Outlier Ventures, Tawasal
Native token:       Alpha (mined via PoW/RandomX)
Architecture:       5 layers — PoW, BFT, Sparse Merkle, State Transition, Agent Execution
```

---

## Related Articles in This Series

- [AI Agents and Web3](../ai-agents-web3-guide/README.md)
- [How LLMs Work](../how-llms-work/README.md)
- [How Smart Contracts Work](../smart-contracts-deep-dive/README.md)
- [Crypto Testnet Guide](../crypto-testnet-guide/README.md)
- [Concrete XYZ — DeFi Yield Infrastructure](../concrete-xyz-defi-guide/README.md)

---

> ⚠️ **Disclaimer:** This article is for educational purposes only and does not constitute financial or investment advice. Testnet participation and points-based campaigns carry no guarantee of future token value or allocation. Always verify you are using official URLs before connecting wallets.

---

## License

Released under the [MIT License](LICENSE). Free to use, share, and adapt.

---

*Found this useful? Star the repo ⭐ and share it with someone exploring agentic AI infrastructure.*
