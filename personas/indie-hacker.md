# Indie Hacker

If AI Field Guide has a default reader right now, it is the indie hacker.

Not the enterprise buyer.
Not the benchmark maximalist.
Not the person collecting every new tool.

The indie hacker wants something simpler:

- ship faster
- validate faster
- keep burn low
- avoid tool sprawl
- get to revenue before building a tiny internal platform by accident

## The core idea

An indie hacker should optimize for **speed to shipped product**, not for the most impressive stack.

The best AI stack for an indie hacker is usually:
- small
- cheap enough to justify early
- good at building real product work
- boring enough to maintain
- flexible enough to go from idea to launch

## What indie hackers actually optimize for

A good indie-hacker stack should maximize:

- speed to MVP
- speed to first launch
- speed to first revenue signal
- low monthly burn
- low setup overhead
- enough product leverage to work solo or near-solo

A bad stack usually looks like:

- too many overlapping subscriptions
- expensive tooling before validation
- complex infra before users
- too much focus on coding theater instead of shipping
- AI workflows that feel powerful but do not move the business forward

## The most common mistakes

### 1. Buying the fantasy stack too early
This is the classic trap.

You see:
- Claude Max
- Cursor Pro
- ChatGPT Plus
- Perplexity
- Lovable
- Bolt
- Copilot
- two design tools
- maybe another research tool

Now you are paying real money before you have users.

Indie hackers do not need the most complete stack on day one.
They need the smallest stack that helps them get to a real product faster.

### 2. Confusing generation with progress
A generated landing page is not traction.
A dashboard scaffold is not validation.
A polished demo is not product-market fit.

AI makes it easier to create output.
The indie-hacker challenge is still choosing what is worth building.

### 3. Overengineering before distribution
Many indie hackers lose weeks on architecture, multi-agent systems, and workflow complexity before they have a single real user.

That is almost always backwards.

### 4. Paying for overlap
The same pattern shows up constantly:
- too many tools
- too much overlap
- unclear role for each subscription

A good indie-hacker stack should have clear jobs:
- one main coding tool
- one heavier reasoning tool if needed
- simple infra
- maybe one research tool if it truly helps

### 5. Ignoring cost cliffs
The pain is not just tool price.
It is what happens later:
- rate limits
- overages
- infra upgrades
- hidden token spend
- commercial-use tier changes after launch

Indie hackers care about whether the stack stays sane after the first customer.

## The default recommendation

For most indie hackers building software in 2026, the strongest default path looks like this:

- **Cursor** for daily coding and iteration
- **Claude Code / Claude Pro** for heavier planning, repo-wide work, and refactors
- **Vercel** for deployment
- **Supabase** for backend, database, and auth
- one research tool only if it clearly saves time

Why this keeps showing up:
- it is strong enough to matter
- simple enough to maintain
- cheap enough to start with
- common enough that examples and workflows are easy to find

## What indie hackers should care about most

### 1. Time to useful launch
The stack should help you get from:
- idea
- to MVP
- to deployed product
- to first user feedback

### 2. Cost discipline
The stack should not feel like a second startup.
A lot of indie hackers would be better off with:
- one paid AI tool
- one optional second tool
- cheap/free infra

than with an $180/month fantasy setup.

### 3. Product leverage
The stack should help with:
- coding
- refactoring
- research
- debugging
- launching

It does not need to be perfect at everything.
It needs to be useful where indie hackers actually spend time.

### 4. Simplicity
Simple stacks survive.
Complex stacks create new work.

## Budget lanes

## $0 validation lane
Good for:
- testing an idea
- building a rough first version
- checking whether the product deserves more investment

Rule: do not spend serious money before the idea earns it.

## ~$40 serious starter lane
This is the strongest default lane for many indie hackers.

Typical shape:
- Cursor Pro
- Claude Pro / Claude Code
- free or cheap infra

Why it works:
- enough power to materially change workflow
- still disciplined
- low enough to justify before revenue

See: [`../stacks/$40-indie-hacker-stack.md`](../stacks/$40-indie-hacker-stack.md)

## ~$100+ working lane
This is where many indie hackers land after launch.

Typical additions:
- research tool
- analytics
- email
- monitoring
- infra upgrades

This is easier to justify once the project has real users or money coming in.

## Practical rules for indie hackers

### Rule 1: every paid tool should earn its keep
If a tool does not clearly:
- speed up shipping
- reduce a real bottleneck
- help get to revenue

cut it.

### Rule 2: build the boring version first
The best indie-hacker stack is often not the coolest one.
It is the one that lets you launch this week.

### Rule 3: use AI to compress execution, not to avoid thinking
AI helps with implementation.
It does not remove the need for product judgment.

### Rule 4: launch before stack perfection
If you are still debating tools after two weeks, the stack is already becoming the project.

## Current verdict

The best AI stack for an indie hacker is not the biggest one.
It is the one that gets you to a launched product with the least wasted motion.

Right now, the strongest default pattern is:

- **Cursor for daily work**
- **Claude Code for heavy work**
- **cheap/free infrastructure until the product earns more complexity**

That is the center of gravity this guide should optimize for.

## Related pages

- [`../stacks/$40-indie-hacker-stack.md`](../stacks/$40-indie-hacker-stack.md)
- [`../use-cases/build-a-web-app.md`](../use-cases/build-a-web-app.md)
- [`../use-cases/refactor-a-large-codebase.md`](../use-cases/refactor-a-large-codebase.md)
- [`./solo-developer.md`](./solo-developer.md)
- [`../tools/cursor.md`](../tools/cursor.md)
- [`../tools/claude-code.md`](../tools/claude-code.md)
