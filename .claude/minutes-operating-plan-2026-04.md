# Minutes Operating Plan

Status: operating strategy memo
Date: 2026-04-09
Owner: local planning doc

## Purpose

This document turns the current Minutes strategy into an operating plan.

It answers:

- who the next 6 months are for
- what "working" means
- what to build first
- what to test for monetization
- when to keep building independently
- when to partner, sell, or steward it instead

This is not a positioning memo.
It is a decision system.

It should also be read with one important attitude:

- the next goal is proof of routine, not proof of a full business

## One-line thesis

Minutes should try to become the default open-source, local-file-native conversation memory layer for solo AI-native power users with high-stakes recall and follow-through problems.

## The 6-month bet

### Primary ICP

For the next 6 months, the primary user is:

- a solo operator / founder / advisor / consultant
- already using Claude, Codex, Gemini, or agent workflows regularly
- with many important conversations
- who feels real pain around recall, commitments, follow-up, and relationship continuity
- and who values local ownership, inspectability, and control

### Why this ICP

This user has all of the following at once:

- painful enough problems to care
- enough technical comfort to adopt Minutes today
- a strong trust preference around sensitive conversations
- willingness to use desktop + CLI + MCP flows
- more appetite to pay for leverage than generic developers

### Explicit anti-ICP for now

Do not optimize the next 6 months for:

- generic meeting-notes buyers
- broad team collaboration
- sales organizations
- enterprise admins
- general PKM users
- non-technical mass-market productivity users

They may matter later.
They should not steer near-term product decisions.

## The user job

The core job is not:

- "transcribe my meeting"

It is:

- "make my important conversations reliably usable later by me and my agents"

The sub-jobs are:

1. Capture or import the conversation without drama.
2. Turn it into trustworthy structured memory.
3. Let me ask what changed, what I promised, what they care about, and what I should do next.
4. Make that useful inside my existing agent workflows.

## The product promise

The promise to this ICP should be:

- Your conversations become durable, local, inspectable memory.
- Your agent can reliably recall people, commitments, decisions, and changes over time.
- You keep control of the files.
- The workflows get better as your corpus grows.

Not:

- prettiest notes
- best summary
- most automations
- biggest team feature set

## The control-point thesis

Minutes should assume that under MIT:

- the code can be copied
- the files can be parsed externally
- workflows can be imitated

So the real control point must be earned through:

1. trusted ingestion
2. canonical local corpus
3. reliable identity resolution
4. strong graph-backed recall
5. default distribution across agent-native surfaces
6. habit-forming workflows

That stack, not code exclusivity, is what can create durable leverage.

## North star

### Primary north-star metric

**Activated memory users**

Definition:

- users with at least 5 captured or imported conversations
- and at least 3 recall workflow uses in 14 days

Recall workflow uses include:

- prep
- brief
- debrief
- weekly
- person / research / consistency queries
- agent-mediated recall queries through MCP or SDK

Why this metric:

- it combines corpus creation and actual recall behavior
- it is much harder to fake than installs, stars, or transcript generation
- it tracks the real job-to-be-done

## Metrics stack

### Acquisition metric

- weekly new users who successfully capture or import at least 1 conversation

### Activation metric

- percent of new users who reach Activated Memory User status within 21 days

Target for a good wedge:

- 25%+ of serious new users

### Time-to-first-recall metric

- median time from install to first successful recall outcome

Definition:

- not first transcript
- not first demo
- first moment where the user gets a useful answer to a real memory question from Minutes

Examples:

- "what did I promise Sarah?"
- "what changed since my last call with Alex?"
- "what are the open commitments from this week?"

Why it matters:

- if the first useful recall moment takes too long, most users will never reach activation
- this is the most important setup-to-value bridge in the whole product

Working target:

- under 30 minutes for a serious new user with one real conversation or import path

### Retention metric

- 8-week retention of Activated Memory Users

Definition:

- user still has at least 1 new conversation added or 1 recall workflow session in week 8

Good signal:

- 35%+ for the primary ICP

Great signal:

- 50%+

### Trust / product quality metric

- percent of recall answers judged correct-enough by the user in dogfood or interview follow-up

Proxy metrics:

- false "first meeting" rate
- alias collision rate
- speaker identity correction rate
- import failure rate
- share of workflows that fall back to raw transcript search

### Monetization signal metric

- count of users who explicitly ask for, join a waitlist for, or pre-pay for one of the aligned paid layers

Aligned paid layers:

- sync / backup / handoff
- pro workflow package
- premium imports / identity cleanup
- small-team secure sharing

### Strategic leakage metric

- count of third-party wrappers / forks / hosted uses where value appears to accrue away from Minutes

