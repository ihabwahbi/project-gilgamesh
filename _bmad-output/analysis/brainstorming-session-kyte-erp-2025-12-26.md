---
stepsCompleted: [1, 2, 3, 4]
inputDocuments:
  - /workspace/projects/kyte (ERP mockup)
  - /workspace/projects/cost-management/thoughts/shared/implementation-reports/2025-12-23-comprehensive-app-valuation.md
session_topic: 'Kyte ERP - Market viability and MVP scope for AI-powered Australian SMB ERP'
session_goals: 'Validate market opportunity, define MVP scope, establish go-to-market strategy'
selected_approach: 'first-principles + assumption-validation'
techniques_used:
  - first-principles-thinking
  - assumption-validation
  - market-research
  - competitive-analysis
ideas_generated: [market-validation, integration-insight-value-prop, vertical-selection, mvp-scope, pricing-strategy, pilot-strategy]
context_file: ''
decision: GO
target_revenue: $199/mo per customer, pilot at $99/mo lock-in
target_vertical: Wholesale/Distribution
---

# Kyte ERP Brainstorming Session Results

**Facilitator:** Mary (Business Analyst)
**Participant:** Ihab
**Date:** December 26, 2025
**Decision:** **GO — Build Kyte ERP**

---

## Executive Summary

| Question | Answer |
|----------|--------|
| Is the market real? | **YES** — AU ERP market $1.3B → $3.8B by 2030 (16% CAGR) |
| Is the pain real? | **YES** — 53% SMBs report data inconsistencies, 40% manual entry errors |
| Can Ihab build it? | **YES** — Demonstrated $1.4M app in 4 weeks solo |
| Is there competitive advantage? | **YES** — AI-native, unified insights, Australian-first, cost savings |
| What's the MVP? | Inventory + Sales + Finance + AI for Wholesale/Distribution |
| Timeline to MVP? | **4-5 weeks** |
| Pricing? | **$199/mo** (Growth), $99/mo pilot lock-in |
| Go-to-market? | Land ONE pilot customer first, then scale |

---

## Session Context

### What is Kyte?

Kyte is envisioned as a modern, AI-powered ERP system for Australian small businesses. The existing mockup includes:

| Component | Status |
|-----------|--------|
| Tech Stack | Next.js 14, React 18, TypeScript, tRPC, Drizzle ORM, PostgreSQL, Turborepo |
| UI Framework | Tailwind CSS v4, Radix UI components |
| Modules (Mockup) | Dashboard, Inventory, Sales/CRM, HR, Finance, Settings |
| AI Feature | "Kyte AI" assistant integrated throughout |
| Database Schemas | Users, Products, Categories, Inventory, Customers, Orders, Employees |

### Ihab's Capabilities

Ihab demonstrated extraordinary development velocity with his Cost Management application:

| Metric | Value |
|--------|-------|
| Total Lines of Code | 195,000+ |
| Source Files | 23,900+ |
| Development Time | **1 month (solo)** |
| Equivalent Market Value | **$1.2M - $1.5M** |
| Traditional Timeline | 14-20 months with 6-9 developers |

Key capabilities proven:
- Full-stack architecture (Next.js + tRPC + PostgreSQL)
- Enterprise-grade authentication (WebAuthn, passkeys)
- AI integration (multi-provider LLM, RAG memory, tool registry)
- Complex business logic (P&L calculations, ETL pipelines)
- Production deployment (Azure, Docker, CI/CD)

---

## Phase 1: Market Viability Analysis

### Australian ERP Market

| Metric | Value | Source |
|--------|-------|--------|
| Australia ERP Market (2023) | $1.33 billion AUD | Grand View Research |
| Australia ERP Market (2030) | $3.78 billion AUD | Grand View Research |
| Australia CAGR | ~16% annually | Calculated |
| Global ERP Market (2025) | $73 billion USD | Cargoson |
| Cloud ERP Share | 70% of market | Cargoson |
| Cloud ERP Growth | 14.5% annually | vs 2% on-premise |
| SMB ERP Growth | 14.7% CAGR | Industry research |
| SMBs using/planning ERP | 92% of high-performers | Industry research |

