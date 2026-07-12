# Institutional Tools Landscape — Defense, Think Tanks & NGOs

**Scope:** Public market research — existing tools, pricing, and identified gaps in the institutional AI tooling space  
**Date:** July 2026  
**Focus:** European / SE European (Greek) market  
**Methodology:** Public sources only — vendor websites, government publications, academic papers, industry reports  

---

## Executive Summary

Across defense, think tank, and NGO verticals, institutional tooling is **fragmented, expensive, largely cloud-dependent, and only beginning to integrate LLM capabilities.** The gaps share a common pattern:

- **Defense:** Wargaming simulators lack LLM integration; classified environments prevent use of cloud AI; ethical frameworks are manual checklists
- **Think Tanks:** Policy research tools are narrow SaaS products with no adversarial reasoning or scenario modeling
- **NGOs:** Grant management tools automate workflows but offer no AI-driven impact measurement, scenario modeling, or GDPR-compliant analysis

**The European market amplifies these gaps:** GDPR, NATO security requirements, and the EU's push for digital sovereignty (European Defence Fund, EuroHPC, Pharos) create demand for European sovereign AI platforms that US-centric vendors cannot fill.

---

## 1. Defense / Military Institutions

### 1.1 Scenario Modeling & Wargaming

| Tool | Type | Pricing | Key Features | LLM Integration? |
|------|------|---------|-------------|:-:|
| **JTLS-GO** (Rolands & Associates) | Government/military | ~$50K–$200K+ per license | Theater-level joint/combined ops simulation; air, land, sea, SOF | ❌ None |
| **JCATS** (LLNL) | Government/military | Contract-based (govt only) | Tactical-level joint conflict simulation | ❌ None |
| **WISDOM** (NATO MSCOE) | Government/military | NATO-internal | Scenario configuration, visualization, integration with JTLS/JCATS | ❌ None |
| **ONE-SAF** (US Army) | Government/military | Government-only | US Army constructive simulation baseline | ❌ None |
| **SWORD** (ST Engineering Antycip) | Commercial | ~€50K–€150K | Tactical simulation, HLA-compatible | ❌ None |
| **ScenarioAI + Systematic** | Commercial | Contract-based | AI/ML-enhanced wargaming; NATO Next Gen M&S demo (2024) | ⚠️ Partial |
| **BAE Systems AI Wargaming Suite** | Commercial | Contract-based (€M+) | AI-driven hybrid warfare modeling | ⚠️ Partial |
| **Panopticon AI** | Startup | Contract-based | AI wargaming, scenario forecasting | ✅ Core AI |
| **Snow Globe** (arXiv, open-source) | Research | Free | Open-ended wargames with LLMs; proof-of-concept | ✅ Built on LLMs |

**Identified Gaps:**
- **No LLM-native dynamic scenario generation** — existing tools require manual scenario design by SMEs
- **No uncensored reasoning** — commercial AI tools apply corporate filters; militaries need unconstrained what-if analysis
- **No sovereign on-premise option in SE Europe** — NATO tools are government-internal; commercial tools are cloud or proprietary
- **Adjudication is rigid** — JTLS/ONE-SAF use deterministic equations; LLMs could enable narrative-driven qualitative adjudication

---

### 1.2 Adversarial Reasoning & Red-Teaming

| Tool | Type | Pricing | Key Features | LLM Integration? |
|------|------|---------|-------------|:-:|
| **PyRIT** (Microsoft) | Open-source | Free | Automated adversarial attack generation; red-teaming SDK | ✅ Core |
| **Garak** (NVIDIA) | Open-source | Free | 120+ probe types for LLM vulnerability scanning | ✅ Core |
| **Promptfoo** | Open-source + paid | Free / Team $99/mo | LLM security testing, red-teaming fuzzing | ✅ Core |
| **DeepTeam** | Commercial | Freemium | LLM red-teaming, MITRE ATLAS integration | ✅ Core |
| **General Analysis** | Commercial | Contract-based | Comprehensive AI red-teaming platform | ✅ Core |
| **Giskard** | Open-source + paid | Free / Enterprise custom | ML & LLM safety testing | ✅ Core |
| **MITRE ATLAS** | Framework | Free | 16 tactics, 84 techniques for AI adversary TTPs | ✅ Framework |
| **NIST AI RMF** | Framework | Free | AI risk management process framework | ⚠️ Framework |
| **HiddenLayer** | Commercial | Contract-based | ML/AI security monitoring | ✅ |

**Identified Gaps:**
- **All tools target AI security, not geopolitical/military adversarial reasoning** — no tool combines AI red-teaming with strategic adversarial reasoning
- **No classified-grade deployment** — PyRIT/Garak/Promptfoo are designed for cloud; no air-gapped enterprise red-teaming platform
- **No integrated wargaming + red-teaming** — no tool links adversarial AI probing with military scenario modeling
- **No European sovereign option** — all major tools are US-based

