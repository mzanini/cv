# Marco Zanini - Staff/Principal Platform & API Engineer
[github.com/mzanini](https://github.com/mzanini/) • [linkedin.com/in/marco-zanini](https://www.linkedin.com/in/marco-zanini) • marco.zanini@hey.com

> I’ve led and shipped company-wide initiatives with lasting impact on performance, cost efficiency, and product differentiation. At Ravenna, I own the knowledge ingestion pipeline behind its agentic service desk, built its device management integrations, and delivered several performance optimizations, such as removing ALB sticky sessions and cross-pod Redis rate limiting. Before that, I architected and led Clari’s Heroku→AWS migration, shipped Groove’s first public API, and owned its Salesforce managed package. <br>

_Based in the Greater Seattle Area_ <br>

## 🤓 Work Experience

### @ [**Ravenna**](https://ravenna.ai/) _in Seattle, WA_ <br>

> TypeScript, Node.js, tRPC, Prisma, PostgreSQL (Aurora), Temporal, Redis, OpenSearch, React, AWS (ECS, CloudFront), Terraform, OpenTelemetry, Grafana

**Staff Software Engineer - Platform Team** _(Nov 2025 - Present)_ <br>
Building the integrations, knowledge and infrastructure platform behind an AI-native service desk for IT and HR teams.
- Own [knowledge base ingestion](https://docs.ravenna.ai/documentation/automate/knowledge/overview) that grounds Ravenna's AI agents: ~1M documents for 120+ customer organizations, ~12k syncs/month at 96% success. Unified ingestion behind a provider-independent document model, making new sources quicker to add and existing ones easier to maintain. Added Zendesk, Guru, GitHub, among others.
- Optimized ingestion performance and cost: eliminated the top 3 Aurora wait-time queries (~100 → 2-3 queries per batch), cut pages dropped to third-party rate limits from ~43k a night to ~0 by pacing calls across pods with a distributed Redis rate limiter, and reduced Grafana Cloud metrics spend.
- Leading security hardening for Google's CASA assessment: moved authorization to the API boundary with org scoping enforced by the type system, closed cross-org access gaps, kept credentials out of URLs and logs, and put core's origin behind a private CloudFront VPC origin.
- Shipped 4 device management integrations end to end ([Fleet](https://docs.ravenna.ai/integrations/fleet/overview), [Jamf Pro](https://docs.ravenna.ai/integrations/jamf/overview), [Iru](https://docs.ravenna.ai/integrations/iru/overview), [Intune](https://docs.ravenna.ai/integrations/intune/overview)), among Ravenna's first AI agent tools, from device lock and wipe to disk encryption keys; designed the [contextual ticket cards](https://docs.ravenna.ai/documentation/tickets/cards) that show requesters' devices and assets in tickets.
- Rebalanced production traffic by removing ALB sticky sessions, which pinned every open browser tab to one pod: in business hours, the busiest pod went from ~1.6× to ~1.0× the fleet's average load, with peaks down from 3.2× to 2×.

### @ [**Clari**](https://www.clari.com/) _in Seattle, WA (remote)_ <br>

> Ruby on Rails, TypeScript, GraphQL, PostgreSQL,  React, AWS, Kubernetes, Docker, Heroku, JSON:API

**Staff Software Engineer - Architecture Team** _(Aug 2023 - Oct 2025)_ <br>
Driving technical projects across the company: focusing on architecture, performance, and cost optimization.
- Architected and led the migration of all 8 services from Heroku to AWS EKS (Kubernetes), consolidating onto one platform for a projected 40% infrastructure cost saving.
- Led a zero-downtime migration of asynchronous job processing from Heroku to AWS EKS, sustained 175M jobs/week and cutting infrastructure costs by ~$500K annually.
- Migrated Heroku Key-Value store to AWS ElastiCache (4 instances); 130k requests/minute, p90<10ms; all while cutting costs >50%.
- Shipped first version of partner API and API strategy for Clari's Groove, enabling third-party integrations. Using JSON:API, OAuth 2.0: 5+ integrations live ([ZoomInfo](https://pipeline.zoominfo.com/sales/clari-groove-integration), [LeanData](https://leandatahelp.zendesk.com/hc/en-us/articles/31981353374619-LeanData-Clari-Groove-Integration-Add-to-Flows), [Nooks](https://www.nooks.ai/blog-posts/less-clicking-more-calling-groove-now-works-inside-nooks)); ~3k requests/day across core partner flows.
- Re-architected Groove’s Dialer to a Postgres-backed event pipeline; handles ~30k calls/hour and cut dropped calls ~75%.

### @ [**Groove (acquired by Clari)**](https://www.groove.co/) _in Seattle, WA_ <br>

> Ruby on Rails, GraphQL, PostgreSQL, JavaScript/TypeScript, Next.js, React, Salesforce Apex, Heroku, AWS

**Full-stack SWE → Sr SWE → Eng Lead → Eng Manager → Software Architect** _(Jun 2018 - Aug 2023)_ <br>
Lead company-wide projects to add new features, improve code modularity, performance and reliability.

- Upgraded Rails 4.2→5.2→6.1; introduced private gems, ActionCable, Redis cache, encrypted credentials; began monolith decomposition with packwerk.
- Rolled out read-replica DB; offloaded 10% of reads, stabilizing peak traffic and improving P95 latency for heavy reports.
- Managed 5 engineers to launch [Groove's Conversation Intelligence](https://www.groove.co/blog/groove-announces-new-conversation-intelligence-product-and-mobile-app); 66k+ calls processed of which 80% mapped to Salesforce objects.
- Rebuilt meeting scheduler (Next.js + Rails); improved UX, reduced latency with server-side rendering.
- Shipped [Automatic Logging To Custom Objects](https://www.groove.co/blog/groove-releases-new-features-for-complex-enterprise-workflows/), allowing Groove to serve customers in non-tech verticals.
- Shipped [Auto Contact Capture](https://www.groove.co/blog/groove-expands-revenue-intelligence-capabilities-with-auto-contact-capture/), increasing number of automatically captured contacts by 20% in early tests.
- Migrated Salesforce Managed Package to [SFDX](https://developer.salesforce.com/developer-centers/developer-experience); enabled parallel feature work and CI/CD, growing contributors from 1 to 8 and increasing release frequency five-fold.

### @ [**Meteorcomm**](https://meteorcomm.com/) _in Seattle, WA_<br>

> C++, Ruby, AMQP, Apache Qpid, Docker, Kubernetes, OpenShift, Red Hat Enterprise Linux, Ansible

**Software Engineer II / Team Lead** _(Jan 2017 - May 2018)_ <br>
- Redesigned a legacy messaging application toward a containerized architecture (Docker/Kubernetes/OpenShift), reducing rollout risk and simplifying ops.
- Implemented C++ services for [PTC](https://railroads.dot.gov/train-control/ptc/positive-train-control-ptc) and Ruby simulators used in UAT, enabling decoupled testing and faster feedback cycles.
- Evangelized reliability tooling (Google Sanitizers) and estimation practices adopted by 5 engineering teams.

### @ [**Schlumberger**](https://www.slb.com/) _in Paris, France_ <br>

> C++, C#, WPF, TDD

**Software Engineer** _(Feb 2013 - Jun 2016)_ <br>
- Implemented C++ services and UI workflows for data acquisition/processing.
- Converted MATLAB library to C++ (Armadillo), 2× faster and no license dependency.
- Drove engineering practices as Scrum Master (TDD/pairing), increased test coverage ~50%; shipped monitoring POC projecting ~$5k/job savings.

### @ [**The Irish Software Engineering Research Center (LERO)**](https://www.lero.ie/) _in Limerick, Ireland_ <br>

> Java

**Researcher (Cloud Security)** _(October 2011 – March 2012)_ <br>
Researched dynamic cloud security and built context-aware countermeasures in collaboration with IBM Dublin

## 🚀 Entrepreneurship

### @ [**Zero Mile Labs**](https://www.zeromilelabs.com) _in Issaquah, WA_ **(Side Project)**<br>

> React Native, Ruby on Rails, GraphQL

**Owner** _(Jan 2021 - Present)_ <br>
I founded Zero Mile Labs with one goal: shorten the distance between people and their food. With that goal, I built [CropStand](https://www.zeromilelabs.com/cropstand), a mobile app that allows small food producers to get their roadside produce stand online in minutes. Producers list the produce they have available and accept payments entirely in the app.

Logo and app design, wireframing, development and deployment all done by yours truly. The app is available on both iOS and Android.

## 🔬 Education

### @ [**Polytechnic University of Milan**](https://www.polimi.it/en/) _in Milan, Italy_

**Master of Science**, Computer Engineering _(2010 - 2012)_

**Bachelor of Science**, Computer Engineering _(2006 - 2010)_

## 💬 Languages

**Italian**: Native <br>
**English**: Bilingual <br>
**French**: Full Professional Proficiency <br>
