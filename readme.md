# Aaditya Singh

**Product & business analytics · Bengaluru, India**
Open to work · Bengaluru +4 · hybrid / remote

## Engineering systems that don't just scale, they *sustain.*

MBA in Marketing & Business Analytics and B.Tech in ECE, both from BIT Mesra. I've **rewritten a scheduler in Go for Google Summer of Code**, commissioned a **$600M hot strip mill**, and now run onboarding, CRM and certification products at **ClassView.ai**.

[Get CV](/resume.pdf) · [Contact me](#contact) · [See case studies](#case-studies) · [LinkedIn](https://www.linkedin.com/in/aadi-singh/) · [PixelPages newsletter](#writing-and-education)

**Now:** building a 6-tier teacher certification product proposed with IIT Bombay, and writing PixelPages, the morning paper for people who build.

**Worked with:** ClassView.ai · Corizo · SAIL (RDCIS) · Google Summer of Code · FOSSASIA · Jindal Steel & Power · MECON · Openforce · Walkover

---

## Impact

Five numbers from the last three years:

| Number | What it means | Where |
|---|---|---|
| **55%** | Lower per-classroom setup cost through in-house installation | ClassView.ai |
| **18,726** | Lessons across 49 schools analysed to set a certification rule | ClassView.ai |
| **2,000+** | Leads from pan-India outbound, converting at 1.46% lead-to-paid | Corizo |
| **5,000+** | Lines of legacy C migrated to Go across 4 scheduler modules | GSoC · FOSSology |
| **100+** | Open-source contributors mentored | GSoC · Openforce |

---

## Experience

### Operations Manager · Innovartan (ClassView.ai)
*Oct 2026 – Present · Noida, on-site*

Scoped a 6-tier teacher certification product for IIT Bombay co-branding and redesigned school onboarding into a 22-day, 5-stage SOP. Introduced Adoption and Impact Reports, and built a webhook-fed CRM dashboard that sends teacher-reported issues straight to the product team.

`55% lower setup cost` `18,726 lessons analysed` `155 teachers · 15 schools`

### Marketing Executive · Corizo Edutech
*May – Sep 2026 · Bengaluru, on-site*

Owned pan-India student acquisition from first contact to paid enrolment, running 2,600+ personalised emails and 80 calls a day. Tracked where leads dropped off across 4 channels and focused effort on the segments most likely to buy.

`2,000+ leads` `1.46% lead-to-paid` `₹2L revenue · ₹100 per lead`

### Vocational Trainee, Finance & Accounts · Steel Authority of India (RDCIS)
*Jun – Jul 2025 · Ranchi, on-site*

Audited 5 accounting-system modules and compared SAIL with Tata Steel and JSW Steel on 14 financial ratios (FY20–FY25). Drafted FinStream, a modular ERP blueprint with 4-tier role-based access and bank-API payments.

`8 integration gaps found` `8 KPIs · 8-month plan` `₹5.11L/yr backup model`

### Contributor, Scheduler Overhaul · Google Summer of Code (FOSSology)
*May – Sep 2024 · Remote*

Moved FOSSology's legacy C scheduler to Go and designed a multilevel feedback queue with PID-controlled rate limiting for 4 scheduling use cases. Shipped a one-step Bash CI/CD setup so new contributors could get started faster.

`5,000+ lines migrated` `4 core modules` `100+ contributors mentored`

### Contributor · FOSSASIA (Open Event Server)
*Jan – Mar 2024 · Remote*

Built the Badge Generation and Mailing List models and the full Exhibitor Management module in Python/Django, with REST endpoints and pytest unit and integration tests.

`Django` `REST APIs` `pytest`

### Graduate Engineering Trainee, Electrical & Automation · Jindal Steel & Power
*Jul 2023 – Jan 2024 · Angul, on-site*

Commissioned electrical systems for a 5 MTPA hot strip mill alongside TMEIC, Siemens and CISDI. Managed HMI network nodes and built Tableau and Power BI dashboards on sales and order data.

`$600M mill` `3 OEM partners` `5 MTPA capacity`

### Earlier

- **MECON · Vocational Trainee, IT Services** (May – Jun 2022, Ranchi): built a Java/Swing/JDBC asset management app covering 1,000+ assets that cut manual tracking by 20%, and tuned an Oracle server within a 1 GB limit.
- **Openforce · Mentee, Open Source Development** (Mar 2022, remote): found issue-tracking bottlenecks across open-source repositories and standardised contributor documentation.
- **Walkover · Trainee, Web Development** (Dec 2021 – Mar 2022, remote): co-built Build Docs in a 4-person team on Node.js and Firebase, deployed on Heroku.

---

## Case studies

### Osam: finding the *one* failing process in a year of plant data
*Featured · Jan – May 2026 · Plant analytics · with Rahul, Anurag and 3 others*
**Stack:** R, Excel, K-Means, LDA, XGBoost

**The problem.** For Osam Supply Chain Logistics, I analysed a year of sensor data across 10 control parameters. Only one process was out of spec: pasteurisation holding time (Cpk −0.609), which failed FSSAI requirements on 95.1% of operating days.

**What the data showed.** Seasonality drove both yield loss and energy use. Summer cost 5.74 Wh/L against 4.31 Wh/L in other seasons, a 33% penalty. One-way ANOVA (F = 562.3, p < 10⁻¹²) and Pearson correlation (r = −0.947) across three seasonal regimes confirmed the link.

**What I built.** A predictive buffer system that sets the flow rate at the start of each shift so holding time stays compliant:

- K-Means clustering (k = 3) to group volume patterns
- An LDA classifier to identify the operating regime (95.9% test accuracy)
- An XGBoost forecaster (11.9% MAPE)

**Why it matters.** The plant can set the right flow rate before a batch starts, instead of finding out afterwards that it went off-spec.

| Key result | Value |
|---|---|
| Cpk of holding time | −0.609 |
| LDA regime accuracy | 95.9% |
| XGBoost forecast error (MAPE) | 11.9% |

### Triply
*Nov 2024 – Present · Product strategy · with Shreya*
**Stack:** Go, PostgreSQL, Redis, 3 government APIs · **Headline number:** ₹2L Cr+ ride-hailing market, 24+ fragmented providers

**The problem.** India's ride-hailing market (about ₹2,00,250 Cr) is split across 24+ regional providers and has a gap in trust and compliance. I explored what a compliance-first aggregator could look like.

**Market and users.** I compared 4 user personas against Uber, Ola, CabBazaar and Choose.app to find where existing apps fall short, then positioned Triply around verified, compliant drivers and vehicles.

**Product and compliance layer.** Driver and vehicle KYC runs on 3 government APIs:

- **VAHAN** for vehicle records
- **Sarathi** for driving licences
- **DigiLocker** for identity documents

The flow is designed to meet the Motor Vehicle Aggregator Guidelines, the IT Act 2000 and the DPDP Act 2023.

**Measuring success.** 10+ KPIs under Google's HEART framework, with safety thresholds that automatically trigger a release rollback.

### Medens
*Jan 2023 – Present · Healthcare PRD · team of 5*
**Stack:** Flutter, Firebase, ABDM/ABHA, HEART · **Headline number:** 64 vs 150 doctors per 100,000 (India vs global average)

**The problem.** India has about 64 doctors per 100,000 people, against a global average of about 150, and patient records, diagnostics and outbreak data live in separate systems. I explored one AI-assisted platform for hospitals, labs and health departments.

**Market and users.** I sized India's digital health market at about ₹1,31,750 Cr (2024) and mapped 5 stakeholder groups: providers, patients, diagnostic labs, government health bodies, and pharma and insurers. I benchmarked 4 AI diagnostics players (Qure.ai, Niramai, SigTuple, DeepTek) and 4 telemedicine platforms (Practo, Tata 1mg, MediBuddy, Apollo 24/7), and positioned Medens as one platform rather than a point solution.

**Product requirements.** The PRD rests on four pillars:

- AI-assisted diagnostics
- Real-time health analytics
- Patient health management linked to ABHA IDs
- Pandemic response dashboards

Four user stories (a rural doctor, a chronic-care patient, a state health department and a lab chain) drive the requirements. The design supports ABDM and NDHM integration and follows the DPDP Act 2023 and CDSCO guidance for software as a medical device.

**Measuring success.** HEART metrics with separate baselines and targets, plus rollback criteria for false-negative rate, diagnostic accuracy, data security and alert response time.

### Smaller builds

- **EcoMap** (2022) · HTML5, CSS3, JavaScript, D3.js: an interactive map of CO₂ emissions across 195+ countries, with year filters and total vs per-capita views.
- **Build Docs** (2021–22, with Aryan and Aditi) · Node.js, Firebase, Heroku: a central document platform built at Walkover so scattered work documents were easier to find, share and secure. I built the credential management on Node.js and Firebase, replaced the Passport.js approach with a cloud-based design after it kept causing errors, and deployed it on Heroku using Nodemon for fast iteration.

---

## Skills

| Area | Skills |
|---|---|
| **Product & project** | Roadmapping, PRDs, User research, Market sizing, Competitive analysis, HEART metrics, Prioritisation, SOP design, Agile/Scrum, Jira, Figma |
| **Data & analytics** | SQL, Python (Pandas, NumPy, scikit-learn), R (tidyverse, ggplot2), Excel (VBA, pivot tables), Power BI, Tableau, ANOVA, Regression, Process capability (Cpk) |
| **Growth & business** | Funnel analysis, Segmentation, Cold outreach, Email marketing, Financial analysis, Supply chain analytics |
| **Engineering** | Go, Java, Python/Django, JavaScript, Flutter, PostgreSQL, MongoDB, Redis, Firebase, AWS, Docker, Git, CI/CD, Bash |

### Credentials

| Credential | Detail |
|---|---|
| DevOps on AWS | Specialisation, Amazon Web Services |
| Become a Product Manager | Discovery, roadmaps, GTM · 13 hours |
| Deep Learning A–Z | CNNs, RNNs and deep learning architectures |
| Figma for Developers | Auto layout, components, handoff |
| Excel, beginner to advanced | Pivot tables, VBA, dashboards |
| HackerRank | SQL 4★ · 10 Days of JS gold badge |

---

## Writing and education

### PixelPages
The morning paper for everyone who builds, writes and thinks: notes on Industry 4.0, compliance systems and data infrastructure.

**1,444** impressions on the launch post · **1,287** followers on LinkedIn · [Subscribe on LinkedIn](https://www.linkedin.com/in/aadi-singh/)

### Education

- **MBA, Marketing & Business Analytics**, Birla Institute of Technology, Mesra (2024–2026)
- **B.Tech, Electronics & Communication**, Birla Institute of Technology, Mesra (2019–2023)

### Mentoring and social impact

Mentored 100+ developers through GSoC, Openforce and CodeFlow. Recognised for UNICEF Child Voices programmes and Pollution Control Board environmental campaigns.

---

## Contact

### Thanks for *visiting.*

Got questions, comments or feedback? Feel free to reach out.

- **Email:** aadityasingh29.01@gmail.com
- **LinkedIn:** [linkedin.com/in/aadi-singh](https://www.linkedin.com/in/aadi-singh/)
- **Web:** [aadityasingh.org](https://aadityasingh.org)