---

### 1.3 Ethical Analysis Frameworks

| Tool / Framework | Type | Pricing | Key Features |
|-----------------|------|---------|-------------|
| **DST Ethical AI Checklist** (Australia) | Government framework | Free | Checklist, Risk Matrix, LEAPP program |
| **RAID Toolkit** (DAIRNet, Australia) | Government framework | Free | Grounded in NATO, UK, US, AU, OECD frameworks |
| **UK DSTL AI Ethics Cards** | Government framework | Free | Flexible card-based toolkit for defence AI |
| **NATO AI Strategy** | Policy framework | N/A | Endorsed 2024 revised AI Strategy |
| **EU AI Act (Defence Exemptions)** | Regulation | N/A | Military AI largely exempt; soft-law frameworks apply |
| **Taddeo et al. Ethical Principles** | Academic | Free | 5 principles for military AI ethics |

**Identified Gaps:**
- **All frameworks are manual checklists** — no automated ethical reasoning or compliance checking at runtime
- **No LLM-native ethical analysis** — no tool uses AI to evaluate military decisions against ethical frameworks
- **No integration with wargaming/scenario tools** — ethical checklists exist separately from simulation
- **European frameworks are fragmented** — NATO, EU, and national frameworks don't converge

---

### 1.4 Classified Data Handling

| Tool / Platform | Type | Pricing | Key Features |
|-----------------|------|---------|-------------|
| **Palantir Gotham / AIP** | Commercial | ~$141K/core perpetual | Classified data fusion, AI decision support |
| **Anduril Lattice** | Commercial | Contract-based (DoD $20B IDIQ) | Edge-based mission autonomy, sensor integration |
| **VDF.AI** | Commercial | Contract-based | Sovereign AI agents; air-gapped on-premise |
| **Scrydon** | Commercial (European) | Contract-based | European-native sovereign AI; air-gapped tactical intelligence |
| **Google Distributed Cloud (Air-Gapped)** | Commercial | Contract-based | Air-gapped cloud for classified workloads |
| **Hopsworks** | Open-core | Free / Enterprise custom | Sovereign AI infrastructure; on-prem Kubernetes |
| **Specgen** | Commercial (French) | Contract-based | French sovereign on-premise AI for defense |
| **MediaStream.AI** | Commercial (UK) | Contract-based | UK sovereign AI infrastructure; air-gapped |
| **NATO DIANA Accelerator** | Program | Grant funding (up to €400K) | Dual-use deep tech accelerator |

**Identified Gaps:**
- **US-centric dominance** — Palantir/Anduril control the classified AI market
- **No Greek/Mediterranean sovereign option** — European alternatives are Nordic, French, or UK
- **Integration gap** — existing sovereign platforms are infrastructure-only; no platform combines infrastructure + LLM reasoning + domain-specific tools
- **No uncensored models for classified use** — all commercial models have content filters
- **GDPR + NATO security dual requirement** — no platform fully satisfies both

---

### 1.5 European / Greek Defense Market

| Institution / Initiative | Relevance |
|-------------------------|-----------|
| **Hellenic Centre for Defence Innovation (ELKAK)** | Greek government body funding defense R&D |
| **ELIAMEP Defence Hub** | Greek think tank defense analysis |
| **Pharos** | Greek national AI hub (EuroHPC); operational 2026–2028 |
| **Greek National AI Strategy** | Published 2024; covers defense, healthcare, education |
| **European Defence Fund (EDF)** | €8B (2021–2027); co-finances AI-enabled defense projects |
| **PESCO** | EU permanent structured cooperation; includes AI defense projects |
| **NATO DIANA** | Accelerator with 16 sites; dual-use tech |
| **Hellenic Aerospace Industry (HAI)** | Country's largest defense company |
| **Space Hellas, Elfon, Mevaco** | Greek defense ICT ecosystem |

**Market Observation:** Greece has no domestic sovereign AI platform for defense. The Pharos AI hub is infrastructure-focused (compute), not application-layer. ELKAK funds R&D but has no operational AI platform. Greek defense currently relies on foreign (US/French/German) tools across all categories.

---

## 2. Think Tanks

### 2.1 Policy Research & Synthesis

