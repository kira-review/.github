<h1 align="center">Kira <sub>キラ</sub></h1>

<p align="center"><strong>AI that learns how your team works.</strong></p>

<p align="center"><em>Intelligence that understands. Context that transforms.</em></p>

<p align="center">
  <img src="https://img.shields.io/badge/in_production-B35A6A?style=flat-square" alt="In production">
  <img src="https://img.shields.io/badge/code-private-1A1A1F?style=flat-square" alt="Private code">
  <img src="https://img.shields.io/badge/creative_·_recruitment-F7C2CD?style=flat-square" alt="Creative and recruitment">
</p>

---

Kira is an AI coworker for creative and recruitment teams. It analyzes artwork and candidates,
remembers how **your** reviewers judge work, and gets more aligned with them with every review.

It is not a generic ATS, and not a one-shot "score my design" tool. The product is the
**memory loop**:

```
  Kira proposes an evaluation   →   a human corrects it
            ↑                                ↓
  the next evaluation starts there  ←  the correction becomes team knowledge
```

## What it does

**Creative** — evaluates artwork, campaigns and copy per criterion (composition, typography,
colour, brand consistency), measures what can be measured in the image, and shows which
memories each score drew on. Reviewers correct it criterion by criterion, and the correction
sticks.

**Recruitment** — reads CVs and portfolios, scores candidates against a job and explains the
ranking. Protected personal characteristics are stripped from documents before any model sees
them, and every claim about a candidate carries the quote from the source that backs it.

**Knowledge** — every brand the team serves has its own memory. Rules the team already has go
in pasted or extracted from a brand book, and one client's material is never offered as a
reference for another.

**Conversation** — the whole of Kira can be driven from Claude, through an MCP server.

## Ground rules

1. **Nothing runs by itself.** Every analysis starts with someone asking for it, unless the
   team turns automation on.
2. **AI proposes, humans decide.** No AI-written record is authoritative on its own.
3. **Kira admits when it is wrong.** It measures its own bias against each reviewer's and
   shows it.

<p align="center">
  <img src="assets/signature.png" width="720" alt="Mountain, sun and cherry blossom — Kira's signature visual">
</p>

## How it is built

<p>
  <img src="https://img.shields.io/badge/React-1A1A1F?style=flat-square&logo=react&logoColor=F7C2CD" alt="React">
  <img src="https://img.shields.io/badge/TypeScript-1A1A1F?style=flat-square&logo=typescript&logoColor=F7C2CD" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind-1A1A1F?style=flat-square&logo=tailwindcss&logoColor=F7C2CD" alt="Tailwind">
  <img src="https://img.shields.io/badge/Hono-1A1A1F?style=flat-square&logo=hono&logoColor=F7C2CD" alt="Hono">
  <img src="https://img.shields.io/badge/Node_22-1A1A1F?style=flat-square&logo=nodedotjs&logoColor=F7C2CD" alt="Node 22">
  <img src="https://img.shields.io/badge/PostgreSQL_+_pgvector-1A1A1F?style=flat-square&logo=postgresql&logoColor=F7C2CD" alt="PostgreSQL + pgvector">
  <img src="https://img.shields.io/badge/Drizzle-1A1A1F?style=flat-square&logo=drizzle&logoColor=F7C2CD" alt="Drizzle">
  <img src="https://img.shields.io/badge/Claude-1A1A1F?style=flat-square&logo=anthropic&logoColor=F7C2CD" alt="Claude">
  <img src="https://img.shields.io/badge/MCP-1A1A1F?style=flat-square&logo=modelcontextprotocol&logoColor=F7C2CD" alt="MCP">
</p>

- **Memory with RAG** over pgvector embeddings, ranked and with traceable provenance.
- **Multi-tenant** with PostgreSQL row-level security: each agency isolated by the database.
- **Queues** with pg-boss for analyses, and S3-compatible storage.
- **246 integration tests** against a real Postgres, including a real MCP client.
- **Measured accessibility:** every text pair in the interface passes WCAG AA, computed rather than eyeballed.

## Design

A *Shoji + Workbench* language: surfaces divided by a hairline, no shadows, 2px radius; work
laid out in rows with a severity stripe that makes what needs attention findable before any
text is read. Jost for headings, Inter for the interface.

<p align="center">
  <img src="assets/palette.png" width="720" alt="Palette: Ink, Slate, Stone, Sakura, Blossom, Petal, Wood, Leaf">
</p>

---

<p align="center"><sub>The code is private. To learn more or see a demo, get in touch with the team.</sub></p>
