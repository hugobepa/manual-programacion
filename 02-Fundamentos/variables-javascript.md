
---
tags:
  - tipo/concepto
  - nivel/junior
  - lenguaje/javascript
fecha_creacion: 2026-04-06
---

# Variables en JavaScript

## 📝 Explicación Junior
Una variable es una **caja donde guardamos información** para usarla después. Como una etiqueta en una caja de mudanza.

## 💻 Ejemplo Código

### 👶 Junior (básico / "Funciona pero...")
```javascript
// Declaración con var (antiguo, evitar)
var nombre = "Juan";
var edad = 25;

// Cambiar valor
nombre = "Carlos";

// Imprimir
console.log(nombre); // "Carlos"
console.log("Hola " + nombre + ", tienes " + edad + " años");
```

### 👨‍ Senior (optimizado / Clean Code)
```javascript
// const por defecto (inmutable)
const NAME = "Juan";
let age = 25;

// let solo si cambia
age = 26;

// Template literals (más limpio)
console.log(`Name: ${NAME}, Age: ${age}`);
```

## 📊 Comparativa: var vs let vs const

| Keyword | Scope | Hoisting | Reasignable | Uso recomendado |
|---------|-------|----------|-------------|-----------------|
| `var` | Function | Sí | Sí | ❌ Evitar (legado) |
| `let` | Block | No | Sí | ✅ Cuando cambie el valor |
| `const` | Block | No | No | ✅ Por defecto (90% casos) |

## 🔗 Documentación Oficial
- [MDN - Variables](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Grammar_and_types#declaraciones)
- [MDN - let](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/let)
- [MDN - const](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/const)

## 🏷️ Tags
#lenguaje/javascript #tipo/concepto #nivel/junior