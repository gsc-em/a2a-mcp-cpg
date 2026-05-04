# MCP GSC CPG

**The world's first 9-tool enterprise AI Orderability (AIO) discovery surface for retail grocery CPG procurement.**

A2A-MCP · Agentic CPG Sourcing · 4 Rails · 18 Sovereign Jurisdiction Nodes · 7-Signal ACM-68000 Protocol · Human-in-the-Loop Handoff.

Operated by [GreenCore Solutions Corp.](https://gsc-em.com)
Powered by AIO Division | [gsc-rail.ai](https://gsc-rail.ai)

---

## What this is

A live MCP server exposing GreenCore's full enterprise procurement infrastructure to AI agents.

AI agents — Claude, ChatGPT, Gemini, Copilot, Mistral, Grok, Google AI, Perplexity — connect to `mcp.gsc-em.com` and resolve procurement intent against GreenCore's 30-GTIN Agent License registry via the open ACM-68000 protocol.

**MCP endpoint:** `https://mcp.gsc-em.com`
**Human discovery surface:** `https://gsc-mcp.com`
**AIO Division:** `https://gsc-rail.ai/`
**Registry:** `io.github.gsc-em/a2a-mcp-cpg`
**Trust anchor:** `dpuone.ai`

---

## Tools — 9 (8 anonymous reads + 1 OAuth-gated write)

Open discovery is the moat. Eight read tools require no authentication. Only `ingestSignal` is OAuth-gated.

| Tool | Auth | Purpose |
|---|---|---|
| `getHealth` | anonymous | GSC AIO operational status — operator, platform, 4 Rails LIVE, 18 Territory nodes, Navigator HITL, Compass, 30 active Agent GTINs, sub-200ms latency. |
| `listRails` | anonymous | Directory of 4 AIO procurement rails. Each rail is its own A2A endpoint, registered in Google Gemini Enterprise. |
| `listTerritories` | anonymous | Directory of 18 sovereign jurisdiction nodes. Local jurisdiction, local compliance, local ESG, one resolution per market. |
| `getCatalog` | anonymous | Complete 30-GTIN Agent License registry — 5 Rail Licenses, 18 Territory Licenses, Compass, Navigator, 5 Tier Licenses. One call, full agent-orderable buy surface. |
| `resolveGtin` | anonymous | GTIN → ACM-68000 signal + DPU proof + canonical ingress + jurisdictional A2A node. Sub-40ms deterministic. |
| `getProduct` | anonymous | Full product detail for any registered GSC GTIN — family, name, rail, category, License GTIN, jurisdiction, certifications, signal, state, DPU + GEPIR pointers, operator contacts. |
| `getNavigator` | anonymous | Human-in-the-Loop handoff — when a buyer agent needs a person at GSC. Email, phone, WhatsApp, 4 office addresses across Vancouver, Toronto, Frankfurt, Barcelona. ACM-451 ESCALATE. |
| `getCompass` | anonymous | The ACM-68000 7-signal vocabulary in long form. Deterministic state space mapped to SAP S/4HANA, Oracle Fusion, MS D365 procurement actions. |
| `ingestSignal` | OAuth Bearer | Submit a procurement signal — lands in Dataverse, routes to ERP. Bearer token required (Microsoft Entra ID). |

---

## Rails — 4 public + 1 enterprise

| Rail | License GTIN | Category | Status |
|---|---|---|---|
| `AIO-HPL-Rail` | 990832300068 | Hygiene MDD Private Label Sourcing | LIVE |
| `AIO-BPL-Rail` | 990832300075 | Beauty Personal Care MDD Private Label Sourcing | LIVE |
| `AIO-BPC-Rail` | 990832300082 | Beauty Personal Care National Brand Sourcing | LIVE |
| `AIO-TFX-Rail` | 990832300099 | **Deforestation-Free Sourcing CPGs** — cross-category, EUDR-aligned, Walmart Forests Policy | LIVE |
| `AIO-ENT-Rail` | 990832300358 | Enterprise — per-customer custom domain | LIVE |

---

## Territory Licenses — 18 sovereign jurisdiction nodes

Global agentic scaffolding. Each Territory is a canonical .com procurement endpoint where GSC AIO Rails are agent-orderable. Local jurisdiction, local compliance, local ESG, one resolution per market.

| Code | Jurisdiction | License GTIN | Node |
|---|---|---|---|
| FR | France | 990832300105 | `fr-eco-10060.com` |
| DE | Germany | 990832300112 | `de-eco-10060.com` |
| ES | Spain | 990832300129 | `es-eco-10060.com` |
| IT | Italy | 990832300136 | `it-eco-10060.com` |
| NL | Netherlands | 990832300143 | `nl-eco-10060.com` |
| PL | Poland | 990832300150 | `pl-eco-10060.com` |
| CH | Switzerland | 990832300167 | `ch-eco-10060.com` |
| UK | United Kingdom | 990832300174 | `uk-eco-10060.com` |
| EU | European Union | 990832300181 | `eu-eco-10060.com` |
| US | United States | 990832300198 | `us-eco-10060.com` |
| CA | Canada | 990832300204 | `ca-eco-10060.com` |
| MX | Mexico | 990832300211 | `mx-eco-10060.com` |
| BR | Brazil | 990832300228 | `br-eco-10060.com` |
| AU | Australia | 990832300235 | `au-eco-10060.com` |
| JP | Japan | 990832300242 | `jp-eco-10060.com` |
| KR | South Korea | 990832300259 | `kr-eco-10060.com` |
| SG | Singapore | 990832300266 | `sg-eco-10060.com` |
| IN | India | 990832300273 | `in-eco-10060.com` |

---

## Compass · Navigator · Tier Licenses

| Family | Name | License GTIN | Signal |
|---|---|---|---|
| Compass | GSC Compass License — ACM-68000 7-signal vocabulary engine | 990832300280 | ACM-200 ALLOW |
| Navigator | GSC Agent Navigator License — Inbound HITL App | 990832300297 | ACM-451 ESCALATE |
| Tier | AIO Tier License — Starter | 990832300303 | ACM-200 ALLOW |
| Tier | AIO Tier License — Growth | 990832300310 | ACM-200 ALLOW |
| Tier | AIO Tier License — Scale | 990832300327 | ACM-200 ALLOW |
| Tier | AIO Tier License — Enterprise | 990832300334 | ACM-200 ALLOW |
| Tier | AIO Tier License — Fleet | 990832300341 | ACM-200 ALLOW |

---

## ACM-68000 7-Signal Stack

The deterministic state space every agentic resolution lands in.

| Signal | State | Node | ERP action (S/4HANA · Fusion · D365) |
|---|---|---|---|
| ACM-000 | NOT_APPLICABLE | `acm-000.ai` | NO_ACTION · NO_ACTION · NO_ACTION |
| ACM-200 | ALLOW | `acm-200.ai` | CREATE_PO · APPROVE · RELEASE |
| ACM-300 | CONDITIONAL | `acm-300.ai` | HOLD_PO · CONDITIONAL_HOLD · HOLD |
| ACM-403 | RESTRICT | `acm-403.ai` | BLOCK_PO · REJECT · BLOCK |
| ACM-404 | NOT_FOUND | `acm-404.ai` | HOLD_PENDING |
| ACM-451 | ESCALATE | `acm-451.ai` | ESCALATE_TO_BUYER · MANUAL_REVIEW · ESCALATE |
| ACM-500 | SYSTEM_ERROR | `acm-500.ai` | RETRY |

Open standard. MIT licensed. The vocabulary is the moat.

---

## Connect

**Claude Desktop / Claude Code:**