| Tool | Type | Pricing | Key Features | LLM Integration? |
|------|------|---------|-------------|:-:|
| **Overton Index** | SaaS | $10K–$30K/yr institution; $1,405/yr individual | 11M+ policy documents from 44K+ orgs | ⚠️ Search-based |
| **Overton Engage** | SaaS | Custom pricing | Research-policy impact tracking | ⚠️ Search-based |
| **Nesta Policy Atlas** | Free tool | Free | Digital policy evidence exploration | ⚠️ Search-based |
| **PolicyPulse** (arXiv) | Research tool | Free | LLM-based policy synthesis | ✅ LLM-native |
| **Elicit** | SaaS | Free / Team $10/mo / Enterprise custom | AI research assistant | ✅ LLM-native |
| **Consensus** | SaaS | Free / Premium $9.99/mo | AI academic search & synthesis | ✅ LLM-native |
| **scite.ai** | SaaS | Free / $20/mo / Team custom | Citation analysis | ✅ LLM-native |

**Identified Gaps:**
- **No classified-grade policy research tool** — Overton, Elicit, Consensus are SaaS; think tanks handling sensitive analysis cannot use them
- **No integrated adversarial reasoning** — policy synthesis tools summarize but don't stress-test positions
- **No offline/air-gapped option** — all major tools are cloud-indexed
- **No Greek/EU policy data specialization** — Overton is Anglophone-centric
- **No wargaming integration** — think tanks produce analysis but cannot run scenario modeling

---

### 2.2 Scenario Modeling (Think Tank Context)

| Tool | Type | Pricing | Key Features |
|------|------|---------|-------------|
| **RAND Corporation methods** | Academic | Free (methodology) | Strategic wargaming, structured analytic techniques |
| **CSIS Wargaming** | Academic | Free (methodology) | Democratized wargaming approaches |
| **SIGMA Scenario Manager** | Commercial | Custom pricing | Structured scenario planning |
| **GBN / Shell Scenario Planning** | Commercial | Custom pricing | Qualitative scenario methodology |
| **Foresight Platform** | Commercial | Custom pricing | Horizon scanning, trend analysis |

**Identified Gaps:**
- **No affordable LLM-native scenario tool** — think tanks cannot afford defense-grade simulators
- **No integration with policy research** — scenarios built in isolation from document analysis
- **No collaborative on-premise platform** — most use SharePoint + email

---

### 2.3 Key European / Greek Think Tanks

| Think Tank | Location | Focus |
|-----------|----------|-------|
| **ELIAMEP** | Athens, Greece | European/foreign policy, defense, security |
| **IOBE** | Athens, Greece | Economic policy, industrial strategy |
| **Dianeosis** | Athens, Greece | Policy research, social analysis |
| **CEPS** | Brussels, Belgium | EU policy, regulation, AI |
| **ECFR** | Berlin/London | Foreign policy, EU defense |
| **EPC** | Brussels, Belgium | EU policy, defense |
| **IAI** | Rome, Italy | International affairs, defense |
| **FRIDE / Elcano** | Madrid, Spain | Foreign policy, EU affairs |

---

## 3. NGOs

### 3.1 Grant Compliance & Impact Measurement

| Tool | Type | Pricing | Key Features | LLM Integration? |
|------|------|---------|-------------|:-:|
| **Fluxx Grantmaker** | SaaS | ~$15K–$50K+/year | End-to-end grant lifecycle | ❌ None |
| **Submittable** | SaaS | ~$5K–$25K/year | Application management, review | ⚠️ Basic AI |
| **Optimy** | SaaS (European) | ~€5K–€20K/year | Grant management, CSR reporting | ❌ None |
| **Good Grants** | SaaS | ~$200–$500/mo | Small-medium grant management | ❌ None |
| **Euna Grants** | SaaS | ~$10K–$40K/year | Federal/compliance grant tracking | ❌ None |
| **Instrumentl** | SaaS | $179/mo + $499/mo Pro | Grant discovery + post-award | ⚠️ Basic AI |
| **Amplifund** | SaaS | ~$10K–$30K/year | Federal grant compliance | ❌ None |
| **Blackbaud Grantmaking** | SaaS | ~$5K–$20K/year | Fund accounting, grant tracking | ❌ None |
| **Sopact** | SaaS | Custom pricing | AI-powered impact measurement | ✅ AI-native |
| **Benevity** | SaaS | Custom pricing | CSR, grant management, impact | ⚠️ Basic AI |

**Identified Gaps:**
- **No on-premise option for sensitive grant data** — all tools are SaaS; NGOs handling sensitive data cannot use them
- **Impact measurement is disconnected from AI analysis** — Sopact is cloud-only
- **No GDPR-compliant non-US alternative** — most tools are US-based
- **Grant compliance is manual** — no AI-driven compliance checking
- **No scenario modeling for program planning** — NGOs cannot model strategy changes
- **Greek NGOs underserved** — limited Greek-language support

---

### 3.2 Ethical Analysis Frameworks (NGO Context)

