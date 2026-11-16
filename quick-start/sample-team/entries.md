### LS-0001 · Lower the DNS time to live before moving hosts
- Type: fix
- Source: Launch notes, internal, 2025-09-16
- Tags: hosting, performance
- Links: LS-0019
- Added: 2025-09-16 by Developer
- Status: kept
- Sensitivity: internal

After we moved a client site to a new host, some visitors still saw the old cached pages for a full day. The old DNS records had a long time to live, so the change took a day to reach everyone. Lower the time to live a few days before the move, then raise it again once the new host is live.

**Why it matters:** A short time to live makes a hosting move take minutes for visitors, not a day.

### LS-0002 · One named contact makes the first month calmer
- Type: insight
- Source: Client survey, Larchmont Studio, 2026-01-12
- Tags: client-onboarding, communication
- Links: LS-0004
- Added: 2026-01-12 by Operations lead
- Status: kept
- Sensitivity: internal

In our yearly client survey, clients who had one named person answering every question rated their first month higher. Clients passed between two or three of us rated it lower, even when the work arrived on time.

**Why it matters:** How the first month feels shapes how a client remembers the whole project.

### LS-0003 · Clients read the first invoice as the real quote
- Type: lesson
- Source: Project retro, Halden Bakery site, 2026-02-14
- Tags: pricing, estimates, communication
- Links: LS-0011
- Added: 2026-02-14 by Project manager
- Status: kept
- Sensitivity: internal

The client accepted the estimate but pushed back hard on the first invoice. Our estimate showed ranges; the invoice showed one number, and that number is what they remembered.

**Why it matters:** Show a single expected figure next to every range in estimates.

### LS-0004 · Every new client gets one named contact
- Type: decision
- Source: Studio meeting, internal, 2026-02-16
- Tags: client-onboarding, process
- Links: LS-0002, LS-0010
- Added: 2026-02-16 by Founder
- Status: kept
- Sensitivity: internal

Every new client now gets one named contact at the studio and a kickoff call within three working days of signing. The contact stays the same for the first month, even when the work moves between people.

**Why it matters:** It turns the survey finding into a rule the whole team follows.

### LS-0005 · Tell us everything you need in week one
- Type: quote
- Source: Kickoff call, Marrowfen Flowers, 2026-02-17
- Tags: client-onboarding, communication
- Links: LS-0006
- Added: 2026-02-17 by Project manager
- Status: kept
- Sensitivity: internal

> "Can you send one list of everything you need from us in the first week? I keep finding out about things one email at a time."

**Why it matters:** New clients want the whole picture of their homework up front, not piece by piece.

### LS-0006 · Send the content checklist before the kickoff call
- Type: lesson
- Source: Studio meeting, internal, 2026-02-19
- Tags: client-onboarding, scope
- Links: LS-0005, LS-0022
- Added: 2026-02-19 by Project manager
- Status: kept
- Sensitivity: internal

We used to send the content checklist after the kickoff call, so clients heard about photos, copy and logins a week in. Sending it a few days before the call means they arrive with questions, and the call settles what is in scope.

**Why it matters:** Clients who see the checklist early plan their own time and push back less on scope later.

### LS-0007 · Bill hosting as its own monthly line
- Type: decision
- Source: Founders meeting, internal, 2026-02-20
- Tags: hosting, retainer
- Themes: q1-pricing-review
- Links: LS-0013
- Added: 2026-02-20 by Founder
- Status: kept
- Sensitivity: internal

Hosting moves out of the support retainer and onto its own monthly line on every invoice. Clients can then see what keeps the site running and what pays for our time.

**Why it matters:** Clients stop reading the retainer as the price of hosting and question it less.

### LS-0008 · Rough wireframes early mean fewer layout changes later
- Type: insight
- Source: Unknown
- Tags: scope, design-feedback
- Added: 2026-02-23 by Designer
- Status: kept
- Sensitivity: internal

Clients who see a rough wireframe in the first week ask for fewer layout changes once the designs are polished. A sketch invites the big comments early, while they are still cheap to act on.

**Why it matters:** Moving big layout feedback to week one saves rework at the end of a project.

