---
summary: "{{VALUE:Resumen del proyecto}}"
language: "<% await tp.system.suggester(["JavaScript", "TypeScript", "Python"], ["javascript", "typescript", "python"]) %>"
framework: "<% await tp.system.suggester(["React", "Next.js", "Astro", "TanStack", "None"], ["react", "nextjs", "astro", "tanstack", ""]) %>"
tools: "<% await tp.system.suggester(["shadcn", "tailwind", "motion", "threejs3d", "lerpa", "reui", "strapi", "wordpress", "payloadcms", "directus", "contentful", "sanity", "None"], ["shadcn", "tailwind", "motion", "threejs3d", "lerpa", "reui", "strapi", "wordpress", "payloadcms", "directus", "contentful", "sanity", ""]) %>"
---

# 🚀 {{TITLE}}

> **Resumen:** {{summary}}

## Objetivo
{{VALUE:Describe the project}}

## Tecnologías
| Capa | Tecnología |
| :--- | :--- |
| **Frontend** | |
| **Backend** | |
| **Database** | |
| **Auth** | |
| **Deploy** | |

## Características
- [ ] Feature 1

## Arquitectura
<!-- Añadir Mermaid o enlace a Canvas -->