### Competitive Landscape (Australia)

| Competitor | Type | Weakness |
|------------|------|----------|
| MYOB | Accounting → ERP (Acumatica) | Legacy architecture, not AI-native |
| Xero | Accounting only | Not a full ERP, limited modules |
| QuickBooks | Accounting | US-focused, not Australian-first |
| NetSuite | Full ERP | Expensive, complex, enterprise-focused |
| Odoo | Open-source ERP | Requires customization, support gaps |
| SAP/Oracle | Enterprise | Overkill for SMBs, expensive |

### Gap Identified

**No existing solution offers:**
- AI-native architecture (not bolted-on AI)
- Australian-first compliance and design
- SMB-friendly pricing ($199/mo vs $500+/mo)
- True unified data model (not integrations)
- Self-service customization

---

## Phase 2: Assumption Validation

### Assumption 1: Integration Pain Point
**"Businesses using Xero + Employment Hero + others lack integration"**

| Evidence | Finding |
|----------|---------|
| Average SaaS tools per business | 130-300 applications |
| SMB leaders with data inconsistencies | 53% report problems |
| Manual data entry error rate | Affects 40% of business records |
| Time on automatable tasks | 41% of knowledge worker time wasted |
| Employment Hero + Xero | Dedicated error dashboard exists for sync failures |

**Verdict: STRONGLY VALIDATED**

### Assumption 2: Customization Demand
**"Kyte can be customized to granular business-specific workflows"**

| Evidence | Finding |
|----------|---------|
| SMB workflow automation demand | Growing rapidly |
| Custom ERP value | Documented ROI for unique workflows |

**Verdict: VALIDATED WITH CAVEAT**

SMBs want customization but EASY customization:
- No complex configuration UIs
- No consultants needed
- No months of implementation
- No IT staff required

**Kyte's opportunity:** AI-powered, natural language workflow customization.

### Assumption 3: Target Small Businesses
**"I should target small businesses (10-50 employees)"**

| Evidence | Finding |
|----------|---------|
| High-performing SMBs using/planning ERP | 92% |
| Small Business ERP CAGR | 14.7% annual growth |
| SMBs finding compliance stressful | 56% |
| SMBs worried about payroll errors | 37% |
| Mental health impact | 48% negatively affected |
| Australian SMBs (10-50 employees) | ~250,000 businesses |

**Verdict: VALIDATED**

---

## Phase 3: Value Proposition

### The Integration Paradox

| Zapier/Make Approach | Kyte Approach |
|---------------------|---------------|
| Syncs data between systems | One unified data model |
| Each tool has its own reports | One source of truth |
| AI would need to query 5 systems | AI sees everything instantly |
| Data movement | **Business intelligence** |

### The Insight Unlock

**Fragmented Systems:**
```
Xero → Manual extraction → Excel → Analysis (hours, stale, errors)
Employment Hero ↗
Cin7 Inventory ↗
HubSpot ↗
```

**Kyte:**
```
Unified Data Model → Kyte AI → Instant insights + recommendations
```

**Example AI Insight (impossible with fragmented tools):**
> "Your profit margin dropped 8% this month because overtime hours increased 40% while you had 3 stockouts that delayed orders. Want me to adjust reorder points?"

### Cost Savings Angle

| Current Stack (Typical AU SMB) | Monthly Cost |
|-------------------------------|--------------|
| Xero (Growing plan) | $86 |
| Employment Hero (10 users) | $120 |
| Cin7/DEAR Inventory | $249 |
| HubSpot (Starter) | $50 |
| Zapier (Pro) | $75 |
| **Total** | **$580/mo** |

| Kyte (All-in-One) | Monthly Cost |
|-------------------|--------------|
| Kyte Growth | **$199/mo** |
| **Savings** | **$381/mo ($4,572/year)** |

**Positioning:** *"Half the cost. Ten times the insight."*

---

## Phase 4: MVP Scope Definition

### Vertical Selection: Wholesale/Distribution