### LS-0009 · Find out who controls DNS a week before launch
- Type: lesson
- Source: Launch retro, internal, 2026-02-25
- Tags: hosting, process
- Links: LS-0014
- Added: 2026-02-25 by Developer
- Status: promoted
- Promoted to: promoted/launch-checklist.md
- Sensitivity: internal

A launch slipped by two days because nobody on the client side knew who controlled their domain's DNS. A week before launch, ask who holds the domain account and check they can make a change.

**Why it matters:** A launch date means nothing until someone can change the DNS on the day.

### LS-0010 · First-month feedback comes faster with one named contact
- Type: insight
- Source: Onboarding review, internal, 2026-02-27
- Tags: client-onboarding, design-feedback
- Links: LS-0004
- Added: 2026-02-27 by Designer
- Status: kept
- Sensitivity: internal

Looking back at this month's new projects, design feedback came back in about two days when the client knew exactly who would act on it. When feedback went to a shared inbox, it took more than a week.

**Why it matters:** One named contact speeds up design rounds as well as making clients feel looked after.

### LS-0011 · "Just tell me the number"
- Type: quote
- Source: Discovery call, Corrowin Dental, 2026-03-02
- Tags: pricing, estimates
- Links: LS-0003
- Added: 2026-03-02 by Founder
- Status: kept
- Sensitivity: internal

> "I don't need three options. Just tell me the number you'd pick."

**Why it matters:** Second client this quarter asking for one recommended price, not a menu.

### LS-0012 · Image size limits in the old CMS
- Type: reference
- Source: Image size guide, old CMS help pages, 2026-03-16
- Tags: cms, performance
- Themes: cms-migration
- Links: LS-0019
- Added: 2026-03-16 by Developer
- Status: retired
- Sensitivity: internal
- Last reviewed: 2026-06-29

The old CMS rejected images over 2 MB and shrank anything wider than 2000 pixels, so we exported large images at 1920 pixels wide. These limits stopped applying once every site moved to the new CMS.

**Why it matters:** It kept image uploads working on sites still waiting for the CMS move.

### LS-0013 · Agree retainer rate changes in writing at signing
- Type: lesson
- Source: Founders meeting, internal, 2026-03-25
- Tags: pricing, retainer
- Themes: q1-pricing-review
- Links: LS-0007
- Added: 2026-03-25 by Founder
- Status: kept
- Sensitivity: restricted

A retainer client disputed our mid-year price rise and kept paying the old rate for three months while we talked it through. The contract said rates could change, but not when or by how much. Write the review date and the largest possible rise into every retainer at signing.

**Why it matters:** A clear rule at signing avoids a pricing dispute that costs months of goodwill.

### LS-0014 · The hosting provider's checks before a launch
- Type: reference
- Source: Hosting provider's launch guide, 2026-04-07
- Tags: hosting, tooling
- Links: LS-0009
- Added: 2026-04-07 by Developer
- Status: promoted
- Promoted to: promoted/launch-checklist.md
- Sensitivity: internal

Our hosting provider's launch guide lists three things to finish before a site goes live: install the security certificate, set redirects for old addresses and take a full backup. Each takes minutes, but any of them can hold up a launch if it is left to the day.

**Why it matters:** Every launch gets the same short list of checks, whoever runs it.

### LS-0015 · Day rate agreed with the freelance developer
- Type: decision
- Source: Founders meeting, internal, 2026-04-10
- Tags: hiring, process
- Added: 2026-04-10 by Founder
- Status: kept
- Sensitivity: restricted

We agreed a day rate of 380 with the freelance developer helping on the CMS move, fixed until the move is finished. Keep the rate out of estimates and client conversations; clients are billed at our usual rate.

**Why it matters:** Anyone pricing the CMS move needs the real cost of the extra developer.

### LS-0016 · Light grey text looks smart but is hard to read
- Type: quote
- Source: Design review, Tolvery Opticians, 2026-04-14
- Tags: design-feedback, accessibility
- Added: 2026-04-14 by Designer
- Status: kept
- Sensitivity: internal

> "The light grey text looks smart, but many of our customers can't read it."

**Why it matters:** Clients notice low contrast as an accessibility problem before we do.

