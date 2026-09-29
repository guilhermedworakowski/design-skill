# cognitive-biases

## Description

This file documents **18 cognitive biases and psychological laws** applied to digital product design, mapped directly against the agents and frameworks of this design skill.

Its purpose is twofold:

1. **As a reference for agents** — each bias entry specifies which agent should apply it and at which stage of the design process. Agents must cross-reference this file when making decisions about persuasion, information architecture, interaction design, or engagement strategy.

2. **As a study guide for the design team** — the file documents the theoretical foundation of each bias (name, description, best moment to apply, how to use, a practical example, and relations to other biases), alongside the exact design skill connections that make it actionable.

**Bibliographic sources:** *Enviesados* (Rian Dutra) · *Laws of UX* (Jon Yablonski) · *The Power of Habit* (Charles Duhigg) · *Thinking, Fast and Slow* (Daniel Kahneman) · *Influence* (Robert Cialdini).

**Scope:** This file is a standalone reference. It should not be imported into the skill automatically — it must be read deliberately when a bias-informed design decision is required.

---

## How to Read This File

Each entry follows this structure:

| Field | Description |
|---|---|
| **Description** | Theoretical foundation and cognitive mechanism |
| **Best Moment** | Where in the design process this bias has the highest impact |
| **How to Use** | Practical application patterns |
| **Example** | Practical application in real digital products (e-commerce, SaaS, fintech, education, streaming, etc.) |
| **Relations** | Other biases this one activates or is reinforced by |
| **Agent** | Which specialist agent is primarily responsible for applying it |
| **Framework** | Which design framework from `references/frameworks.md` this maps to |

---

## Biases

---

### 01 · Anchoring Bias

**Description**
The anchor is the first piece of information the brain receives, which becomes the central reference for all subsequent judgments. Kahneman and Tversky demonstrated that people rely heavily on the first number, price, or data point presented — even if irrelevant — adjusting estimates from it rather than starting from zero. In product, the way an option is presented first shapes how all others are perceived.

**Best Moment**
Ideation and UI Design — when defining price hierarchies, product ordering, dashboard data display, or any interface where comparison is part of the decision.

**How to Use**
- Present the highest price first (Premium plan) so that others appear more accessible by comparison.
- Display crossed-out prices alongside discounted values to anchor perceived value.
- In comparison tables, position the desired option as the central reference point.
- In dashboards, the first metric displayed sets the cognitive baseline for all others.

