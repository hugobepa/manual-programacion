# AGENTS.md – Vault Instructions for AI Assistants

## Developer Profile

I am an indie frontend developer. My primary stack:

- **Languages:** TypeScript, JavaScript (ES2022), Python.
- **Frameworks/Libraries:** React, Next.js, Astro, Tailwind CSS, shadcn/ui, TanStack Query, TanStack Table, Zustand, Three.js.
- **Tools:** oRPC, Better Auth, Drizzle ORM, Supabase, Neon, Stripe, Polar, etc.
- **Package manager:** npm(preferer),bun,pnpm,Yarn 4+ (preferred) .

## Vault Structure (folders and their purpose)
```

📁 vault-root/
├── 📁 01_Concepts/ # Theory, exercises, resources (organized by subfolder)
│ ├── 📁 Notes/ # Pure theory and explanations
│ ├── 📁 Exercises/ # Practical exercises with solutions
│ └── 📁 Resources/ # External references, articles, links (no files, just notes)
├── 📁 02_Snippets/ # Reusable code snippets (short, self-contained)
├── 📁 03_Debug/ # Bug reports and their solutions
├── 📁 04_Projects/ # Project planning and documentation
│ ├── 📁 General/ # Cross-project notes (optional)
│ ├── 📁 Dashboard/ # Project 1: Admin Dashboard (React + Next.js + TanStack)
│ ├── 📁 WordPress/ # Project 2: Headless WordPress + React
│ ├── 📁 Astro/ # Project 3: Corporate static site with Astro
│ ├── 📁 MultiFramework/ # Project 4: Universal design system (Web Components)
│ └── 📁 Web3D/ # Project 5: Interactive 3D experiences (Three.js)
├── 📁 _Templates/ # Templater templates for new notes
│ ├── Concept_Template.md
│ ├── Snippet_Template.md
│ ├── Bug_Template.md
│ └── Project_Template.md
├── 📁 80_Resources/ # Binary or large reference files
│ ├── 📁 pdfs/ # PDF manuals, books, specification
│ ├── 📁 epubs/ # E-books
│ └── 📁 md/ # External Markdown references
├── 📁 81_Images/ # Images, diagrams, screenshots
│ ├── 📁 diagrams/ # Architecture, flow, UML diagrams
│ └── 📁 screenshots/ # UI / debugging screenshots
└── 📄 AGENTS.md # This file – instructions for AI

````

> **Important**: The folder structure is for human organisation. When reading notes, prioritise the frontmatter fields and the `summary`. Do not rely on folder names for semantic filtering.

---

## Frontmatter Standard (YAML properties)

Every note **MUST** have these fields at the top (between `---`):

| Field       | Type     | Allowed values                                                                  | Required |
| :---------- | :------- | :------------------------------------------------------------------------------ | :------- |
| `summary`   | string   | Short description (max 200 chars)                                               | **YES**  |
| `language`  | string   | `javascript`, `typescript`, or `python`                                         | **YES**  |
| `framework` | string   | `react`, `nextjs`, `astro`, `tanstack`, or `""` (empty string means none)       | **YES**  |
| `tools`     | string   | List as a comma‑separated string (e.g., `"shadcn, tailwind, threejs3d, strapi"`) | **RECOMMENDED** |

> **All other fields (e.g., `type`, `status`, `date`, `project`, `platform`, `tags`) are OPTIONAL and MUST be ignored for code generation.** They are for personal organization only.

**Example of a valid frontmatter:**

```yaml
---
summary: "useState hook for managing local state in React functional components"
language: "javascript"
framework: "react"
tools: "shadcn, tailwind"
---
````

---

## Code Generation Rules (MANDATORY)

When generating code, ALWAYS follow these rules:

1. **TypeScript strict mode**: `strict: true`, `noImplicitAny`, `strictNullChecks`.
2. **No `any`**: use `unknown`, proper types, or interfaces.
3. **React components**: define `interface Props` (or `type Props`) and export with `export const`.
4. **No derived state in `useEffect`**: compute derived values with `useMemo` or during render.
5. **Custom hooks** → `hooks/` folder; **types** → `types/` folder.
6. **Absolute imports**: `import { Button } from '@/shared/components/Button'`.
7. **Prefer functional components** over class components.
8. **Prefer Tailwind CSS** for styling, and `shadcn/ui` for UI components.
9. **Prefer Zustand** over React Context for global state (except for simple theme/ auth).
10. **Prefer TanStack Query** for server state (data fetching, caching, mutations).

---

## Response & Behaviour Rules

1. **Language**: Respond **in Spanish** (code comments can be in English or Spanish, as appropriate).
   - Exception: code itself (variables, functions) must use English names.
2. **Conciseness**: Keep responses clear, direct, and technical. Avoid verbose explanations unless explicitly asked.
3. **Honesty**: If you don't know something, say: _"No tengo información sobre eso en mis notas."_ Never invent facts or hallucinate.
4. **No external links**: Do not include clickable URLs. Mention the resource name (e.g., "React documentation").
5. **No chinese characters**: Write only in English or Spanish. Chinese is strictly forbidden.
6. **UTF‑8 encoding**: Ensure all output (code, explanations) is UTF‑8 compatible. Avoid emojis or special Unicode symbols that may break parsing.
7. **Sources & verification**: When referencing external knowledge, mention the source (e.g., "React official docs"). If a fact is not verifiable from your training data or my vault, state that clearly.
8. **Search depth**: When searching my notes for context, read the `summary` first, then the frontmatter fields, then the content. This reduces token usage and improves accuracy.
9. **Temperature and verbosity**: Keep the response temperature equivalent to **0.4** – factual, deterministic, and not creative. Limit output to the necessary information.

---

## How to Use This Vault (RAG workflow)

1. **Read the `summary`**: Understand the note's essence quickly.
2. **Check `language` and `framework`**: Determine the tech stack for code examples.
3. **Check `tools`**: Know which UI/CMS libraries are used.
4. **Read the body**: Extract code snippets, examples, and explanations.
5. **Use folder structure only for navigation**: Do not filter or classify by folder; rely on frontmatter.

**For project-specific context**, each subfolder in `04_Projects/` may contain a `PROJECT.md` file with objectives, stack details, and conventions. If present, read it when working on that project.

**For a general index**, a `README.md` file may exist in the root; it summarises the vault and can be used as a quick orientation.

---

## Notes on Note Content Quality

- Use clear headings (`#`, `##`, `###`) to structure content.
- Write short paragraphs and use bullet lists for readability.
- Include **real code examples** (not pseudo‑code) when possible.
- For diagrams, prefer **Mermaid** and ensure the text is legible.
- For external references, write the name and (optionally) the URL in plain text – avoid Markdown links to reduce token overhead.

---
## Folder -- templates

- 01_Concepts ---- _Templates/Concept_Template.md
- 02_Snippets ---- _Templates/Snippet_Template.md
- 03_Debug --- _Templates/Bug_Template
- 04_Projects --- _Templates/Project_Template

---

## Final Reminder

> The primary goal of this vault is to provide a **reliable, low‑noise knowledge base** for an AI assistant that generates production‑ready code. Stick to the frontmatter standards, follow the code rules, and always prioritize my notes over your own parametric knowledge when there is a conflict.