| Tool / Framework | Type | Pricing | Key Features |
|-----------------|------|---------|-------------|
| **UNESCO AI Ethics Framework** | Policy framework | Free | Global AI ethics guidelines |
| **EU AI Act Compliance Tools** | Commercial | €1K–€50K/year | AI system classification, risk assessment |
| **Partnership on AI (PAI)** | Membership | Free/paid | Multi-stakeholder AI ethics |
| **OECD AI Principles** | Policy framework | Free | Intergovernmental AI ethics standards |
| **IRIS+ (GIIN)** | Framework | Free | Impact measurement standards for ESG |
| **Human Rights Due Diligence Tools** | Commercial/Open | Varies | UN Guiding Principles compliance |

**Identified Gaps:**
- **No LLM-native ethical compliance checking** — NGOs must manually assess against frameworks
- **No integrated human rights impact assessment** — ethical analysis separate from program management
- **No on-premise option for sensitive human rights data** — NGOs collecting testimonies cannot use cloud AI

---

### 3.3 Key European / Greek NGOs

| NGO | Location | Focus |
|-----|----------|-------|
| **SolidarityNow** | Athens, Greece | Refugee support, social inclusion |
| **Praksis** | Athens, Greece | Humanitarian aid, social services |
| **Médecins Sans Frontières** | International | Medical humanitarian |
| **Greenpeace Greece** | Athens, Greece | Environmental |
| **WWF Greece** | Athens, Greece | Environmental conservation |
| **The Smile of the Child** | Athens, Greece | Child protection |
| **Human Rights Watch (EU)** | Brussels | Human rights |
| **Transparency International (EU)** | Brussels | Anti-corruption |

---

## 4. Cross-Cutting Analysis

### 4.1 The AI/LLM Integration Gap

| Category | Current State | What's Missing |
|----------|--------------|----------------|
| Scenario Modeling | Deterministic simulators; manual design | LLM-driven dynamic scenario generation, adversarial branching |
| Adversarial Reasoning | AI security red-teaming only | Strategic adversarial reasoning for military/geopolitical scenarios |
| Ethical Analysis | Manual checklists; no runtime enforcement | LLM-powered ethical reasoning, automated compliance, auditable provenance |
| Policy Research | Narrow SaaS tools (search, citations) | LLM-native synthesis, adversarial stress-testing, scenario integration |
| Classified Data Handling | US-centric proprietary platforms | European sovereign alternative with LLM reasoning |
| Grant Compliance | Workflow automation; no AI analysis | AI-driven impact measurement, compliance checking, program scenarios |

### 4.2 The Sovereign Gap

**US vendors dominate every category.** The European response is fragmented:

- **Infrastructure layer:** Pharos (Greece), EuroHPC, Gaia-X — compute, not application
- **Security layer:** Scrydon (Nordic), Specgen (French), MediaStream (UK) — narrow, country-specific
- **No unified sovereign AI platform** that combines LLM reasoning + domain-specific tools + air-gapped deployment in SE Europe

### 4.3 Pricing Benchmark Summary

| Category | Typical Tool Cost |
|----------|------------------|
| Wargaming simulation | $50K–$200K+ (license) |
| AI red-teaming | $0–$50K/year (open-source to enterprise) |
| Ethical compliance | $0 (manual) / $1K–$50K (EU AI Act tools) |
| Policy research | $10K–$30K/year |
| Grant management | $5K–$50K+/year |
| Classified AI platform | $M+ (Palantir, Anduril) |

---

## 5. Methodology & Sources

This report is based on public market research conducted July 2026:

- **NATO** modelling & simulation resources (MSCOE, WISDOM, JTLS-GO documentation)
- **Vendor websites** (Palantir, Anduril, BAE Systems, Overton, Fluxx, Sopact, etc.)
- **Academic sources** (arXiv: 2404.11446, Springer/CETaS/CSIS wargaming research)
- **Government publications** (European Defence Fund, NATO AI Strategy, Greek National AI Strategy)
- **Industry analysis** (Strategic Market Research, Gartner, DATaintelo, Future Market Insights)
- **Open-source tooling** (PyRIT, Garak, Promptfoo, MITRE ATLAS, NIST AI RMF)
- **European/Greek ecosystem** (ELKAK, Pharos, DIANA, EDF, ELIAMEP)

**Pricing notes:** Defense tool pricing is indicative (based on public procurement data and industry reports). Think tank and NGO SaaS pricing is based on published pricing pages and review sites (Capterra, GetApp, Software Advice).

---

*All information is from public sources. No proprietary or classified information is included.*  
*Published as community research for the open-source AI sovereignty space.*  
*Last updated: July 2026*
