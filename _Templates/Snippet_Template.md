---
summary: "{{VALUE:Breve descripción del snippet}}"
language: "<% await tp.system.suggester(["JavaScript", "TypeScript", "Python"], ["javascript", "typescript", "python"]) %>"
framework: "<% await tp.system.suggester(["React", "Next.js", "Astro", "TanStack", "None"], ["react", "nextjs", "astro", "tanstack", ""]) %>"
tools: "<% await tp.system.suggester(["shadcn", "tailwind", "motion", "threejs3d", "lerpa", "reui", "strapi", "wordpress", "payloadcms", "directus", "contentful", "sanity", "None"], ["shadcn", "tailwind", "motion", "threejs3d", "lerpa", "reui", "strapi", "wordpress", "payloadcms", "directus", "contentful", "sanity", ""]) %>"
---

# 🧩 {{TITLE}}

> **Resumen:** {{summary}}

## ¿Qué hace?
{{VALUE:Explain}}

## El código
```{{language}}
// Code here
````

## Cómo usarlo

1. {{VALUE:Step 1}}
2. {{VALUE:Step 2}}