### LS-0017 · Preview links break when the CMS draft is renamed
- Type: fix
- Source: Support thread, internal, 2026-04-21
- Tags: cms, tooling
- Added: 2026-04-21 by Developer
- Status: new
- Sensitivity: internal

Renaming a draft changes its slug, which kills any preview link already sent to the client. Lock the slug before sharing a preview, or send the preview through the share panel, which uses the page ID.

**Why it matters:** [draft] Saves a confusing client email every time a draft is renamed.

### LS-0018 · Customers struggle to read the light grey text
- Type: quote
- Source: Design review, Tolvery Opticians, 2026-04-14
- Tags: design-feedback, accessibility
- Added: 2026-05-04 by Project manager
- Status: new
- Sensitivity: internal

> "The light grey text looks smart, but most of our customers can't read it."

**Why it matters:** Check text contrast before the first design review instead of waiting for the client to spot it.

### LS-0019 · Set redirects before switching DNS after a CMS move
- Type: fix
- Source: Support thread, internal, 2026-06-15
- Tags: hosting, cms
- Themes: cms-migration
- Links: LS-0001, LS-0012
- Added: 2026-06-15 by Developer
- Status: kept
- Sensitivity: internal

After a CMS move, old page addresses showed errors for an hour because the redirects went in after the DNS switch. Load the redirect list onto the new host first, test a few old addresses, then switch the DNS.

**Why it matters:** Old links in emails and search results keep working from the first minute.

### LS-0020 · A starter folder of templates for each new hire
- Type: idea
- Source: Studio meeting, internal, 2026-07-20
- Tags: hiring, tooling
- Themes: new-hire-onboarding
- Links: LS-0023
- Added: 2026-07-20 by Operations lead
- Status: kept
- Sensitivity: internal

Every new hire could get a starter folder on day one, with our estimate, proposal and handoff templates, the content checklist and a short glossary. Logins and passwords stay out of it; the operations lead sets those up in person.

**Why it matters:** [draft] New people could find the studio's templates without asking around.

### LS-0021 · Client wants a colleague copied on final files
- Type: quote
- Source: Launch call, Marrowfen Flowers, 2026-09-14
- Tags: design-feedback, communication
- Added: 2026-09-14 by Project manager
- Status: new
- Sensitivity: internal

> "Could you copy Gemma on the final files? She looks after all our photos now."

**Why it matters:** The person who looks after a client's photos needs the final files as much as the owner does.

### LS-0022 · Estimate the client's content work on its own line
- Type: lesson
- Source: Project retro, Corrowin Dental site, 2026-09-30
- Tags: estimate, scope
- Links: LS-0006
- Added: 2026-09-30 by Project manager
- Status: new
- Sensitivity: internal

The dental practice's new site went live three weeks late, and most of the wait was for their copy and photos. Our estimate had folded their content work into ours. Next time, estimate the client's content work on its own line, with its own dates.

**Why it matters:** Clients see that the content is their work too, and the timeline stays honest.

### LS-0023 · New designers shadow one client handoff early
- Type: idea
- Source: Studio meeting, internal, 2026-10-01
- Tags: hiring, handoff
- Themes: new-hire-onboarding
- Links: LS-0020, LS-0024
- Added: 2026-10-01 by Designer
- Status: new
- Sensitivity: internal

New designers could shadow one client handoff in their first two weeks. Seeing what a client gets at the end makes our file and naming rules make sense.

**Why it matters:** [draft] New designers would learn why the handoff rules exist, not just what they are.

### LS-0024 · The handoff checklist helped the new designer most
- Type: insight
- Source: Onboarding check-in, internal, 2026-10-02
- Tags: handoff, process
- Themes: new-hire-onboarding
- Links: LS-0023
- Added: 2026-10-02 by Operations lead
- Status: new
- Sensitivity: internal

At her first check-in, our newest designer said the handoff checklist was the most useful thing she read in week one. It showed her how a project ends before she had seen one start.

**Why it matters:** The handoff checklist doubles as an introduction to how we work.

