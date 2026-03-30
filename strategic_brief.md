# MapleHR Expansion Growth: Strategic Brief
*Steph Owen*

## What I Built and Why

I built two things: an expansion signal dashboard and a contextual in-product upgrade prompt.

The dashboard scores all 18 accounts on behavioral intent, weighted by health and churn risk. 
It surfaced the clearest pattern in the data: healthy Essentials accounts are clicking into locked 
Advantage features and hitting a dead end with no path forward.

That finding drove the prototype build. When a qualifying account clicks a locked feature, a 
modal fires naming the specific feature, anchoring the price at $3 more per employee per month, 
and offering a primary CTA to upgrade, along with a secondary CTA to talk to sales. Accounts 
with a health score below 65 or high churn risk are excluded; they need a save motion, not an 
upgrade push.

I chose this over usage limit prompts, export nudges, and add-on page interventions because a 
locked feature click is declared intent. You don't have to infer it. And specificity converts where 
generic upgrade banners don't.

## How It Works

Switch to Bright Smile Dental: health score 88, low churn, Essentials plan. Click any locked 
Advantage feature and the modal fires, naming the feature, showing the $3/ee/mo delta, and 
offering a clear upgrade path. Users can also click "Talk to Sales" to have a MapleHR rep reach 
out. Switch to Golden Fork Restaurants: health score 18, high churn. Click the same feature. 
Nothing fires. That's the targeting logic working as intended.

## What's Next

The goal is a product that knows when a customer is ready to grow before a sales rep does, 
and makes the next step obvious without anyone having to ask.

Getting there requires three things: proper instrumentation so every signal flows into a 
behavioral data model, an agent layer that can query that model and trigger the right 
intervention automatically, and an experimentation infrastructure that treats every prompt, 
every threshold, and every targeting rule as a hypothesis to test. Usage limit hits ship as the 
next experiment. Targeting logic gets sharper with each test. We go from 30 experiments a year 
to hundreds, not by moving faster, but by building the system that makes learning continuous.