**Example**
SaaS pricing pages that list the Enterprise plan first make the Pro plan look accessible by comparison. E-commerce shows the original price crossed out next to the sale price to anchor perceived value. In analytics dashboards, the first number shown (e.g. last month's revenue) becomes the baseline against which every other metric is read — so its choice is a design decision, not a neutral one.

**Relations**
Decoy Effect · Framing Effect · Loss Aversion

**Agent**
Designer Engineer (UI execution) · Strategist (pricing and IA decisions)

**Framework**
Double Diamond (Ideation phase) · MoSCoW (value framing in feature prioritization)

---

### 02 · Social Proof

**Description**
In situations of uncertainty, humans use the behavior of others as a guide. Cialdini formalized this in *Influence* (1984): we follow what others do because we interpret it as evidence of the correct behavior. In digital environments, social proof reduces the cognitive effort of decision-making — if others have done it, it must be safe. The closer the reference person is to the user in profile, the stronger the effect.

**Best Moment**
UI Design, Prototyping, and Active Product — in registration flows, product selection, conversion pages, and retention touchpoints.

**How to Use**
- Display number of active users, ratings, and reviews close to the decision point.
- Use real testimonials with photo and name.
- Segment social proof by user niche ("Most popular among designers like you").
- Show activity counts that update in near real-time to signal vitality.

**Example**
Marketplaces show "1,200 people bought this in the last month" next to the Add to cart button. Course platforms display enrolled students and ratings beside the enroll CTA. B2B landing pages show logos of known customers above the fold. Segmented proof persuades more than a global count: "Popular with teams your size" beats "10,000 users".

**Relations**
Framing Effect · FOMO · Confirmation Bias

**Agent**
Designer Engineer (UI execution) · Researcher (validating which social signals users trust)

**Framework**
Qualitative Research — to identify which social proof signals are credible to the target user segment · A/B Testing — to validate which format (counts vs. ratings vs. testimonials) converts better

---

### 03 · Loss Aversion

**Description**
Kahneman and Tversky demonstrated that the pain of losing something is psychologically approximately 2× more intense than the pleasure of gaining an equivalent amount. Messages that highlight what the user will lose by not acting — rather than what they will gain — tend to convert better. Loss aversion is the foundation of all genuine urgency logic in product design.

**Best Moment**
UI Design and Active Product — especially in conversion flows, cancellation, retention, and reactivation sequences.

**How to Use**
- Write loss-framed CTAs: "Don't lose your exclusive offer" instead of "Claim your offer."
- In cancellation flows, show what the user will lose (saved work, history, settings, remaining credit).
- In time-limited promotions, emphasize the remaining time — not the benefit itself.
- In reactivation campaigns, lead with what the user has missed since their last session.

**Example**
"Your trial ends in 3 days — keep your projects and settings" outperforms "Upgrade now." In a subscription cancellation flow, showing the saved playlists, history or preferences makes the cost of leaving concrete — honestly, and without making cancellation harder. In reactivation emails, "Here's what you missed this week" drives more re-engagement than "We have new features."

**Relations**
Scarcity · FOMO · Framing Effect · Anchoring Bias

**Agent**
Designer Engineer (copy and UI framing) · Strategist (retention strategy design)

**Framework**
Double Diamond (Define phase — identifying where loss-aversion moments exist in the user journey) · Service Blueprint (mapping backstage triggers that can surface loss-framing to users at the right moment)

---

### 04 · Framing Effect

**Description**
The same information, presented in different ways, produces different decisions. Kahneman demonstrated that people react differently to "90% survival rate" vs. "10% mortality rate" — identical data. In design, framing controls how the user interprets a piece of data, an action, or an offer. The way a proposition is framed determines its perceived value, risk, and urgency.

**Best Moment**
UX Writing, UI Design, and Prototyping — in CTA microcopy, plan descriptions, status labels, feedback messages, and any content where interpretation determines action.

**How to Use**
- Use positive frames in onboarding ("You're one step away") and loss frames in conversion ("Don't miss out").
- In pricing, frame cost per day instead of per month.
- Progress frames ("85% complete") motivate more than deficit frames ("15% remaining").
- Phrase the same feature as a benefit to the user, not a technical description of the system.

**Example**
"Just $0.80 a day" lands differently than "$24 a month." "Your profile is 85% complete" motivates more than "Your profile is 15% incomplete." In a learning app, "Only 2 lessons to your certificate" builds aspiration through proximity. A backup feature described as "Never lose a file again" is more compelling than "Automatic cloud sync."

**Relations**
Anchoring Bias · Loss Aversion · Scarcity · Social Proof

**Agent**
Designer Engineer (copy execution) · Strategist (defining which frames align with product positioning)

**Framework**
Double Diamond (Define phase — reframing the problem space) · Jobs to Be Done (framing the product around user outcomes, not features)

---

### 05 · Decoy Effect

**Description**
When an asymmetrically dominated third option is inserted into a choice set, it pushes the user toward the option the designer intends. The classic experiment from *The Economist*: with three plans (digital $59 / print $125 / digital+print $125), 84% chose the bundle. Without the print-only decoy, the majority chose the cheaper digital option. The Decoy transforms a difficult binary choice into an obvious comparative one.

**Best Moment**
UI Design — when structuring plan tables, product versions, add-on options, or any interface presenting 3+ comparable choices.

**How to Use**
- Create a middle plan with an inferior cost-benefit ratio compared to the plan you want to sell.
- Always position the decoy adjacent to the preferred option.
- Use labels like "Most popular" or "Best value" to signal direction.
- Ensure the decoy is clearly dominated — the preferred option must be obviously superior.

**Example**
Subscription plans such as Basic $8 / Standard $14 / Premium $16: Standard works as the decoy that makes Premium feel like the obvious choice. Cinema popcorn (small $3 / medium $6.50 / large $7) follows the same logic. In storage or seat-based plans, a middle plan with barely more value than the entry plan pushes users toward the top plan.

**Relations**
Anchoring Bias · Framing Effect · Hick's Law

**Agent**
Designer Engineer (UI structure) · Strategist (plan and pricing architecture)

**Framework**
Double Diamond (Ideation phase — structuring solution options) · MoSCoW (framing feature packages by value level)

---

### 06 · Hick's Law

**Description**
Formulated by William Edmund Hick and Ray Hyman in the 1950s, this law establishes that the time to make a decision grows logarithmically with the number of available options. In contexts with too many choices, the user enters decision paralysis — and tends not to decide at all. This law underpins progressive onboarding design, simplified menus, and guided selection flows with progressive filters.

**Best Moment**
Information Architecture, Prototyping, and UI Design — in navigation systems, filters, forms, registration flows, and any product selection interface.

**How to Use**
- Reduce visible options per level. Reveal complexity progressively as needed.
- In onboarding, present one action per screen.
- Group related items to reduce the perceptual count of choices.
- Default selections and pre-filters reduce the active decision space without removing options.

**Example**
A large e-commerce catalog needs a clear hierarchy (department > category > subcategory) with smart pre-applied filters. Streaming services show curated rows ("Continue watching," "Top 10," "New") instead of the whole catalog at once. At checkout, showing the 3 most-used payment methods first, with the rest under "More options," reduces abandonment.

**Relations**
Miller's Law · Status Quo Bias · Decoy Effect

**Agent**
Designer Engineer (navigation and IA execution) · Strategist (information architecture definition)

**Framework**
Double Diamond (Define phase — structuring the solution space) · Flowcharts (mapping simplified decision paths)

---

### 07 · Miller's Law

**Description**
Psychologist George Miller demonstrated in 1956 that human working memory holds an average of 7 (±2) items simultaneously. Beyond that, information processing degrades. This limit defines how menus, forms, dashboards, and lists should be structured. The concept of "chunking" — grouping information into blocks — derives directly from this principle.

**Best Moment**
Information Architecture, UI Design, and Prototyping — especially in forms, navigation systems, and data-heavy displays.

**How to Use**
- Group items into blocks of no more than 7. In long forms, use visual sections with titles.
- In navigation, limit to 5–7 primary items.
- Apply chunking to long numbers (card number: 4242 4242 4242 4242, not 4242424242424242).
- In dashboards, show the 5–7 most critical metrics with an expand option for details.

**Example**
Sign-up and identity-verification forms perform better when split into clear steps (personal data > address > verification) with a progress bar. Analytics dashboards show no more than 7 primary KPIs with an "expand" option for details. Long codes — card numbers, tracking numbers, verification codes — are displayed in chunks.

**Relations**
Hick's Law · Zeigarnik Effect · Cognitive Load

**Agent**
Designer Engineer (form and data design) · Strategist (information architecture chunking)

**Framework**
Double Diamond (Prototype phase) · Flowcharts (chunking steps into digestible decision nodes)

---

### 08 · Zeigarnik Effect

**Description**
Psychologist Bluma Zeigarnik discovered in the 1920s that incomplete tasks remain more salient in memory than completed ones. The brain maintains a "cognitive tension" around the unfinished, generating a natural impulse to complete. This is the foundation of progress bars, gamified onboarding, and verification flows that reinforce incompleteness until the final action.

**Best Moment**
UI Design, Onboarding, and Active Product — in registration flows, account verification, courses and learning paths, and recurring engagement mechanics.

**How to Use**
- Use progress bars that start partially filled.
- Show what remains to complete ("2 steps left to activate your account").
- In courses and learning paths, display the gap between the current lesson and the end of the module.
- In push notifications, reference specific incomplete tasks to trigger re-engagement.
- Never show a fully empty progress bar — start at a minimum of 20% to create momentum.

**Example**
Profile-strength meters ("Your profile is 70% complete") keep users filling in details. Account-verification flows show "3 of 5 steps completed" with a visual bar. Abandoned-cart reminders reference the specific unfinished task: "You left 2 items in your cart." In learning apps, a daily goal with 4 of 5 lessons done creates stronger completion urgency than one just started.

**Relations**
Goal Gradient Effect · Habit Loop · FOMO

**Agent**
Designer Engineer (progress UI and onboarding) · Strategist (engagement and retention strategy)

**Framework**
Double Diamond (Ideation phase — identifying where incompleteness can be designed intentionally) · Opportunity Solution Tree (mapping incomplete flows as product opportunities)

---

### 09 · Goal Gradient Effect

**Description**
The closer an individual is to a goal, the greater the intensity of effort applied to reach it. Clark Hull's classic experiment with rats in mazes showed that speed increased as they approached the reward. In digital products, this explains why progress bars near the end are more motivating than at the start, and why checklists and courses that highlight how little is left increase completion.

**Best Moment**
UI Design and Active Product — in onboarding, verification flows, courses, fundraising goals, and gamified challenges.

**How to Use**
- Display visual progress with increasing visual emphasis as the goal approaches.
- Add a small extra incentive (e.g. unlocking a feature, a completion badge) when the user is within 20% of the target.
- Use messages that become more specific as the user closes in ("Only 2 steps left!").
- Introduce "almost there" micro-celebrations at 80% and 90% completion milestones.

**Example**
Crowdfunding and fundraising campaigns receive more contributions as they approach their goal — showing "87% funded" with a prominent progress bar makes that proximity visible. In learning apps, "Only 2 lessons left" plus a visible certificate accelerates course completion. Fitness apps' activity rings that intensify as they near 100% apply Goal Gradient visually. In a setup checklist, making the last step the simplest one keeps the final push from stalling.

**Relations**
Zeigarnik Effect · Habit Loop · Loss Aversion

**Agent**
Designer Engineer (progress UI design) · Strategist (goal and challenge architecture)

**Framework**
Opportunity Solution Tree (identifying goal-gradient opportunities within the user journey) · Double Diamond (Prototype phase — testing goal-gradient mechanics)

---

### 10 · Habit Loop

**Description**
Charles Duhigg describes in *The Power of Habit* that every habitual behavior is composed of three elements: **Cue (Trigger) → Routine → Reward**. The cue is the stimulus that initiates the behavior; the routine is the action itself; the reward is what reinforces the circuit and creates anticipatory desire. With repetition, the loop is automated in the basal ganglia and occurs without conscious effort. Products that build intentional habit loops are harder to abandon, because changing a habit requires substituting the routine — not eliminating the loop.

**Best Moment**
Product Strategy and UI Design — from the initial product definition through to recurring engagement flow construction.

**How to Use**
- Identify the user's natural trigger (notification, time of day, a recurring event).
- Reduce routine effort (one tap to complete the core action, fast interface, no friction in the critical path).
- Deliver immediate and variable rewards (surprise content, a useful tip, achievement recognition).
- Design secondary loops that carry over into the next session.

**Example**
A language-learning app: Cue = reminder at the time the user chose → Routine = a 5-minute lesson, one tap away from the notification → Reward = streak count, XP and a short celebration. A fitness app: Cue = morning notification → Routine = log a workout → Reward = the progress ring closes. Duhigg's Pepsodent case shows that immediate sensory reward is critical — visual, sound and haptic microfeedback right after the core action is the product's "tingling sensation."

**Relations**
Goal Gradient Effect · Zeigarnik Effect · FOMO · Variable Ratio Reinforcement

**Agent**
Strategist (habit loop architecture and engagement strategy) · Designer Engineer (notification design and reward feedback)

**Framework**
Jobs to Be Done (mapping the functional, emotional, and social job the habit loop fulfills) · Service Blueprint (mapping the full loop across frontstage and backstage touchpoints)

---

### 11 · Scarcity Bias & FOMO

**Description**
Scarcity increases the perceived value of an opportunity simply through its limitation. FOMO (Fear of Missing Out) is the emotional dimension of scarcity — the fear of being excluded from something others are experiencing. Together, they create powerful urgency. Scarcity can be of quantity ("only 3 available"), time ("offer expires in 2h"), or access ("exclusive for beta testers"). Authenticity is critical: fabricated scarcity destroys trust.

**Best Moment**
UI Design and Active Product — in promotions, live events, product launches, and conversion flows where time or availability is genuinely limited.

**How to Use**
- Use visual countdown timers on promotions with real deadlines.
- Display remaining availability ("only 12 spots left for this workshop").
- Create segment-exclusive offers (active users, beta testers, long-time customers) that reinforce limited access.
- For live contexts, surface the natural time constraint of the event itself.
- Never fabricate scarcity — only apply where the limitation is real.

**Example**
Travel and ticketing products show "Only 3 seats left at this price" when inventory really is limited. Live events and webinars have a natural time constraint: "Registration closes in 2 hours." Limited-edition product drops display real remaining stock. Early-access or member-only offers create legitimate exclusivity. In every case, the limit shown must be the limit that exists.

**Relations**
Loss Aversion · Social Proof · Framing Effect · Habit Loop

**Agent**
Designer Engineer (UI countdown and availability display) · Strategist (promotion architecture and segmentation)

**Framework**
A/B Testing (testing scarcity message formats and their conversion impact) · Service Blueprint (mapping where authentic scarcity moments exist across the user journey)

---

### 12 · Peak-End Rule

**Description**
Kahneman demonstrated that people do not evaluate an experience by averaging all its moments, but by two specific points: the emotional peak (the most intense moment, positive or negative) and the end (how it concluded). An experience can have many mediocre moments — but if the peak and end are positive, it will be remembered positively. This has direct implications for onboarding, offboarding, and celebration moment design.

**Best Moment**
UI Design and Testing — when reviewing complete flows, identifying high-emotion moments, and designing session endings.

**How to Use**
- Deliberately design the moments of highest emotional intensity (first purchase, first completed goal, first milestone reached).
- Ensure session endings are positive regardless of the outcome (encouragement message, next goal available, progress-saved framing).
- Use animation and visual feedback at celebration moments.
- In research, evaluate experiences by peak and end moments — not averages.

**Example**
In e-commerce, the peak is the purchase confirmation — a clear, warm success screen with order summary and delivery estimate matters more than shaving a second off checkout. A support conversation should end with a resolution summary and a friendly close. In SaaS onboarding, the "aha moment" (first report generated, first file shared with the team) is the peak to accelerate and celebrate. Even when a session ends badly (declined payment, failed upload), the ending should offer a clear way forward.

**Relations**
Zeigarnik Effect · Habit Loop · Social Proof

**Agent**
Designer Engineer (celebration and session-end UI) · Researcher (identifying peak and end moments through usability testing and session analysis)

**Framework**
Qualitative Research (surfacing which moments users describe as most memorable) · Usability Testing (observing emotional peaks and how users describe the end of a session)

---

### 13 · Von Restorff Effect

**Description**
Also called the Isolation Effect: an item that stands out visually from its context is significantly more memorable and more likely to be selected. Identified by psychologist Hedwig von Restorff in 1933, this principle is the foundation of highlighted CTA design, "Most popular" badges, and any interface element that requires priority attention. Used sparingly, it creates clear hierarchy; overused, it cancels itself out.

**Best Moment**
UI Design — when designing visual hierarchy, CTAs, badges, and featured elements in any interface with multiple competing items.

**How to Use**
- Use color, size, weight, or shape to distinguish the priority element from its context.
- In pricing tables, highlight the recommended plan with a different background color.
- Apply sparingly — if everything stands out, nothing does. One Von Restorff element per context.
- Combine with Anchoring: the visually isolated element becomes the cognitive anchor.

**Example**
Pricing tables highlight the recommended plan with a different background and a "Most popular" badge. Sale prices stand out from regular prices through color and size. In a notification list, unread items are visually isolated. In navigation, a single "New" badge or live indicator should be the most visually distinct element — never several at once.

**Relations**
Framing Effect · Scarcity · Anchoring Bias

**Agent**
Designer Engineer (visual hierarchy and badge design)

**Framework**
Double Diamond (Prototype phase — testing whether the isolated element is correctly identified as the priority)

---

### 14 · Serial Position Effect

**Description**
Hermann Ebbinghaus described that people better remember items at the beginning (primacy effect) and end (recency effect) of a list, forgetting those in the middle. In navigation lists, onboarding sequences, or menus, item positioning is not neutral — the extremes capture more attention and memory than the center.

**Best Moment**
Information Architecture and UI Design — when defining item order in navigation systems, product lists, onboarding sequences, and menus.

**How to Use**
- Place the most important items at the beginning and end of lists and navigation.
- Avoid burying critical actions in the middle of long flows.
- In onboarding, start with a quick win (primacy) and close with the most valuable action (recency).
- In navigation with 5+ items, audit what sits in positions 2–4 — those are the weakest positions.

**Example**
In primary navigation, the most important destination takes the first slot, and the last slot often holds a high-value destination (cart, profile, notifications). In product listings and search results, positions 1–3 and the last visible items get the most clicks — curating those slots has direct revenue impact. In onboarding, start with a quick win and end with the most valuable action (inviting the team, connecting the first integration) rather than burying it in the middle.

**Relations**
Miller's Law · Hick's Law · Von Restorff Effect

**Agent**
Designer Engineer (navigation and list design) · Strategist (information architecture ordering)

**Framework**
Double Diamond (Define phase — structuring navigation priorities) · Flowcharts (mapping which steps anchor the start and end of each flow)

---

### 15 · Jakob's Law

**Description**
Formulated by Jakob Nielsen: users spend most of their time on other digital products, and therefore expect your product to work the same way they do. When a product deviates significantly from established patterns, cognitive load increases and frustration follows. Familiarity reduces learning effort and accelerates adoption. Innovation should live in the experience — not in the conventions.

**Best Moment**
Discovery and Prototyping — when defining interaction patterns, nomenclature, and element location in the interface.

**How to Use**
- Follow market conventions for critical elements (cart in the top right, logo in the top left, primary CTA in an accent color).
- Innovate in experience — not in convention. Reserve originality for genuine differentiation moments.
- Benchmark competitors before designing any navigation or core interaction pattern.
- When deviating from convention, validate with usability testing before shipping.

**Example**
E-commerce users expect the cart at the top right, search at the top and a checkout pattern shaped by the big marketplaces they already use. A banking app that moves the transfer action away from where other banking apps put it generates errors and support tickets. Innovation should live in the product's value — speed, pricing, content, service — not in the conventions users have already internalized. The checkout must behave exactly as users expect; any surprise there costs conversion.

**Relations**
Hick's Law · Status Quo Bias · Cognitive Load

**Agent**
Researcher (benchmarking existing patterns) · Designer Engineer (convention compliance in prototypes)

**Framework**
Benchmarking (auditing competitor interaction patterns before deviating from them) · Usability Testing (validating whether any convention deviation creates confusion)

---

### 16 · Confirmation Bias

**Description**
The systematic tendency to seek, interpret, and remember information that confirms pre-existing beliefs, while ignoring contrary evidence. In the design process, confirmation bias is one of the greatest threats to research quality — the designer tends to interpret test data as validation of hypotheses already held. For the user, it reinforces past behavioral patterns and choices, creating behavioral consistency with choices already made.

**Best Moment**
Discovery and Research (mitigate in the design process). Active Product (leverage to reinforce the user's choice after conversion).

**How to Use**
- In the design process: use red teams to challenge hypotheses. Document assumptions before researching.
- After conversion, reinforce the user's decision with data that confirms the quality of their choice ("You chose one of the best-rated plans in its category").
- Design post-decision screens that validate the action taken rather than leaving the user in uncertainty.

**Example**
After a purchase or subscription, messages like "Great choice — this is our best-rated plan" reduce post-decision dissonance (buyer's remorse). In SaaS products, a periodic summary of what the user achieved (hours saved, reports generated, projects delivered) confirms that staying has been worth it, reducing churn. Inside the design team, having someone red-team research conclusions before they are presented keeps the team from seeing only what it expected to see.

**Relations**
Social Proof · Availability Heuristic · Peak-End Rule

**Agent**
Researcher (mitigating it during the research process) · Designer Engineer (leveraging it in post-conversion UI)

**Framework**
Qualitative Research (structured interview techniques that counteract confirmation bias in data collection) · A/B Testing (using quantitative data to override qualitative confirmation bias in design decisions)

---

### 17 · Variable Ratio Reinforcement (VRR)

**Description**
Formulated by behavioral scientist B.F. Skinner, this principle describes the most powerful reward schedule for sustaining behavior: rewarding at unpredictable intervals. Unlike fixed, predictable rewards (which lose impact over time), variable rewards maintain elevated engagement because the brain anticipates a reward at every interaction. Social feeds and email inboxes operate on this logic — every refresh could bring something new. Ethical applications include surprise notifications, unexpected perks, and varied content.

**Best Moment**
Product Strategy and UI Design — in the design of reward systems, push notifications, and recurring engagement loops.

**How to Use**
- Introduce surprise rewards at unexpected moments (2nd purchase of the week, first weekly login, 10th order of the month).
- Vary the type of reward — sometimes free shipping, sometimes early access, sometimes a personalized recommendation.
- Avoid total predictability in reward systems — the surprise is part of the value.
- Never apply VRR to manipulate vulnerable users — limit to genuinely positive reinforcement.

**Example**
An e-commerce app can offer a "surprise" at unpredictable moments — free shipping on an order, early access to a sale. Learning apps vary the reward (badges, XP boosts, streak freezes) to keep practice engaging. Social feeds and inboxes run on VRR by nature — every refresh might bring something new — which is exactly why this mechanism demands the strongest ethical care, especially with users showing signs of compulsive use.

**Relations**
Habit Loop · Goal Gradient Effect · Scarcity

**Agent**
Strategist (reward system architecture) · Designer Engineer (notification timing and reward UI design)

**Framework**
Opportunity Solution Tree (mapping VRR-driven reward moments as product opportunities) · A/B Testing (testing reward frequency and type to optimize engagement without dependency)

---

### 18 · Fitts's Law

**Description**
Paul Fitts demonstrated in 1954 that the time to reach a target is a function of the distance to the target and its size. The larger and closer an interactive element, the faster and more accurate the click or tap. This law has direct implications for mobile interface design, where inadequate touch areas are a frequent cause of errors, frustration, and task abandonment.

**Best Moment**
Prototyping and UI Design — when defining size, spacing, and positioning of interactive elements, especially in mobile interfaces.

**How to Use**
- Primary CTA elements must be large (minimum 44×44pt on mobile).
- Frequent actions must be in comfortable reach zones (bottom third of the screen on mobile, reachable with the thumb).
- Increase the size of critical targets proportionally to their importance.
- Separate destructive elements (delete, cancel) from constructive elements to prevent accidental activation.

**Example**
The "Place order" or "Pay" button at checkout is the most critical target of an e-commerce product — large, well-positioned and visually distinct. On mobile, primary CTAs belong in the bottom third of the screen for thumb reach. Keeping "Delete" away from "Save" reduces accidental errors. In apps used on the move (ride-hailing, delivery, navigation), critical buttons must be large enough to hit accurately while walking or in a vehicle.

**Relations**
Miller's Law · Jakob's Law · Cognitive Load

**Agent**
Designer Engineer (mobile UI sizing and touch target design)

**Framework**
Double Diamond (Prototype phase — validating touch target accuracy in usability testing) · Usability Testing (observing tap accuracy on critical targets)

---

## Cross-Bias Relationships

The following table maps how biases reinforce each other. Understanding these connections enables layered engagement strategies where a single design decision activates multiple cognitive mechanisms simultaneously.

| Bias | Activates / Is Reinforced By |
|---|---|
| **Anchoring Bias** | Decoy Effect (reinforces the reference point) · Framing Effect (defines the anchor frame) · Loss Aversion (high anchor amplifies the fear of losing the discount) |
| **Loss Aversion** | Scarcity (amplifies the fear of missing the opportunity) · FOMO (emotional version of loss) · Framing Effect (loss vs. gain frames) |
| **Habit Loop** | Goal Gradient (accelerates approach to the reward) · Zeigarnik Effect (maintains tension between sessions) · VRR (keeps the loop unpredictable and engaging) |
| **Social Proof** | Framing Effect (how social signals are presented changes impact) · FOMO (others are doing it = I'm losing) · Confirmation Bias (reinforces an already-made decision) |
| **Hick's Law** | Miller's Law (option limit + memory limit are complementary) · Decoy Effect (3 options + decoy is the classic implementation) |
| **Zeigarnik Effect** | Goal Gradient (incompleteness accelerates the final push) · Habit Loop (the tension of the unfinished is the trigger for the next loop) |
| **Peak-End Rule** | Habit Loop (the peak is the reward; the end is the loop closure) · Social Proof (shared peaks generate social proof) |
| **Von Restorff** | Anchoring Bias (the isolated element becomes the anchor) · Scarcity (visual isolation reinforces perceived rarity) |
| **VRR** | Habit Loop (variability makes the loop unpredictable and stronger) · Goal Gradient (variable rewards near the goal accelerate effort) |
| **Framing Effect** | All biases — framing is the meta-layer through which every other bias is delivered |

---

## Agent × Bias Responsibility Map

| Agent | Primary Biases | Role |
|---|---|---|
| **Researcher** | Confirmation Bias · Jakob's Law · Peak-End Rule · Framing Effect | Identifies where biases affect user behavior; mitigates them in the research process; surfaces findings that inform how biases should be applied in design |
| **Strategist** | Habit Loop · Goal Gradient · VRR · Scarcity · Loss Aversion · Decoy Effect | Defines the engagement architecture, reward system, and pricing strategy where these biases operate at the systemic level |
| **Designer Engineer** | Anchoring · Von Restorff · Zeigarnik · Fitts's Law · Hick's Law · Miller's Law · Serial Position · Framing (copy) | Executes bias-informed decisions at the interface level — visual hierarchy, copy, touch targets, navigation, and feedback patterns |

---

## Ethical Note on Behavioral Design

### What Persuasion vs. Manipulation Means

There is a clear line between **persuasive design** — which uses cognitive biases to help users make decisions aligned with their own genuine goals — and **dark patterns** — which exploit biases to manipulate users against their own interests.

Persuasive design builds long-term trust and retention. Dark patterns generate short-term conversion and long-term trust destruction. In products that handle money, health or personal data — or that reach vulnerable users — the designer's ethical responsibility is amplified.

**The practical test:** Ask whether the bias is facilitating what the user genuinely wants to do, or tricking them into doing what you want them to do. The second answer is a dark pattern.

---

### Dark Patterns to Avoid

The following are specific dark pattern implementations of the biases documented in this file. They must never be used in products designed with this skill.

| Dark Pattern | Bias Exploited | Why It Is Prohibited |
|---|---|---|
| **Fabricated scarcity** ("Only 2 left!" when inventory is unlimited) | Scarcity · Loss Aversion | Destroys trust when discovered; violates user honesty expectations |
| **Infinite countdown timers** (timers that reset when they expire) | Scarcity · FOMO | Manufactures urgency that is not real; erodes brand credibility |
| **Hidden cancellation costs** (surfacing loss framing only after the user tries to cancel, not before) | Loss Aversion · Framing Effect | Traps users through information asymmetry rather than genuine value |
| **Roach motel** (easy to sign up, nearly impossible to cancel) | Habit Loop · Status Quo Bias | Retains users through friction, not value; generates regulatory risk |
| **Confirmshaming** ("No thanks, I don't want to save money") | Framing Effect · Loss Aversion | Emotionally manipulates the secondary option to coerce the primary action |
| **Trick questions** (double negatives or confusing language in opt-out checkboxes) | Cognitive Load · Framing Effect | Exploits cognitive load to obtain consent users would not otherwise give |
| **False social proof** (fake reviews, fabricated user counts, non-existent testimonials) | Social Proof | Direct deception; illegal in most markets under consumer protection law |
| **Artificial near-misses** (feedback designed to make users feel they "almost" got a reward, prize or goal more often than reality, so they keep trying) | VRR · Loss Aversion | Psychologically manipulates vulnerable users; exposed to consumer protection regulation |
| **Misdirection** (attention drawn to a distracting element while a harmful action is triggered elsewhere) | Von Restorff · Cognitive Load | Deliberate deception through visual manipulation |
| **Disguised ads** (content formatted identically to editorial content without disclosure) | Social Proof · Confirmation Bias | Regulatory violation; destroys user trust |
| **Forced continuity** (charging users after a free trial without a clear reminder) | Loss Aversion · Status Quo Bias | Financial harm through deliberate friction in the cancellation path |

---

### Designer Checklist Before Shipping Any Bias-Informed Feature

Before any feature that applies the biases documented here ships to production, the Designer Engineer must confirm:

- [ ] The scarcity signal is real — not fabricated or exaggerated.
- [ ] The urgency message reflects an actual deadline or constraint.
- [ ] The social proof data is accurate and verifiable.
- [ ] Loss framing is used to help users act on genuine value — not to create anxiety.
- [ ] The cancellation or opt-out path is as easy to find and complete as the sign-up path.
- [ ] The variable reward system does not target users showing signs of compulsive use or other vulnerability.
- [ ] The copy has been reviewed against the tone of voice in `references/patterns.md`.
- [ ] The feature has been evaluated against the heuristic for user control and freedom (`references/heuristics.md`).
