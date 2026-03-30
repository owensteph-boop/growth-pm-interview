# MapleHR — PM Exercise (Expansion Growth)

## Quick Start

1. **Read the exercise brief below** — your scenario, the challenge, and what we're looking for
2. **Open `index.html`** in your browser — that's the app

No server, no install, no build step. All data is embedded directly in the HTML file.

## What's Here

```
index.html          The full app — markup, styles (Tailwind CDN), and JavaScript in one file
data/
  customers.json    18 simulated customer accounts across plan tiers
  modules.json      Module definitions with setup steps and plan requirements
  usage_events.json 170 behavioral events (logins, feature clicks, exports, etc.)
```

### The App

A simulated MapleHR platform with:

- **Homepage** — company info, notification banners, quick-access widgets, and an activity feed showing recent events for the selected account
- **Modules page** — active modules with setup progress, available modules on the current plan, and add-ons
- **Account switcher** — dropdown in the top bar to switch between customer accounts. The whole app updates to reflect that customer's plan, modules, and activity

### The Data

**Customers** span three plan tiers (Essentials, Advantage, Premium) with varying company sizes, add-ons, setup progress, and health indicators. Some are thriving, some are stalled, some are showing expansion signals.

**Usage events** include logins, locked feature clicks, manual data exports, setup steps completed/skipped, first feature uses, support tickets, usage limit hits, and add-on page views.

**Modules** define what's available at each plan tier, what setup looks like, and which features are add-ons.

### Complexity

The app starts simple on purpose. You're welcome to keep it as vanilla HTML/JS, or use your AI tool to restructure it into whatever stack you prefer — React, Vue, Svelte, a full server setup, whatever feels right. The starting point is intentionally low-friction so you can spend your time on the problem, not the setup.

---

## The Company: MapleHR

MapleHR is a mid-market HR platform serving ~30,000 customers, primarily companies with 25–500 employees. The platform covers Core HR (employee records, org charts, reporting), PTO management, hiring/ATS, time tracking, performance management, benefits administration, and advanced analytics.

MapleHR operates on a tiered pricing model:

| Plan | Price | Includes |
|------|-------|----------|
| **Essentials** | $6/employee/mo | Core HR, Employee Records, Reporting, Basic PTO |
| **Advantage** | $9/employee/mo | Everything in Essentials + ATS, Time Tracking, Performance |
| **Premium** | $14/employee/mo | Everything in Advantage + Benefits Admin, Advanced Analytics |

**Add-ons** (available on any plan): Payroll ($6/ee/mo), EOR/Global Employment ($12/ee/mo), LMS/Training ($3/ee/mo), Candidate Assessments ($2/ee/mo).

---

## Your Scenario

You've just joined MapleHR as PM for Expansion Growth. The company has 3,000 customers but expansion revenue has been mostly sales-driven — reps manually identify accounts that might upgrade and reach out.

Leadership wants to change that. The goal: ensure customers seek BHR first when they are looking to get more out of their HR stack.

Here's what you're working with:

### What you know about the customer base

- **60%** of customers are on Essentials, **28%** on Advantage, **12%** on Premium
- Customers who upgrade typically do so **6–14 months** after initial purchase
- Current experiment velocity: ~30 tests/year, mostly email subject lines and landing page variations. 

### Your challenge

Build a working prototype that demonstrates how you would approach product-led expansion at MapleHR. You have the starter repo (a functioning MapleHR app with mock data) as your foundation.

As you complete this exercise, you may need to make assumptions. That is totally fine, just let us know what you assumed and why.

### What we want to understand from you

- What is an example diagnosis of a problem to solve at MapleHR and why is it important to solve it now?
- What kind of guiding policies would you set up to help the people you work with understand your priorities going forward?

---

## How This Works

1. **Use an AI coding tool** to build your prototype. Claude Code, Codex, Cursor, Copilot, Windsurf — whatever you're most comfortable with. This is a core part of what we're evaluating, and we genuinely want to see your workflow.

2. **Please keep this to around 2-3 hours.** We want to respect your time. We'd much rather see a well-scoped prototype with clear thinking behind it than something over-engineered. Knowing what to build (and what to leave out) in a limited window is part of the craft.

3. **Keep a lightweight process log.** This can be a markdown file, a Loom recording, or screenshots — whatever's easiest for you. We're curious about:
   - What you prompted your AI tool to do (and what you rejected or iterated on)
   - Key decisions you made and why
   - Where you spent your time

4. **Write a one-page brief** covering:
   - **What you built and why** — what's the strategic rationale? Why this over the ten other things you could have built?
   - **How it works** — a quick walkthrough
   - **What you'd do next** — if you had 6 months instead of 4 hours, what does this become?

5. **Be ready to walk us through it live.** The interview conversation is where we'll dig into your thinking, your tradeoffs, and your product instincts. The prototype is a conversation starter, not the final exam.

---

## What We're Evaluating

We really want to see how you approach solving product problems first and foremost.

- **Product judgment** — What did you pick to solve? Why is that?
- **Strategic thinking** — How does this connect to a product vision and themes?
- **AI fluency** — How did you use AI in your process?
- **Scoping ability** — What scope made the cut and what didn't?
- **Communication** — Share your journey during the exercise with us.

If your prototype is rough but your thinking is sharp, that's a great outcome. We're much more interested in the reasoning behind your choices than in pixel-perfect execution.

---

## Deliverables

1. **Your prototype** — built on the starter repo using an AI coding tool
2. **Your process log** — how you used AI, what decisions you made
3. **Your one-page brief** — what you built, why, and what comes next
4. **A loom or video recording** - walking us through your solution

Good luck. We're excited to see how you think about this.
