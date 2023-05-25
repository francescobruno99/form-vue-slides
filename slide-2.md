---
transition: slide-up #fade-out
layout: two-cols
---

::right::

<!-- # Aspetti positivi -->

<br><br><br><br><br><br>

- 🧑‍💻 **Developer Friendly** - you declare a validator once and Zod will automatically infer the static TypeScript type
- 📝 **Ts-Docs** - automatic documentation
- 🛠 **Easy to use** - bult-in validation rules
- ⚖️ **Zero dependencies** - tiny (8kb minified + zipped)

::default::

# Zod

[Zod](https://zod.dev) is a TypeScript-first schema declaration and validation library.

This is done using the **Zod Object**

```ts {none|all|1|3-13|15-16|all}
import { z } from "zod";

const role = ["user", "teacher", "admin"];

// creating a schema
const User = z.object({
  firstName: z.string(),
  lastName: z.string(),
  nickname: z.string(),
  age: z.number().int().min(18),
  email: z.string().email(),
  role: z.enum(role),
});

// extract the inferred type
type User = z.infer<typeof User>;
```

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(75deg, #27c57e 10%, #e6b457 40%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

.slidev-code {
    margin-right: 20px;
}
</style>

<!--
Zod è un è una libreria Typescript per la validazione degli "schema".
Nel nostro contesto usiamo Zod per validare i campi delle nostre form.
La validazione si costruisce attraverso lo Zod Object (vedi esempio rappresentato).

Abbiamo scelto di utilizzare Zod perché:
• semplice da utilizzare, molto intuitivo grazie a molte validazioni built-in
• utilizzato assieme a Typescript ci permette di documentare meglio il codice e di poter inferire il tipo
• non ha dipendenze interne ed il peso del pacchetto è veramente irrisorio
-->