This is not automatically bad.
It becomes important only if adoption is strong and capture is weak.

## The 6-month roadmap

### Phase 1: Trust the corpus

Time: weeks 1-8

Goal:

- make the corpus trustworthy enough that users rely on it

Priority work:

- alias resolution
- identity canonicalization
- speaker reliability
- import fidelity
- first-meeting false-negative reduction
- better artifact provenance and backend visibility
- capture robustness

Success condition:

- power users start treating Minutes as the system of record for conversations

Failure smell:

- users like the idea but do not trust recall answers

### Phase 2: Make recall obviously better than search

Time: weeks 5-12

Goal:

- make graph-backed memory retrieval feel qualitatively better than transcript grep

Priority work:

- graph-backed people / commitment / decision retrieval
- stronger person and topic pages
- better "what changed since last time?" surfaces
- better relationship and follow-through summaries
- cleaner agent read access for structured recall

Success condition:

- users choose recall workflows by default over transcript search

Failure smell:

- users fall back to raw meeting text most of the time

### Phase 3: Make agent usage boringly easy

Time: weeks 8-16

Goal:

- remove friction from agent read access

Priority work:

- zero-config or near-zero-config read-only onboarding
- polished docs for Claude / Codex / Gemini / Cursor / Windsurf style workflows
- canonical examples for common prompts and agent tasks
- better MCP ergonomics for recall, not just tooling breadth

Success condition:

- setup no longer blocks recommendation or repeated use

Failure smell:

- "looks cool, too much setup" dominates feedback

### Phase 4: Monetization probes without betraying the thesis

Time: weeks 12-24

Goal:

- learn what aligned paid layer has real pull

Priority work:

- landing pages / waitlists / concierge offers for:
  - secure sync / backup / handoff
  - pro operator workflow package
  - premium import / corpus cleanup service
- lightweight willingness-to-pay interviews
- prepayment or design-partner asks before full implementation

Success condition:

- one monetization path shows repeated explicit pull

Failure smell:

- users love the product but do not care enough to pay for any aligned convenience layer

## What not to build in this window

- big team admin centers
- generic collaboration suites
- broad enterprise workflow complexity
- cloud memory by default
- prettier-notes-first features
- speculative personalization that outruns trust
- "MCP breadth" work that does not improve recall quality or agent adoption

## The 90-day proof plan

Before treating Minutes as a serious business candidate, prove the basics.

### Targets for the next 90 days

- run 20 targeted user interviews with the primary ICP
- get 30 users to Activated Memory User status
- measure 4-week retention among activated users
- measure median time-to-first-recall
- gather explicit willingness-to-pay feedback on the aligned paid layers

### Why 90 days matters

This is the checkpoint between:

- "good strategy idea"

and:

- "real routine-forming product"

If the product cannot form habit with a small, sharp wedge, monetization strategy is premature.

## Monetization paths to test

### Test A: Secure sync / backup / handoff

Hypothesis:

- primary users will pay for a trusted convenience layer if it preserves the local-first contract

Offer concept:

- encrypted sync and backup for meetings, graph state, and workflow continuity

Good first test:

- waitlist
- design partner interviews
- concierge prototype with explicit guarantees

Suggested pricing hypotheses:

- $12-$24/month individual
- higher if it clearly includes backup + handoff + multi-device continuity

Why test first:

- most aligned with the trust-heavy product
- least dependent on fake scarcity

### Test B: Pro workflow package

Hypothesis:

- founder/operator/advisor users will pay for higher-leverage recall and prep flows

Offer concept:

- advanced prep / debrief / weekly / relationship memory / decision tracking

Good first test:

- gated preview
- private beta
- annual prepay with founder conversations

Suggested pricing hypotheses:

- $15-$39/month individual

Risk:

- users may perceive this as artificial gating if the free core is already very strong

### Test C: Premium import / cleanup / identity service

Hypothesis:

- users with messy prior meeting history will pay to get their corpus into a high-trust state

Offer concept:

- premium importers
- identity cleanup
- corpus normalization
- migration from Granola / Otter / Fireflies exports

Good first test:

- concierge service
- one-time paid migration pilots

Suggested pricing hypotheses:

- $99-$499 one-time, depending on complexity

Why this matters:

- it monetizes the real control point of ingestion quality

### Test D: Small-team secure sharing

Hypothesis:

- some users will want selective sharing without wanting full hosted SaaS

Offer concept:

- secure per-meeting handoff
- shared memory subsets
- encrypted or user-controlled collaboration

Good first test:

- manual design partner loop with 3-10 user teams

Suggested pricing hypotheses:

- $20-$50/user/month

Do not test first.
This is a later extension if individual pull is real.

## Pricing principles

