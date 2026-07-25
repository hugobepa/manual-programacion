---
summary: "{{VALUE:Resumen de 1-2 frases}}"
language: "<% await tp.system.suggester(["JavaScript", "TypeScript", "Python"], ["javascript", "typescript", "python"]) %>"
framework: "<% await tp.system.suggester(["React", "Next.js", "Astro", "TanStack", "None"], ["react", "nextjs", "astro", "tanstack", ""]) %>"
tools: "<% await tp.system.suggester(["shadcn", "tailwind", "motion", "threejs3d", "lerpa", "reui", "strapi", "wordpress", "payloadcms", "directus", "contentful", "sanity", "None"], ["shadcn", "tailwind", "motion", "threejs3d", "lerpa", "reui", "strapi", "wordpress", "payloadcms", "directus", "contentful", "sanity", ""]) %>"
---

# {{TITLE}}

> **Resumen:** {{summary}}

## Definición

{{VALUE:Write the definition}}

## ¿Por qué usar esto?

{{VALUE:Explain when and why}}

## Ejemplo de código

```{{language}}
// Write your code here
```
````

## Recursos

- Documentación oficial: (URL en texto plano)
- PDF: 80_Resources/pdfs/...
- Imagen: 81_Images/...

## Notas relacionadas

- [[]]