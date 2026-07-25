---
summary: "{{VALUE:Resumen del error}}"
language: "<% await tp.system.suggester(["JavaScript", "TypeScript", "Python"], ["javascript", "typescript", "python"]) %>"
framework: "<% await tp.system.suggester(["React", "Next.js", "Astro", "TanStack", "None"], ["react", "nextjs", "astro", "tanstack", ""]) %>"
tools: "<% await tp.system.suggester(["shadcn", "tailwind", "motion", "threejs3d", "lerpa", "reui", "strapi", "wordpress", "payloadcms", "directus", "contentful", "sanity", "None"], ["shadcn", "tailwind", "motion", "threejs3d", "lerpa", "reui", "strapi", "wordpress", "payloadcms", "directus", "contentful", "sanity", ""]) %>"
---

# 🐛 {{TITLE}}

> **Resumen:** {{summary}}

## Mensaje de error
{{VALUE:Paste the error message}}

## Pasos para reproducir
1. {{VALUE:Step 1}}
2. {{VALUE:Step 2}}

## Solución
```{{language}}
// Paste the fix here
````