| Attribute | Reasoning |
|-----------|-----------|
| Market Size | ~45,000 businesses in Australia |
| Pain Level | Highest from disconnected Inventory ↔ Sales ↔ Finance |
| Customer Stickiness | B2B relationships harder to churn |
| Order Values | Higher values justify $199/mo easily |
| Seasonality | Less seasonal than retail |
| Experience Fit | Ihab's Cost Management experience translates |
| Competitive Gap | Often underserved — too small for SAP, too complex for Xero |

### Ideal Pilot Customer Profile

| Attribute | Target |
|-----------|--------|
| Size | 10-30 employees |
| Revenue | $2M - $20M/year |
| Current stack | Xero + spreadsheets OR Xero + basic inventory app |
| Pain signal | "I never know my real stock levels" or "Month-end is a nightmare" |
| Location | Australia |

### MVP Scope (Option B+)

**Included:**

| Module | Features |
|--------|----------|
| **Inventory** | Products, stock levels, reorder points, categories, suppliers |
| **Sales/Orders** | Customers, orders, order status, basic invoicing |
| **Finance (Basic)** | Expense tracking, profit margins by product, cash flow visibility |
| **Dashboard** | Revenue KPIs, stock alerts, top products, trends |
| **Kyte AI** | Unified insights, recommendations, natural language queries |
| **Xero Sync** | Push invoices, sync payments |

**Excluded (v2):**

- Full HR module
- Payroll processing
- Leave management
- Rostering
- Complex general ledger
- Multi-warehouse
- Manufacturing/BOM

### Timeline (Ihab-Calibrated)

| Week | Focus | Deliverable |
|------|-------|-------------|
| Week 1 | Core foundation | Auth, DB schema, tRPC setup, UI shell, all modules scaffolded |
| Week 2 | Inventory + Sales | Full CRUD, orders, customers, products, stock tracking |
| Week 3 | Finance + Dashboard | Invoicing, expenses, margins, KPIs, charts |
| Week 4 | Kyte AI + Polish | AI insights, recommendations, natural language queries |
| Week 5 | Xero sync + Launch prep | Integration, onboarding flow, landing page |

**Total: 4-5 weeks to production-ready MVP**

---

## Phase 5: Pricing Strategy

### Pricing Tiers

| Tier | Price | Target | Limits |
|------|-------|--------|--------|
| **Starter** | $99/mo | Solo/micro wholesalers | 2 users, 500 products, 100 orders/mo |
| **Growth** | $199/mo | Small wholesalers | 10 users, 5,000 products, 1,000 orders/mo |
| **Scale** | $399/mo | Growing distributors | 25 users, unlimited products/orders |

### Pilot Offer

- **Price:** $99/mo locked in forever (Growth features)
- **Commitment:** 2-3 months usage
- **Requirements:** Weekly feedback (15 min), case study rights
- **Value:** Direct founder access, custom features

---

## Phase 6: Go-to-Market Strategy

### Pilot Acquisition Strategy

**Method:** Leverage friends' networks for warm introductions

**Friend Outreach Brief:**

> **What I'm building:** Kyte — an AI-powered business management platform for Australian wholesalers/distributors. One system for inventory, sales, and finance instead of 4-5 disconnected tools.
>
> **What I need:** ONE pilot customer willing to:
> - Use Kyte for free for 2-3 months
> - Give honest feedback weekly (15 min call)
> - Become a case study if it works
>
> **Ideal business:**
> - Wholesaler, distributor, or importer
> - 10-30 staff, $2M-$20M revenue
> - Currently frustrated with their systems
> - Owner/manager willing to try something new
>
> **What they get:**
> - Free access during pilot
> - Direct line to the founder
> - Custom features if needed
> - Locked-in early adopter pricing ($99/mo forever)

### Pilot Onboarding Process

| Step | Action | Goal |
|------|--------|------|
| 1 | Discovery call (30 min) | Understand their specific pain |
| 2 | Data import | Get their products, customers, stock into Kyte |
| 3 | Guided setup (1 hour) | Configure for their workflow |
| 4 | Week 1 check-in | What's working? What's broken? |
| 5 | Week 2-4 iterations | Fix issues, add quick wins |
| 6 | Success review | Did Kyte deliver value? |

