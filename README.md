# MCP GSC CPG

**A2A-MCP · CPG Supply Chain Procurement · AI Orderable (AIO) Hygiene, Beauty and Personal Care Rails and Agents · ESG via ERP Integration with ACM-68000.**

Operated by [GreenCore Solutions Corp.](https://gsc-em.com)

---

## What this is

A live MCP server exposing GreenCore's four CPG procurement rails to AI agents.

AI agents — Claude, GPT, Gemini, Grok, Mistral — connect to `mcp.gsc-em.com` and resolve procurement intent against GreenCore's catalog via the ACM-68000 protocol.

**MCP endpoint:** `https://mcp.gsc-em.com`

**Registry:** `io.github.gsc-em/a2a-mcp-cpg`

---

## Tools

| Tool | Purpose |
|---|---|
| `resolveGtin` | Returns discovery pointers for a GTIN — trust anchor, jurisdictional A2A node, canonical ingress. |
| `getProduct` | Returns full product detail for a registered GTIN — label, SKU, rail, SGS certification, signal. |
| `listProducts` | Returns the full GSC catalog across all four rails. |
| `ingestSignal` | Forwards a procurement intent to the canonical agentic commerce ingress. |

---

## Rails

| Rail | Category | Status |
|---|---|---|
| `AIO-TFX-Rail` | Hygiene — TreeFree Diaper® (Private Label) | Live, 2 GTINs |
| `AIO-HPL-Rail` | Hygiene MDD Private Label | Live, open for converter onboarding |
| `AIO-BPL-Rail` | Beauty Personal Care MDD Private Label | Live, open |
| `AIO-BPC-Rail` | Beauty Personal Care Branded | Live, open |

---

## Live GTINs

**AIO-TFX-Rail · TreeFree Diaper® (Private Label, single-product)**

| GTIN | Format | SGS Certificate | EUDR | ACM Signal |
|---|---|---|---|---|
| `00990832300006` | Open / Tape, 240 Each | SGS 52583 | Deforestation-Free (0% tree fiber → NOT_APPLICABLE logic) | ACM-200 · ALLOW |
| `00990832300013` | Pant / Pull-up, 240 Each | SGS 51912 | Deforestation-Free (0% tree fiber → NOT_APPLICABLE logic) | ACM-200 · ALLOW |

Both made with **TreeFree Core®**.
Compliance Stack: CSRD · EUDR · Loi AGEC · EU Taxonomy

---

## Ghost Headers

Every response carries the GreenCore Ghost Header set:

```
X-GSC-Protocol: ACM-68000
X-GSC-Version: 1.0.0
X-GSC-Router: mcp.gsc-em.com
X-GSC-Role: mcp-server
X-GSC-Operator: GreenCore Solutions Corp.
X-GSC-Registry: io.github.gsc-em/a2a-mcp-cpg
X-MCP-Server: https://mcp.gsc-em.com
X-MCP-Registry: io.github.gsc-em/a2a-mcp-cpg
X-Agent-Access: Claude,Mistral,Gemini,Grok,OpenAI
```

---

## License

MIT — see [LICENSE](LICENSE).

---

## Links

| Name | URL |
|---|---|
| GreenCore Solutions Corp. | [gsc-em.com](https://gsc-em.com) |
| Repository | [github.com/gsc-em/a2a-mcp-cpg](https://github.com/gsc-em/a2a-mcp-cpg) |
| MCP Registry | `io.github.gsc-em/a2a-mcp-cpg` |
