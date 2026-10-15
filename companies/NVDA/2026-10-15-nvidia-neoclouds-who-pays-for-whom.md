# Is Nvidia paying for its own demand? What the filings show about Nvidia, circular financing and the neoclouds

**Format:** Free-form (interactive companion planned) · **Published:** 2026-10-15 · **Version:** 1.0 · **Author:** Christian Awori
**Data:** [`data/`](data/) · **Sources:** table at the end of this document

## Headline verdict

Nvidia's financing loop is real but narrow: most of its sales come from cloud giants paying their own way. The part to watch is a $105 billion guarantee backing OpenAI's data center leases, the one place where Nvidia pays if a customer can't. Among the smaller "neocloud" companies, the question isn't whether demand exists but who can fund the build, and Nscale and IREN are the most exposed.

## Why it matters

Nvidia sits at the center of the AI buildout. If a meaningful share of its demand is financed by Nvidia itself, its growth could be less durable than it looks. If the loop is narrow, the risk sits with a few counterparties instead. Knowing which, and where, tells you what to watch.

## What this read covers

1. What makes Nvidia hard to replace, and where that is weakest.
2. How much of its business is a loop, tested against Nvidia's own quarterly report.
3. The neoclouds, each with a good case and a bad case.
4. Which of those could struggle even if AI demand holds up.

## The evidence

## 1. Nvidia stopped being a chip company

Ask most people what Nvidia sells and they'll say chips. That was true a few years ago. Today it sells something closer to a complete AI data center: the processors, the cables and switches that tie thousands of them into one machine, and the software that runs on top.

**The scale.** In fiscal 2026 (the year ending January 2026), Nvidia's revenue was **$215.9B**, up 65%. About 90% of that, **$193.7B**, came from its Data Center business, which is the AI hardware [S1]. In the latest quarter, to July 26, revenue was $96.2B and Data Center was about 92% of it [S3, S5].

