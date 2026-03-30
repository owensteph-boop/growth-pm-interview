# Process Log: MapleHR Expansion Growth Exercise
*Steph Owen*

## Orientation and Problem Framing (~45 min)
- Read through README.md and explored the MapleHR platform across multiple accounts
- Noted observations: locked feature clicks with no upgrade path, usage limit hits with no 
response, add-on pages with no purchase mechanism, incomplete setups leading to support 
tickets and manual workarounds
- Opened a Claude chat to brainstorm and define the problem statement. Went through several 
iterations before landing on: "MapleHR's expansion motion lives primarily outside the product, 
while the product itself sits on a goldmine of untapped signals. Customers hit moments of peak 
intent with no in-product response."
- Created a Claude project with custom instructions tailored to the role and how I wanted 
Claude to operate as a sparring partner throughout the exercise

## Signal Analysis and Data Visualization (~60 min)
- Worked with Claude to build a signal analysis framework: signal mining, pattern recognition, 
hypothesis formation, impact vs. effort ranking, and data validation
- Asked Claude to categorize signal strength into three tiers before moving to hypotheses. 
Wanted to see the pattern before naming it.
- Pushed back on moving straight to hypotheses. Asked Claude to produce a data visualization 
first so I could perceive the patterns myself rather than just accept an AI-generated summary
- Claude built the expansion signal dashboard (mapleHR_expansion_signal_dashboard.html): 
18 accounts scored on behavioral intent weighted by health and churn risk, with charts showing 
signal type distribution and plan breakdown
- Key insight from the dashboard: locked feature clicks were the dominant signal among healthy, 
low-churn Essentials accounts

## Hypothesis Formation and Bet Selection (~30 min)
- Developed four hypotheses based on signal data:
  - H1: Locked feature clicks (high impact, low effort)
  - H2: Usage limit hits (high impact, low-medium effort)
  - H3: Manual export workarounds (medium impact, high effort)
  - H4: Add-on page views with no conversion (medium impact, low effort)
- Ranked by impact vs. effort. H1 won clearly.
- Pushed back on the initial bet framing to incorporate pricing specificity. The prompt needed 
to name the feature and anchor the $3/ee/mo delta, not just point to a pricing page.
- Stress-tested the hypothesis against account data. Found counter-examples (Golden Fork 
Restaurants: high signal, but health score 18 and high churn risk). Added a health score and 
churn risk filter: prompt only fires for accounts with health above 65 and churn risk not high.

## Building the Prototype (~60 min)
- Asked Claude to write a structured build prompt for Claude Code covering the trigger, modal 
design, targeting logic, and demo accounts to verify
- Opened Claude Code (desktop app), selected the project folder, and pasted the prompt with 
index.html as the working file
- Claude Code built the modal, targeting logic, and account-aware behavior in one pass. Tested 
immediately against Bright Smile Dental (fires correctly) and Golden Fork Restaurants 
(correctly suppressed).
- Identified that the upgrade CTA had no destination. Made the decision to add a self-serve 
confirmation screen showing personalized cost increase based on employee count, a confirm 
CTA, and a Talk to Sales secondary option. This was deliberate: the prototype needed to 
demonstrate the full self-serve motion, not just surface the signal.
- Added toast notifications for both upgrade confirmation and Talk to Sales clicks.

## What I Rejected or Iterated On
- Rejected moving to hypotheses before visualizing the data. Wanted to see patterns first, 
not anchor on assumptions.
- Rejected building a generic upgrade banner. Specificity (feature name, price delta, 
personalized cost) was the core thesis and had to be visible in the prototype.
- Rejected H2, H3, and H4 as the primary build. H2 is the strongest next candidate and would 
be the next experiment to run.
- Rejected adding a fake checkout flow or backend logic. The prototype needed to demonstrate 
the conversion moment, not simulate a full billing system.
- Rejected scope creep during the build. Several other opportunities were visible in the data 
(stalled onboarding, disconnected integrations, notification gaps) but none had the same 
combination of signal clarity and build efficiency as H1.

## Key Decisions and Why
**Health score filter:** A poorly targeted nudge can be worse than no nudge. Accounts below 
65 health or with high churn risk need a save motion, not an upgrade push. This filter is what 
separates an expansion motion from a churn accelerant.

**Self-serve confirmation screen with personalized pricing:** The thesis is that customers 
should be able to discover and pursue more value without a sales rep. A modal that goes 
nowhere doesn't prove that. The confirmation screen with exact cost calculations makes the 
self-serve path real.

**Two deliverables instead of one:** The signal dashboard and the prototype serve different 
purposes. The dashboard is the analytical layer that would inform targeting in production. The 
prototype demonstrates the customer-facing moment. Both were necessary to tell the full story.

**Claude Code over chat:** Used Claude Code (desktop app) for the build phase so edits could 
be made directly to the file without copy-paste loops. This kept iteration fast and the working 
file clean.

## Guiding Principles
These are the filters I'd use to help the team make decisions without needing sign-off on every call:

- **Look before you label.** Visualize signals before forming hypotheses. It's a guard against building the intervention that confirms what you already believe.
- **Signal before surface.** Don't build the prompt until the targeting logic exists to fire it correctly.
- **Protect healthy accounts.** Expansion motions don't fire on accounts showing churn risk. When in doubt, exclude.
- **Self-serve is the default, sales is the fallback.** Every intervention is designed for the customer to complete without a rep. Sales gets looped in when self-serve fails, not before.
- **Specificity converts, generics don't.** Every prompt names the feature, the price, and the outcome. No generic upgrade messaging ships.
- **Ship to learn, not to be right.** Every bet is an experiment. We instrument everything and let the data challenge our assumptions.
- **Every bet needs a short answer to "why now, why this."** Not a deck, just a sentence that survives a challenge.

## Time Breakdown
- Orientation and problem framing: ~45 min
- Signal analysis and dashboard build: ~60 min
- Hypothesis formation and bet selection: ~30 min
- Prototype build and testing: ~60 min
- Brief, process log, and Loom prep: ~60 min
