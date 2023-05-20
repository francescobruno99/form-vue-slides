---
transition: fade-out
layout: two-cols
title: Right
---

::right::

<!-- # Aspetti positivi -->

<br><br><br><br><br><br>

- 🧑‍💻 **Developer Friendly** - si dichiara il validatore una sola volta e Zod inferirà automaticamente il tipo
- 📝 **Ts-Docs** - documenta automaticamente lo "schema"
- 🛠 **Easy to use** - offre moltissime regole di validazione built-in
- ⚖️ **Zero dependencies** - non necessita di alcun pacchetto

::default::

# Zod

[Zod](https://zod.dev) è una libreria Typescript per la validazione degli "schema".

Tutto ciò avviene mediante lo **Zod Object**

```ts {none|all|1|3-13|15-16|all}
import { z } from "zod";

const role = ["user", "teacher", "admin"];

// creating a schema
const User = z.object({
  firstName: z.string(),
  lastName: z.string(),
  nickname: z.string(),
  age: z.number().min(18),
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