**A new yardstick.** Nvidia now measures its own growth by how much it earns for each *gigawatt* of data center capacity it helps fill. (A gigawatt is a measure of electrical power. It's the unit the industry uses to size big data centers.) *What to notice: the dollar amount per gigawatt keeps climbing because Nvidia keeps adding more to the package.*

| Generation | Nvidia revenue per gigawatt | What's in the package |
|---|---|---|
| Hopper | about $18B | Mostly the GPU chips |
| Blackwell | about $25B | Chips, plus fast links between them and networking |
| Vera Rubin (shipping now) | about $40B | Adds a CPU, more networking options, and Groq's inference chip |

*Source: Nvidia CFO on the Q2 FY27 call [S3].*

By our math, Rubin earns Nvidia 1.6 times what Blackwell does for the same gigawatt ($40B ÷ $25B). Even if gross margin slips to the 72–73% Nvidia has guided for fiscal 2028 (gross margin is what's left of each sales dollar after the direct cost of making the product), gross profit per gigawatt still rises about 55%. That's $40B × 72.5% = $29.0B, against $25B × 75% = $18.75B. Nvidia's own numbers for its Ohio campus point the same way: it says one generation of equipment there could mean $150–200B of Nvidia revenue over about 4.25 gigawatts, or roughly $35–47B per gigawatt by our math [S2, S3].

### Why it's hard to replace: three layers

*What to notice: the chip is the layer competitors can copy. The layers around it are what's hard to copy.*

| Layer | In plain terms | What the evidence shows | How strong |
|---|---|---|---|
| **1. The chip** | The processors that do the AI math | The giant cloud companies design their own, and rivals sell alternatives. Anthropic, for example, signed a multi-gigawatt deal for Google and Broadcom chips in April 2026 (reported) [S15] | The weakest layer. Competitors can match it |
| **2. The system and the network** | The links that make thousands of chips act as one computer, sold as full racks | Networking sales passed **$31B** in fiscal 2026 [S4]. Networking was $11B in the fourth quarter alone, up more than 3.5 times from a year earlier [S4]. Rack-sized "Grace Blackwell" systems were about two-thirds of Data Center sales in the fourth quarter of fiscal 2026 [S4] | The strongest layer. It's sold as one package, so replacing one piece means rebuilding the rest |
| **3. The software and platform** | The programming tools developers already know, plus services | Nvidia doesn't report software revenue separately. It says it has a revenue-sharing model with neocloud customers but doesn't give the size [S3]. It also pays for cloud capacity to build its own AI models (Nemotron, Cosmos, GR00T) [S2] | Real, but we can't put a number on it from public filings, so we don't |

**Our view.** Most of Nvidia's staying power sits in the middle layer. Anyone can build a good chip. Building a rack-sized system with the networking, and getting a customer to switch the whole thing, is much harder.

### Can Nvidia keep charging what it charges?

**What supports it**
- Gross margin held at **75.0%** for two quarters in a row [S5]. That's unusual for a hardware company.
- Nvidia says it has Vera Rubin orders from every major cloud giant, AI cloud company and system builder. It gave its first-ever full-year forecast: fiscal 2028 revenue up about **70%**, which it describes as limited by how much it can build, not by demand. It guided the next quarter to **$108B**, plus or minus 2%, and says that outlook assumes no data center compute sales to China [S3].
- Customers outside the large cloud providers (Nvidia's "ACIE" group, which includes the AI cloud companies) bought **$40.3B** of Data Center products last quarter, up 138% from a year earlier. The large cloud providers bought $48.7B, up 102% [S3]. Demand is broadening.

**What cuts against it**
- Nvidia guided gross margin down: 74% next quarter, a low of 71–72% in the fourth quarter of fiscal 2027, and 72–73% in fiscal 2028 [S3, S5]. It blames higher memory-chip costs, not discounts. That matters: it's a cost squeeze, not (yet) customers pushing prices down.
- Nvidia has committed **$279B** to suppliers, up from $119B a quarter earlier, mostly for memory [S3]. Those are bills if demand slows.
- A few buyers account for a lot. One direct customer was **16%** of last quarter's sales, and five direct customers hold 70% of receivables (22%, 14%, 13%, 11% and 10%; our math) [S2]. "Direct customers" are often system builders, so the end buyers aren't named.

**Our view.** Management's own forecast says pricing power holds through fiscal 2028. The margin slide so far comes from rising costs. The thing to watch is whether it stays a cost story or turns into a price story.

---

## 2. Is Nvidia paying for its own demand?

The charge goes like this: Nvidia invests in a company, the company spends that money on Nvidia products, and Nvidia books the sale. If that were the whole business, its growth would be a loop. In finance this is called *circular financing*, or *vendor financing*.

There are three ways a supplier can do it: take a stake in the customer, buy services back from the customer, or promise to cover the customer's bills. Nvidia does all three. Its quarterly report (the 10-Q for the quarter ended July 26, 2026) and its CFO commentary say how big each one is [S2, S3].

*What to notice: the big numbers aren't all the same kind of risk. The last row is the one that behaves like a loan.*

| What | Amount | How it works | What could go wrong |
|---|---|---|---|
| **Stakes in other companies** | **$99B** | By our math: $42.8B publicly traded + $51.2B private (including $3.3B in "infrastructure financiers") + about $5.0B long-term public holdings | Valued at current prices. About $36.9B of the public holdings are under short-term lock-up restrictions, so they can't all be sold at once. H1 gains of **$23.7B** were booked in "other income" and can reverse |
| **Stakes promised, not yet paid** | **$25B** | Commitments to invest more, $18B of it due in the rest of this fiscal year | A future cash outlay |
| **AI cloud agreements** | **$36B** | Clouds buy Nvidia systems, and Nvidia commits to rent computing time from them (about six years). The filing says the clouds can stop supplying it and sell to others at better rates, and the amount shrinks as others use it. This is separate from Nvidia's own $29B of R&D cloud spending | Lower risk. Nvidia gets usable capacity, and the commitment falls if the cloud finds other buyers |
| **Leases to pass on** | **$20B** | Data center leases of about 15 years that Nvidia signed and expects to reassign to third parties | If Nvidia can't reassign them, it keeps the lease |
| **Promises to cover bills (guarantees)** | **up to $108.5B** | **$105B** is a cap on credit support for a campus in Ohio (about 4.25 gigawatts, leased to OpenAI for 20 years), signed in August after the quarter closed. **$3.5B** more covers some neocloud partners' leases, with $0.7B held in escrow | If the customer can't pay the lease, Nvidia has to. It phases in as data centers become ready, the first expected in fiscal 2029, and shrinks as OpenAI pays. Nvidia also has an option to support about 3.8 more gigawatts at the site |

**Other pieces of the picture**
- **Payment terms.** Receivables rose to $63.1B from $38.5B in January. Days sales outstanding went from 45 to 60 since the prior quarter because of extended terms on large multi-quarter deals with investment-grade customers. Terms can run from 90 days to a year [S2, S3].
- **Nvidia says why it does this.** The CFO commentary says many AI clouds and model makers are growing faster than their balance sheets and credit can support, so Nvidia is helping select customers secure land, power and data center capacity [S3].
- **Other people's money.** Alongside its results, Nvidia announced partnerships with Apollo, BlackRock, Blackstone, Brookfield, Goldman Sachs and KKR to mobilize more than $500B of third-party capital over time [S3]. That is not Nvidia's own money, but Nvidia is arranging it.
- **Nvidia is borrowing too.** It issued $25.0B of senior notes in the second quarter for general corporate purposes [S3].

**The named deals.** OpenAI: $30B in February 2026, part of a $110B round at a $730 billion pre-money valuation, per OpenAI's announcement. Jensen Huang has said a $100B investment is probably not in the cards [S6]. CoreWeave: $2B in January 2026 (22,935,780 shares at $87.20, per its SEC filing), on top of a September 2025 agreement for Nvidia to buy CoreWeave's unsold capacity, reported at $6.3B through 2032 [S6, S8]. Intel: a $5B commitment [S2b]. Anthropic: up to $10B from Nvidia and up to $5B from Microsoft, alongside Anthropic's commitment to buy $30B of Azure computing, announced jointly on November 18, 2025 [S15]. Nscale: $1B of a $3.1B loan round, plus a lease guarantee of about $860M (reported) [S11].

### The case that it's a loop
1. **Money goes round.** Nvidia invests, and the company (OpenAI, CoreWeave, Nscale) buys Nvidia systems.
2. **Buy-back deals.** The $36B means Nvidia is paying companies that bought its own equipment.
3. **Risk moves onto Nvidia.** The $105B guarantee backs capacity that Nvidia says could mean $150–200B of Nvidia revenue per generation. OpenAI's lease risk is Nvidia's risk. It's the only item that works like a loan [S3].
4. **The spending is large and recent.** Nvidia spent **$42.4B** buying equity securities in the first half, versus $1.2B a year earlier [S2].
5. **Earnings quality.** GAAP net income for the half was $118.0B against Nvidia's own non-GAAP $99.5B. The gap is $18.5B, 16% of GAAP income by our math, and mostly gains on holdings in AI companies. These are paper gains, not cash [S2, S3].
6. **Longer payment terms.** Receivables are up sharply on extended terms for large customers [S2, S3].

### The case that it isn't
1. **Most demand pays its own way.** The large cloud providers bought $48.7B of the $89.0B Data Center total last quarter, 54.7% by our math [S3]. They fund their own building. Their combined 2026 spending plans come to at least $715B by our math, from each company's latest guidance: Alphabet $195–205B, Microsoft $190B, Meta $130–145B and Amazon $200B or more [S14].
2. **Nvidia makes its own cash.** First-half free cash flow was $69.9B, more than the $42.4B it spent on equity purchases, and cash from operations was $74.4B [S3, S2]. Net of $7.2B of sales, equity spending was $35.2B, 47% of operating cash flow by our math.
3. **The buy-backs shrink on their own.** The $36B falls as outside customers use the capacity.
4. **The guarantee is capped and phased.** It starts in fiscal 2029 and falls as OpenAI pays [S3].
5. **Huang says the big checks are done.** He has said the OpenAI $30B may be the last such investment before an OpenAI IPO [S6].

### Our view
"Circular" is a fair label for a slice of Nvidia's business, not the whole. The biggest source of its sales, the large cloud providers' own spending, isn't Nvidia-financed. But the slice is not small: Nvidia spent $42.4B on equity in six months, about a quarter of first-half revenue, and says it is arranging help for customers whose balance sheets can't keep up. The piece to watch is the **$105B guarantee**. It's the only place where Nvidia pays if a customer can't, it rests on a single customer, and by our math it's about 1.5 times Nvidia's first-half cash from operations. It builds up slowly, starting in fiscal 2029. The stakes are the item most likely to move reported profit, up or down. The buy-backs are the least worrying.

---

## 3. The neoclouds, one at a time

A **neocloud** is a newer company that rents out AI computing power. They exist because the giant cloud companies (Microsoft, Amazon, Google, Meta) couldn't build data centers fast enough. Neoclouds buy Nvidia chips, paying with borrowed money, customer prepayments and new shares, and rent them out under long contracts. Four are covered here.

**Four terms you'll see**
- **Backlog / contract value:** signed deals for service that hasn't been delivered yet. It becomes revenue only as the company builds and delivers.
- **Prepayments:** customers paying part of a contract up front, which helps fund the buildout.
- **Convertible notes ("converts"):** loans that can turn into shares, which dilutes existing owners.
- **Liquidity:** cash plus money the company can still borrow.

*What to notice: all four are growing very fast and losing money, but for different reasons, and they differ in how much of their signed business is actually live.*

| | CoreWeave | Nebius | IREN | Nscale |
|---|---|---|---|---|
| Period | Q2 2026 | Q2 2026 | Year to June 2026 | First half 2026 |
| Revenue | $2.575B (up 112%) | $582M (up 454%) | $707M (AI cloud $128.8M) | $140.6M |
| Net result | Loss of $626M | Loss of $190M (before one-off items, loss of $33M; operating profit before depreciation, +$236M) | Loss of $703M ($639M is a non-cash write-off) | Loss of $1.02B |
| Debt and funding | $35.55B of debt; $15.55B liquidity | $8.04B cash; about $10B of converts at Mar 31, plus $5.75B issued in Aug | $14B of cash and committed financing, against a $25–30B spending plan for FY27 | $3.1B of converts; $4.6B+ of debt raised in 2026 |
| Customer exposure | Top three customers = 72% of Q2 revenue | Microsoft and Meta anchor it; exact shares not found in filings | Microsoft ($9.7B, five years) plus a frontier AI lab | Largest customer = 52% of H1 revenue; Microsoft + Anthropic = 85% of contract value |
| Signed business | About $104B | $40B+ | $4B contracted annual run-rate ($1B live today) | $103.4B contract value; $2.6B live |

*Sources: CoreWeave [S8], Nebius [S9], IREN [S10], Nscale [S11].*

### CoreWeave: the biggest, and the most borrowed
It's the largest neocloud, and its numbers show both sides of that. Revenue more than doubled, and nearly all of its loss is the interest bill.

**The good case**
- The operating loss shrank to **$49M** from $144M the quarter before [S8]. Break-even is near.
- Signed business is about **8 times** its 2026 revenue forecast of $12.4–13.2B (our math), and the company says it added more than $25B in early Q3 [S8].
- It's less dependent on one customer. The top customer was 36% of Q2 revenue, versus 71% a year earlier [S8].
- It had about **$15.55B** of liquidity at June 30 [S8].

**The bad case**
- Interest cost **$640M** in the quarter, nearly the whole $626M loss. That's 24.9% of revenue (our math). Much of the debt carries effective rates of 9–15% (its convertible notes are about 2%), and about $6.2B went to debt payments in the first half [S8].
- Three customers are 72% of revenue, and two of them hold 64% of receivables [S8].
- Management guided Q3 net interest to $860–940M, up from $640M in Q2 (per coverage of its call) [S8].
- The $104B of signed business equals about 40 quarters of today's revenue (our math). It only turns into revenue if CoreWeave builds the sites and power on schedule.
- A reported plan by Meta to sell its own spare computing (section 4) hits one of its important customers.

### Nebius: the fastest growth, with a big bill coming
Nebius is the one making operating profit before depreciation, helped by customers paying part of their contracts up front.

**The good case**
- Operating profit before depreciation was positive at a **40.6%** margin [S9].
- Cash fell from **$9.30B** at March 31 to **$8.04B** at June 30, after about $5.7B of capital spending in Q2 [S9]. About 70% of new Q2 deals included prepayments covering an estimated 50–60% of the related building costs (per coverage of its report) [S9].
- It reports more than **$40B** of commitments from large customers [S9].

**The bad case**
- Planned 2026 spending is **$20–25B**, against $8.04B of cash [S9]. The gap has to come from prepayments, loans and new shares [S9].
- Interest expense was **$119.1M** in Q2, up from $4.8M a year earlier, mostly on its convertible notes [S9].
- To hit its $3.0–3.4B revenue forecast, revenue has to roughly double to about **$1.01–1.21B a quarter** in the second half, from $582M in Q2 (our math) [S9]. Most of its new capacity arrives in late 2026 and mainly pays off in 2027.
- Its shares fell 17% in a day on the Meta report [S13].

### IREN: a former Bitcoin miner turning into an AI cloud
IREN's old mining business is shrinking as the AI business grows, and the transition is expensive.

**The good case**
- AI cloud revenue passed mining revenue in the June quarter ($70.5M vs $66.7M) [S10].
- Its Microsoft contract is 20% prepaid, and financing plus prepayments fund 96% of the chip spending for that contract (a $3.6B investment-grade loan at 6.0%) [S10b].
- The company says recent three-year contracts bring in over $20M per megawatt of capacity, paying back in about two years. That's the company's own claim, not independently checked.

**The bad case**
- Only **$1B of the $4B** "contracted annual run-rate" is live today. The company itself warns that run-rate isn't the same as reported revenue, which "may be materially lower" [S10].
- Its FY27 spending plan is $25–30B against $14B secured, a gap of **$11–16B** (our math) [S10]. Management is targeting about $8B more, which would still leave it $3–8B short (our math).
- Part of its GPU debt is costly: financings of $2.8B fund 90% of the associated chip spending, and one facility carries a 9.0% fixed rate, against 6.0% on the Microsoft financing [S10b].
- The $639M write-off is non-cash, but it shows how costly the mining wind-down is. Operating profit before depreciation was only $19.2M in the June quarter [S10].

### Nscale: huge contracts, very little live
Nscale is the newest. It filed to go public on the NYSE on September 18, so its numbers come from its IPO filing (the S-1).

**The good case**
- Its two biggest customers are Microsoft (up to $43.8B) and Anthropic (up to $44.6B), about 85% of the contract value [S11].
- Nvidia is helping to fund it: $1B of the $3.1B loan round, plus a lease guarantee of about $860M [S11].
- Revenue is up 1,252%, albeit from a very small base [S11].

**The bad case**
- Only **$2.6B of $103.4B** in contract value (as of August 31) is live. That's 2.5% by our math. $56.4B of it is firm obligations over seven years [S11].
- The filing says management at first had "substantial doubt" the company could keep operating, because its funding plan relied on money not yet raised. It was eased by a plan to delay or cut spending if needed [S11].
- As of September 18 the S-1 says no firm financing had been obtained for the Anthropic agreements, and Anthropic can terminate a tranche without liability if delivery is late [S11].
- The filing warns that customers may have "relatively low switching costs" when contracts end [S11].

---

## 4. Who might not make it, even if AI keeps growing

Two questions often get mixed together here:
- **Demand risk:** what if AI spending slows or the bubble pops?
- **Structural risk:** what if a company can't get through *even though demand is fine*? Reasons include money that never arrives, a pile of debt coming due, one customer too many, or signed contracts that never turn into live revenue.

The four tests below look at structural risk. *What to notice: a company can look huge on paper and still fail the last row.*

| Test | CoreWeave | Nebius | IREN | Nscale |
|---|---|---|---|---|
| **Can it fund the build?** | Q2 spending $9.4B against about $15.55B of liquidity | $20–25B of spending against $8.04B of cash; prepayments cover part | Gap of $11–16B between plan and secured funding | The Anthropic build depends on financing not yet secured |
| **Debt due in the next 12 months** | $7.5B ($6.2B + $1.3B), against $15.55B liquidity: covered 2.1 times | Converts mature in 2029 or later; no near-term wall found | Not found in sources | Debt small at June 30 ($137M) but growing fast |
| **One customer too many?** | Top three = 72% | Not found in filings | Microsoft + one lab | 85% with two; 52% with one |
| **How much of the signed business is live?** | Backlog is about 40 quarters of revenue | $40B ÷ $3.0B run-rate ≈ 13 | $1B of $4B (25%) | $2.6B of $103.4B (2.5%) |

*All results are our math from filings [S8–S11]. Where a number wasn't in the sources, we say so.*

### Our reading
This is judgment, not a forecast. From most to least exposed to *structural* failure:

1. **Nscale.** It struggles on all four tests. It leans on money not yet raised, almost everything signed is not yet live, and two customers hold 85% of the contract value. It's also the only one with a going-concern warning in its filing.
2. **IREN.** A real funding gap and a mining business still being wound down. Prepayments and a giant-company customer soften it.
3. **CoreWeave.** The most debt of the four, but also the most scale, the best cover for what's due within a year, and a customer base that's spreading out. Its risks are refinancing, interest rates and delivering on time.
4. **Nebius.** The best on these tests: no near-term debt wall and strong prepayments. It depends on capital markets staying open and on a big step up in the second half.

**Not covered:** Lambda, Crusoe and other private neoclouds. We couldn't find primary sources for them, so they're left out rather than guessed at.

### Even with no bubble
- **A giant becomes a rival.** On July 1, a report that Meta plans to sell its own spare computing knocked CoreWeave down about 14% and Nebius about 17% in a day [S13]. It's a reported plan, not a launch. Meta's contracts with the two reportedly bar it from reselling their capacity.
- **The pie is finite.** Gartner forecasts neoclouds will take 20% of a $267B AI cloud market by 2030, about $53B (our math) [S12]. That's a forecast, and it has to be shared by every company in the group.
- **Our view:** heavy debt plus a few large customers is the classic setup for a shake-out. Not every signed dollar becomes revenue.

### If it is a bubble
The same four tests would likely decide the order: the company with the least live revenue and the most financing still to arrive would feel it first. Nvidia's exposure by company is Nscale ($1B of loans, about $860M of lease guarantees), CoreWeave ($2B stake plus capacity commitments), and, across all the AI clouds, the $36B of buy-back agreements [S2, S11].

---

## 5. What to keep an eye on

The neoclouds are Nvidia's fastest-growing customer group, and one of its biggest areas of financing exposure outside OpenAI. If one failed, Nvidia would take three hits at once: lost orders, a lower value on any stake it holds, and any guarantee or commitment tied to that company. This is the "double hit" our view says is the real tail risk.

| Watch this | Why it matters | Where to find it |
|---|---|---|
| Nvidia's guarantees (now up to $108.5B) | The only loan-like exposure | Each quarterly report |
| Gains and losses on Nvidia's stakes | Paper gains can reverse | Each quarterly report |
| Sales to customers outside the giants | A read on neocloud demand | Earnings call |
| CoreWeave's live power and how much backlog turns into revenue | Signed business only counts once delivered | Quarterly report and call |
| Nebius second-half revenue versus the $1B+ a quarter it needs | A direct test of its forecast | Quarterly report |
| IREN's live run-rate versus the $4B contracted | The live-revenue gap | Quarterly report |
| Nscale's IPO proceeds and the Anthropic financing | Decides whether the $103.4B can be delivered | IPO filing updates |
| Nvidia's gross margin in the fiscal Q4 (guided 71–72%) | Cost squeeze, or a sign of real price pressure | Nvidia earnings |

## How we got here

- **Sources.** Company filings (SEC), earnings materials and transcripts, Gartner for the market forecast, and named news coverage where a filing wasn't available. Every figure carries a source tag, and the tags are defined in the Sources table.
- **Labels.** Figures are reported by the company, derived by us (the arithmetic is shown and marked "by our math"), or our view (judgment, marked as such). Each source is marked primary (a filing or company document) or secondary (coverage of a filing).
- **Checks.** Nvidia's figures were read directly from its 10-Q, its CFO commentary and its Q4 call transcript. Nscale's revenue and customer concentration were checked against its S-1. CoreWeave's revenue, loss, interest, customer shares and debt were read from its 10-Q and results release. Nebius's revenue, adjusted EBITDA and interest expense were read from its 6-K, and IREN's figures from its results release and call. The OpenAI, CoreWeave and Anthropic investment amounts and IREN's 20% prepayment were confirmed in company announcements and SEC filings, and period labels (quarter or half-year) were re-checked against each source. Items that could not be checked against a primary document are marked secondary.
- **What was excluded.** Anything with no primary or named source was left out, including claims about customer-by-customer revenue shares, chip pricing and private companies we could not source (Lambda, Crusoe).
- **The structural tests.** The four tests in section 4 (funding gap, debt due within 12 months, customer concentration, how much of the signed business is live) were applied the same way to each company. The rankings are judgment applied to those test results, not a forecast of AI demand.
- **What would change the call.** A guarantee or equity gain that moves sharply in a future Nvidia quarterly report; Nscale's Anthropic financing being committed or failing; a neocloud's live revenue catching up to its signed business, or not.

## Caveats

- A few figures still come from coverage rather than the filings themselves: CoreWeave's liquidity and Q3 interest guide, Nebius's customer commitments and prepayments, some Nscale details quoting its S-1, the cloud giants' 2026 spending guidance (from news reports of their Q2 results), and Nvidia's per-gigawatt figures and fiscal 2028 comments (from call transcripts and coverage). They are marked secondary.
- The Meta plan to sell spare computing is a report, not a launch.
- The company rankings in section 4 are judgment, not fact.
- Nothing here is a recommendation to buy or sell anything.

## Sources

| ID | Source | Type | Used for | Status |
|---|---|---|---|---|
| S1 | Nvidia 8-K, Q4 FY26 results (25 Feb 2026) | Primary | FY26 revenue, Data Center, margin | Confirmed |
| S2 | Nvidia 10-Q, quarter to 26 Jul 2026 (SEC) | Primary | Stakes, commitments, guarantees, cash flow, receivables, customer concentration, H1 revenue and net income | Confirmed, read directly |
| S2b | Nvidia 10-Q, quarter to 26 Oct 2025 | Primary | Intel $5B commitment | Confirmed |
| S3 | Nvidia CFO commentary, Q2 FY27 (SEC) and Q2 FY27 earnings call | Primary | Customer mix, commitments, guarantee terms, margin guide, outlook, non-GAAP reconciliation; per-gigawatt figures from the call | Commentary confirmed; per-gigawatt and FY28 guide from call transcripts and summaries |
| S4 | Nvidia Q4 FY26 earnings call, corrected transcript (25 Feb 2026) | Primary | Networking over $31B for the year and $11B in Q4; Grace Blackwell about two-thirds of Data Center | Confirmed in the official transcript |
| S6 | OpenAI's announcement (27 Feb 2026) as reported by CNBC; CoreWeave 8-K (23 Jan 2026); CNBC (9 May 2026) | Primary + secondary | OpenAI $30B in a $110B round at $730B pre-money; CoreWeave $2B at $87.20 a share; Huang comments | Amounts confirmed in OpenAI's announcement and CoreWeave's 8-K; Huang comments per CNBC |
| S8 | CoreWeave 10-Q, 30 Jun 2026 and Q2 2026 results release (SEC); The Register, Beancount, sec-api, Stocktitan | Primary + secondary | Revenue, net loss, net interest, operating loss, customer shares, receivables, debt table (primary); liquidity and Q3 interest guide (coverage) | Core figures confirmed; liquidity and Q3 guide per coverage |
| S9 | Nebius 6-Ks, Q1 and Q2 2026 (SEC); Q2 call transcript; Storagenewsletter, Rivkin, Energy Mag | Primary + secondary | Revenue, adjusted EBITDA, adjusted net loss, interest expense, convert issuance, March cash (6-K); capex plan and guidance (call); commitments and prepayments (coverage) | Core figures confirmed; commitments and prepayments per coverage |
| S10 | IREN 8-K, FY26 results (SEC) | Primary | FY26 financials, run-rate, write-offs | Confirmed |
| S10b | IREN FY26 results release and Q4 FY26 call; IREN 8-K (3 Nov 2025) | Primary | Microsoft $9.7B over five years with 20% prepaid (8-K), 96% financed, per-megawatt pricing (company claim), $14B secured, $25-30B plan | Confirmed in company documents |
| S11 | Nscale S-1 (SEC, 18 Sep 2026) and coverage (Fortune, CNBC, Investing.com, Actuia, Mostly Metrics) | Primary + secondary | Revenue and 52% largest customer (S-1 text); going-concern wording (verbatim per Fortune); contract values, Anthropic terms (coverage quoting the S-1) | Core figures confirmed; remaining details per coverage |
| S12 | Gartner press release (30 Jun 2026) | Primary | 20% of $267B by 2030 | Confirmed |
| S13 | Bloomberg report (1 Jul 2026) via Motley Fool, Digg | Secondary | Meta's plan and stock moves | A reported plan, not a confirmed launch |
| S14 | News reports of Alphabet, Meta, Microsoft and Amazon Q2 2026 earnings (Statista, Sherwood News, Motley Fool, Yahoo) | Secondary | 2026 spending guidance by company | Consistent across outlets; Amazon's July raise not itemized, so the text says 'at least' |
| S15 | Microsoft, Nvidia and Anthropic announcement (18 Nov 2025); W.Media and AI Funding Tracker (Google/Broadcom TPU deal) | Primary + secondary | Nvidia up to $10B, Microsoft up to $5B, Anthropic $30B Azure commitment (announcement); TPU deal | Investment amounts confirmed in the announcement; TPU deal per coverage |

## Known gaps (to close in the next update)
1. CoreWeave's liquidity and Q3 interest guide, and Nebius's customer commitments and prepayments, are sourced from coverage of the filings.
2. Some Nscale S-1 details (Anthropic termination terms, the Nvidia convertible note and lease guarantee) are sourced from coverage quoting the S-1.
3. The four cloud giants' 2026 spending guidance comes from news reports of their Q2 results, so the text states a floor ("at least").
4. Nvidia's per-gigawatt figures for Hopper and Blackwell, its fiscal 2028 growth and margin comments, and the fiscal Q4 margin guide come from earnings-call transcripts and coverage, not the filings.

## Version and how to cite

- **1.0, 2026-10-15:** first publication.
- Cite as: Awori, C. (2026). *Is Nvidia paying for its own demand? What the filings show about Nvidia, circular financing and the neoclouds.* TLI Research, v1.0.