### Success Metrics for Pilot

| Metric | Target | Why |
|--------|--------|-----|
| Daily active usage | 5+ days/week | They're actually using it |
| Features used | 3+ modules | Not just one thing |
| Time saved | 5+ hours/week | Quantifiable value |
| "Aha moment" | At least 1 | AI insight they couldn't get before |
| Willingness to pay | Yes | Real validation |
| Referral | Would recommend | Future growth signal |

### Product-Market Fit Signal

**You've validated PMF when the pilot says:**
> "I don't want to go back to my old system."

OR

> "Can I pay now? I want to keep using this."

---

## Action Plan

### Parallel Execution

| Week | Ihab (Building) | Friends (Finding) |
|------|----------------|-------------------|
| Week 1 | Foundation + Inventory | Share brief, identify candidates |
| Week 2 | Sales + Customers | Warm intros, initial conversations |
| Week 3 | Finance + Dashboard | Qualify 1-2 serious candidates |
| Week 4 | Kyte AI + Polish | Schedule pilot onboarding |
| Week 5 | Pilot onboarding | Support conversations |
| Week 6-8 | Iterate based on feedback | — |

### Pre-Build Checklist

- [x] Vertical confirmed: Wholesale/Distribution
- [x] Pricing confirmed: $199/mo (Growth), $99/mo pilot lock-in
- [x] MVP scope defined: Inventory + Sales + Finance + AI + Xero sync
- [x] Timeline set: 4-5 weeks
- [x] Success metrics defined: Daily usage, time saved, willingness to pay
- [ ] Friends briefed: Send outreach brief
- [ ] Demo video created: 5-minute walkthrough of mockup
- [ ] Pilot agreement drafted: Terms for free pilot period

---

## Risk Assessment

| Risk | Severity | Mitigation |
|------|----------|------------|
| Can't find pilot customer | Medium | Multiple friends searching, expand to LinkedIn/communities |
| Pilot doesn't engage | Medium | Weekly check-ins, direct founder support |
| Feature requests overwhelm | Low | Ihab's velocity handles this |
| Xero integration complexity | Low | Well-documented API, can defer if needed |
| Competitors copy | Low | Speed + execution advantage |

---

## Financial Projections (Conservative)

### Path to $10k MRR

| Month | Paying Customers | MRR |
|-------|------------------|-----|
| Month 1-2 | 0 (building + pilot) | $0 |
| Month 3 | 1 pilot converts | $99 |
| Month 4 | 5 customers | $795 |
| Month 5 | 15 customers | $2,385 |
| Month 6 | 30 customers | $4,770 |
| Month 7 | 50 customers | $7,950 |
| Month 8 | 65 customers | $10,335 |

**$10k MRR achievable in ~8 months** (65 customers at blended $159/mo average)

### Break-Even Analysis

| Cost Category | Monthly |
|---------------|---------|
| Hosting (Vercel/Railway) | $50-100 |
| Database (managed Postgres) | $50-100 |
| AI API (OpenAI/Anthropic) | $100-300 |
| Xero partner fees | $0 (revenue share model) |
| Domain/email | $10 |
| **Total** | **~$300-500/mo** |

**Break-even: 3 customers at $199/mo**

---

## Closing Summary

### Why This Will Work

1. **Market is real** — $3.8B AU market by 2030, 16% CAGR
2. **Pain is validated** — 53% data inconsistencies, 40% error rates
3. **Gap exists** — No AI-native, Australian-first, SMB-priced unified ERP
4. **Ihab can build it** — Proven $1.4M output in 4 weeks
5. **Value prop is clear** — Half the cost, ten times the insight
6. **Strategy is lean** — One pilot, validate, then scale

### Decision: GO

**Build Kyte. Land one customer. Prove the value. Then scale.**

---

*Session completed: December 26, 2025*
*Techniques used: First Principles Thinking, Assumption Validation, Market Research*
*Decision: GO*
*Next action: Brief friends, start building Week 1*