- charge for convenience, continuity, and leverage
- do not charge for ownership of the user’s own local files
- avoid turning the free core into bait
- prefer annual or design-partner commitments over casual monthly vanity pricing

## Interview questions that actually matter

When talking to users, ask:

1. What conversation do you most wish your agent remembered correctly today?
2. What do you trust least in your current setup?
3. Where does recall currently break: capture, identity, search, synthesis, or follow-through?
4. If Minutes disappeared tomorrow, what would be hardest to replace?
5. Which of these would you actually pay for:
   - better recall
   - better prep/debrief
   - secure sync / backup
   - migration / cleanup
   - selective team handoff
6. What would make you unwilling to pay even if you liked the product?

## The decision tree

### Branch 1: Build an independent business

Choose this path if within 6 months you see:

- strong activation into recall workflows
- real 8-week retention for the primary ICP
- obvious trust in Minutes as the system of record
- at least one aligned monetization path with explicit pull

Then do:

- double down on that monetization layer
- keep MIT
- continue owning the category through product + docs + ecosystem defaultness

### Branch 2: Build as a strategic asset

Choose this path if:

- product pull is real
- retention is decent
- but monetization pull is weak or naturally belongs to a larger platform

Then do:

- optimize for canonicality, quality, and strategic legibility
- deepen integrations
- become visibly indispensable in the local conversation-memory layer
- explore partnerships, embedding, or acquisition conversations from strength

This is not failure.
It is a valid outcome.

### Branch 3: Build the engine / SDK ecosystem

Choose this path if:

- the underlying primitives clearly matter
- the standalone product shows weaker routine adoption
- and downstream builders want the ingestion / parsing / graph / memory substrate

Then do:

- strengthen crates and SDKs as products in their own right
- improve embedding docs and API stability
- optimize for "Minutes inside other tools"
- treat the default app as a reference implementation, not the only bet

### Branch 4: Steward as public infrastructure

Choose this path if:

- adoption is meaningful
- users love the trust model
- but no business layer feels aligned or strong enough

Then do:

- optimize for durability and ecosystem health
- clarify governance
- encourage wrappers and downstream usage
- treat influence and standard-setting as the win

### Branch 5: Deprioritize or hand off

Choose this path if after a serious 6-month push:

- activation is weak
- retention is weak
- trust remains shaky
- monetization pull is absent
- and the best users still do not make it part of their routine

Then do one of:

- narrow even harder
- partner with a better-distributed platform
- hand it off to a maintainer or steward
- or consciously stop

Do not keep funding a beautiful thesis with weak evidence forever.

## The falsifiers

The strategy is wrong, or at least incomplete, if any of these happen:

1. Users want transcripts, but not recall workflows.
2. Users like the concept, but do not trust Minutes as the system of record.
3. Setup friction suppresses repeat use even among the target ICP.
4. Competing agent platforms absorb enough of the workflow that Minutes becomes just a file emitter.
5. No aligned paid layer generates real pull, even among activated users.

## Platform-memory contingency

If Anthropic, OpenAI, Google, or another major platform ships native conversation memory with near-zero setup:

### Immediate positioning response

- stop leading with "agents can remember conversations"
- lead with:
  - open
  - local
  - portable
  - inspectable
  - artifact-grounded

### Immediate product response

- accelerate import and migration from platform-native memory where possible
- strengthen "system of record" language and workflows
- make recall correctness and corpus portability more central than generic memory claims

### Strategic implication

Platform-native memory raises the bar on convenience.
It does not remove the need for:

- user-owned artifacts
- local trust
- inspectable history
- cross-platform portability

But if Minutes cannot make that distinction vivid and useful, platform absorption becomes existential.

## The one question to revisit every month

**What is getting stronger: the user’s dependence on the Minutes corpus and workflows, or the surrounding ecosystem’s ability to replace them?**

If dependence is compounding faster than replaceability, the strategy is working.
If replaceability is outrunning dependence, the strategy needs to change.

## Immediate next moves

1. Rewrite the current strategy memo to reflect this narrower ICP and the control-point logic.
2. Instrument activation, retention, and time-to-first-recall, even if manually at first.
3. Build the roadmap with ingestion and identity reliability at the top.
4. Start 10-20 targeted interviews with the exact ICP.
5. Run lightweight willingness-to-pay interviews, but do not build a full paid layer before routine use is proven.

## Bottom line

Minutes is worth doing.

But it should be done with eyes open:

- MIT is a trust and adoption tool, not a moat
- the company question depends on control-point strength, not just category elegance
- the first business, if there is one, should likely be optional convenience around a trusted local-first core
- if that paid layer never emerges, the best outcome may still be a strategically valuable open infrastructure asset