### LS-0025 · Collection only for this year's Christmas orders
- Type: decision
- Source: Week close, Halden Bakery orders, 2026-10-12
- Tags: scope
- Themes: halden-bakery-orders
- Links: LS-0032
- Added: 2026-10-12 by Project manager
- Status: new
- Sensitivity: internal

The bakery wanted home delivery as well as collection from the shop. With four weeks until the first orders, we agreed on collection only, put delivery on next year's list and wrote that on the first card of the project.

**Why it matters:** Saying what was out on the first day kept a four-week project to four weeks.

### LS-0026 · Ask whose name goes on the box
- Type: quote
- Source: Week close, Halden Bakery orders, 2026-10-12
- Tags: design-feedback, communication
- Themes: halden-bakery-orders
- Added: 2026-10-12 by Project manager
- Status: new
- Sensitivity: internal

> "Half our orders are presents, so ask whose name goes on the box as well as who is paying."

**Why it matters:** Gift orders need two names, and our first order form asked for only one.

### LS-0027 · Hold a collection slot while the customer pays
- Type: fix
- Source: Week close, Halden Bakery orders, 2026-10-19
- Tags: tooling
- Themes: halden-bakery-orders
- Links: LS-0028
- Added: 2026-10-19 by Project manager
- Status: new
- Sensitivity: internal

In testing, two people took the last collection slot at the same moment and it was overbooked. The page now holds a slot for ten minutes while someone pays, and frees it again if they leave without finishing.

**Why it matters:** An overbooked slot means a queue at the counter on the busiest mornings of the year.

### LS-0028 · Ask what the kitchen can bake each day first
- Type: lesson
- Source: Week close, Halden Bakery orders, 2026-10-19
- Tags: scope, process
- Themes: halden-bakery-orders
- Links: LS-0027
- Added: 2026-10-19 by Project manager
- Status: new
- Sensitivity: internal

We built the page with no daily limit, then learned the ovens manage about sixty orders a day. Adding the limit late meant reworking every slot. Next time, ask what the kitchen can bake each day before designing anything.

**Why it matters:** A shop's physical limits shape an order page more than its wish list does.

### LS-0029 · Shop staff found what our own testing missed
- Type: insight
- Source: Week close, Halden Bakery orders, 2026-10-26
- Tags: process, design-feedback
- Themes: halden-bakery-orders
- Links: LS-0030, LS-0031
- Added: 2026-10-26 by Project manager
- Status: new
- Sensitivity: internal

Two shop staff placed test orders on the counter tablet during a quiet hour. In twenty minutes they found three problems we had missed, including a button hidden behind the tablet's keyboard.

**Why it matters:** The people who use a page all day test it better than we do.

### LS-0030 · A printed slip for every order box
- Type: idea
- Source: Week close, Halden Bakery orders, 2026-10-26
- Tags: handoff, tooling
- Themes: halden-bakery-orders
- Links: LS-0029
- Added: 2026-10-26 by Project manager
- Status: new
- Sensitivity: internal

Staff asked for a slip for each order to tape to its box, with the name and collection time in large print. A print button on the order list could make these slips for the next shop we build for.

**Why it matters:** Staff at a busy counter read paper faster than a screen.

### LS-0031 · Open orders quietly for a day before announcing
- Type: lesson
- Source: Week close, Halden Bakery orders, 2026-11-02
- Tags: process, communication
- Themes: halden-bakery-orders
- Links: LS-0029
- Added: 2026-11-02 by Project manager
- Status: new
- Sensitivity: internal

The bakery announced the page the moment it went live, and the first hour brought forty orders and two small bugs at once. Next time, open it to regular customers for a day, fix what they find, then tell everyone.

**Why it matters:** [draft] A quiet first day finds the last bugs while little is at stake.

### LS-0032 · The owner's plans for a second shop
- Type: insight
- Source: Week close, Halden Bakery orders, 2026-11-02
- Tags: scope
- Themes: halden-bakery-orders
- Links: LS-0025
- Added: 2026-11-02 by Project manager
- Status: new
- Sensitivity: restricted

The owner told us in confidence that the bakery hopes to open a second shop next spring and will want delivery then. Keep this out of anything shared outside the studio.

**Why it matters:** It explains why delivery waits until next year, and it may be our next project.
