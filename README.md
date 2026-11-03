# Hi, I'm Sowad

I run [Kitalon Labs](https://kitalonlabs.com/), a small product studio in Dhaka. I spent twelve years building software, classrooms, and hardware prototypes before LLMs were any good at writing code. Then they got good, and I shipped 17 products in about 18 months, all of them solo, across SaaS, open source, browser extensions, and Android. Claude Code is my main build tool.

Alongside Kitalon Labs, I serve as interim CEO of [Uddom](https://uddom.io/) and advise [LEAD Academy](https://lead.academy/) on AI and partnerships. Before moving back to Dhaka in 2016, I spent eight years in Canada and the US studying, setting up enterprise engineering labs for universities, and launching early startups in Toronto.

---

## What I'm building now

**[GovProcurementAI](https://govprocurementai.com/)** gets most of my attention. It acts as a managed proposal team for small federal contractors and state and local bidders. A client forwards an RFP, gets a first draft back within 24 hours, and then goes through a clause-level FAR/DFARS compliance pass with a human signing off at every step. We work on a retainer plus a share of contracts won. In most small firms, the founder still does this work by hand at midnight. That is the gap we are closing.

A few others I am actively shipping:

- **[JobSim](https://jobsim.works/)**: Replaces the standard job interview with a simulated workday in the browser. Candidates step into a role-specific scenario (sales development, customer success, HR, support, sales management, or a custom build), field messages from AI teammates, and work through real tasks on a clock. Every score ties directly to something the candidate actually did. I am part of the team building it.
- **[Restaurant Phone AI](https://restaurantphoneai.com/)**: A voice agent that answers restaurant phones and takes orders around the clock, wired straight into the POS.
- **[Covena](https://covena.xyz/)**: Tracks EU e-commerce regulations (DSA, GPSR, and related mandates) so cross-border sellers do not get caught off guard.
- **[ReconcileAI](http://174.138.45.139:8080/)**: Automated bank reconciliation built on Plaid, currently in testing with design partners while I figure out where it earns its keep.

## Open source

I build most of these because I hit a wall and wanted the tool to exist.

**[pgmoat](https://kitalonlabs.com/pgmoat)** ([npm](https://www.npmjs.com/package/pgmoat) · [source](https://github.com/kitalonlabs/pgmoat)) is governed Postgres access for AI agents. It lets Claude and other MCP clients query a database with read-only access enforced in layers, sensitive columns hidden by default, rows scoped to the right tenant, and every query recorded in a verifiable audit log. In 2025, [Datadog Security Labs showed](https://securitylabs.datadoghq.com/articles/mcp-vulnerability-case-study-SQL-injection-in-the-postgresql-mcp-server/) that the reference Postgres MCP server could be talked out of its read-only transaction with a simple `COMMIT;`. pgmoat parses every query with the real Postgres parser, checks it against an allow-list, and only then runs it inside a read-only transaction. It is MIT licensed and ships with 315 public safety test cases anyone can add to.

**[NeoGold](https://github.com/Kitalon-Labs-LLC/neogold)** estimates newborn jaundice risk from a smartphone photo of a baby's chest placed next to a signed color-calibration card. The Android app (Kotlin, Jetpack Compose) runs inference completely offline so it works in clinics without reliable internet, and v1.0 is currently in Google Play closed testing for a partner's validation study. Alongside the app, the repo includes the card-signing tool, a Python model-training pipeline, and a FastAPI and PostgreSQL 16 backend (Docker Compose, Caddy) that only accepts consented research uploads. Code is MIT licensed; the calibration card design and docs are CC BY 4.0.

- **[Aether](https://github.com/sowadalmughni/aether-lang)**: A type-safe language for orchestrating LLMs with DAG-based execution. Built in Rust with Axum and Tokio.
- **[NFTicket Protocol](https://github.com/sowadalmughni/nfticket-protocol)**: On-chain event ticketing designed to make scalping unprofitable. TypeScript, Solidity, Hardhat.
- **[RWA-Studio](https://github.com/sowadalmughni/rwa-studio)**: Tokenize a real-world asset in about five clicks. Solidity, OpenZeppelin.
- **[zkIPFS-Proof](https://github.com/sowadalmughni/zkipfs-proof)**: Zero-knowledge proofs for verifying private IPFS data without exposing the underlying file. Rust on the Risc0 zkVM.

## Browser extensions & mobile

Small tools that live inside someone else's daily workflow:

- **[QuoteSweep](https://chromewebstore.google.com/detail/quotesweep/lpmdpoalmclpfagkmkdijhkklcolnmcf)**: Pre-fills five commercial P&C insurance portals from a single risk profile. WXT, React 19, Cloudflare Workers, Neon.
- **[POA Architect](https://chromewebstore.google.com/detail/poa-architect/kmjbpdmhihmpjdekkngeebmginokofdn)**: Walks suspended Amazon sellers step by step through reinstatement appeals.
- **[OneReply](https://chromewebstore.google.com/detail/onereply-%E2%80%94-ai-email-repli/noiajpemkfbhgghgpfafomdiahlmlkci)**: Drafts context-aware email replies right inside Gmail.
- **[JobSafe](https://chromewebstore.google.com/detail/jobsafe/kefmohdijppkijhddolldplkdpcoidkc)**: Flags ghost listings and job scams on LinkedIn, Indeed, and Glassdoor.
- **Android**: Beyond NeoGold above, three utility apps on Google Play written in Kotlin with Jetpack Compose, Hilt, and Room. I built the first one, a unit converter, as a warmup to get my hands dirty with modern Kotlin again, then followed it up with a subscription tracker and an on-device document scanner (and killed a fourth, a photo editor, before launch when it did not clear the bar).

## Tools I reach for

Python, TypeScript, Rust, Kotlin, Solidity, C#, and SQL. FastAPI and NestJS on the backend; Next.js 15 and React 19 up front. Postgres (usually Neon with Drizzle), alongside Redis and SQLite. For AI workloads, I use LangChain and the major model APIs (Anthropic, OpenAI, Gemini), plus MediaPipe, TFLite, and ONNX when inference needs to happen on the device.

## Beyond Kitalon

- **Interim CEO at [Uddom](https://uddom.io/)** (since May 2025): Uddom is a crowdfunding platform for Bangladesh built on [Oak Network](https://oaknetwork.org/), which is backed by Kickstarter and a16z crypto.
- **AI & Technology Consultant at [LEAD Academy](https://lead.academy/)**: Leading fundraising, institutional partnerships, and AI integration for an education platform running live coding classes for kids across Bangladesh.
- **[Voice2Policy](https://voice2policy.ai/)** (2024 to 2025): A paid engagement building civic-tech AI for federal policy analysis. I fine-tuned deBERTa-v2 on AWS SageMaker, shipped the platform on NestJS and Next.js, and authored the policy whitepaper [*AI for Public Good: A Strategic Framework for National Progress in Bangladesh*](https://voice2policy.ai/pdf/AI%20for%20Public%20Good%20Whitepaper-compressed.pdf) on AI adoption across government ministries in Bangladesh.

## How I got here

I moved to Canada in September 2008 to study at the [University of Windsor](https://www.uwindsor.ca/). I spent eight years in North America (including a year in the US), working at [ENGINEERING.com](https://www.engineering.com/) on the [Dassault Systèmes](https://www.3ds.com/) stack (CATIA, DELMIA, and ENOVIA) to set up engineering and PLM labs for universities, and later at Ennovor Tech before trying my hand at startups in Toronto. In January 2016 I moved back to Dhaka and have been building here since.

A few milestones from the pre-AI years I am still proud of:

- **Product Owner & Account Manager at [IMpulse](https://www.impulsebdltd.com/)** (2017 to 2024): Ran the [Pulselinks](https://www.pulselinks.com/) account, a cloud event-management platform built on IMpulse's ERP engine. I led a cross-border team of up to 29 across Switzerland and Bangladesh, cut client deployment time by 60 days, and grew outbound sales by 330%.
- **Technical Director at [Venturas](https://www.venturas-bd.com/)**: Led product and engineering at this [Reapra](https://jp.reapra.com/)-backed EdTech company in Dhaka, where I built and launched two flagship learning platforms:
  - **[PODOKKHEP](https://apkpure.com/podokkhep-homework/podokkhep.bd.homework)**: Bangladesh's first custom digital coaching school for SSC students, which lifted student comprehension scores by roughly 25%.
  - **[JANO KI](https://apkpure.com/janoki/venturas_bd.ianki)**: A flashcard study app for SSC and HSC students that reached 10,000+ students across 70 institutions. [Dhaka Tribune covered the launch](https://www.dhakatribune.com/feature/tech/124031/jano-ki-app-makes-education-simpler-than-ever) after it crossed 5,000 downloads in its first 30 days and broke into App Annie's top 100 education apps in Bangladesh.
- **Co-founded Enlightli**: Took first prize ($8,000) at Toronto's inaugural `#HackTO` hardware hackathon in March 2015 with a cycling helmet whose LEDs ran on body heat. [BetaKit covered the weekend](https://betakit.com/blow-stuff-up-hackto-and-torontos-exploding-maker-movement/).
- **Co-founded Commutero**: An early take on peer-to-peer ridesharing in Toronto that matched local professionals into carpools through LinkedIn during the 2015 Pan Am Games traffic crunch. We shipped it more than a year before Pathao or Uber launched ridesharing in Bangladesh (late 2016), two years before Lyft entered Canada (late 2017), and before UberPool even had a permanent rollout in Toronto. [Vice wrote about it](https://www.vice.com/en/article/hell-is-carpooling-with-local-professionals-from-linkedin/) in July 2015, not kindly.
- **Chapter President, [Engineers Without Borders Canada](https://www.ewb.ca/) (Windsor)**: Led the university chapter and raised more than $100,000 during my term to back development and charity transparency initiatives. [CBC Windsor covered our campaign](https://www.cbc.ca/news/canada/windsor/windsor-engineers-want-more-transparent-charities-1.1023574).
- **[AIPMM](https://aipmm.com/) Certified Product Manager** (2017).

## Giving something back

Technology means very little if it never reaches the people who need a break the most.

In Cox's Bazar, I teach Scratch and Python to Rohingya refugee children through a partnership between [LEAD Academy](https://lead.academy/) and [Charity Right Bangladesh](https://www.charityright.org.uk/campaigns/coding-skills-support-for-underprivileged-students-1/). Across two week-long visits so far, we have run 30 classroom sessions across three student groups. That same drive is why I spend time scaling NGO campaigns at [Uddom](https://uddom.io/), and why I got my start pushing for charity accountability with Engineers Without Borders in Windsor, ON Canada.

## Outside the code

Away from the keyboard, I race homing pigeons in Dhaka and hold membership `#793` at the [Bangladesh Racing Pigeons Entrepreneur Limited (B.R.P.E.L)](https://brpel.com/verified-members-p3/), flying out of a loft I registered as [Rebel Flyers](https://www.facebook.com/REBELFlyers). I also ride mountain bikes and train regularly. My quieter obsession is collecting perfumes, and I care about fashion a fair bit more than a software engineer probably should.

## Find me

- **Web**: [kitalonlabs.com](https://kitalonlabs.com/)
- **LinkedIn**: [linkedin.com/in/sowadalmughni](https://linkedin.com/in/sowadalmughni)
- **Email**: [sowad@kitalonlabs.com](mailto:sowad@kitalonlabs.com)

---

> "I do not wait for the right tools. I build them."
