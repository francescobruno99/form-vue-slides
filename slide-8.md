---
transition: slide-up
---

# VvFormTemplate

Forms can also be created using a template. A template is an array of objects that describes the form fields. All properties that are not listed below are passed to the component as props.

<div grid="~ cols-2 gap-4">

```vue
<script lang="ts" setup>
import { useForm } from "@volverjs/form-vue";
import { z } from "zod";
import templateSchema from "./schema";

const schema = z.object({
  username: z.string(),
  email: z.string().email(),
});

const { VvForm, VvFormTemplate } = useForm(schema);
</script>

<template>
  <VvForm>
    <VvFormTemplate :schema="templateSchema" />
  </VvForm>
</template>
```

<div>

```js
export const templateSchema = [
  {
    vvName: "username",
    vvType: "text",
    label: "Username"
  },
  {
    vvName: "email",
    vvType: "text",
    label: "Email"
  }
];
```

<div grid="~ cols-3" class="pa-2" style="font-size: 1rem;">
  <div>
    <ul>
      <li>vvName</li>
      <li>vvType</li>
      <li>vvIs</li>
    </ul>
  </div>
  <div>
    <ul>
      <li>vvIf</li>
      <li>vvElseIf</li>
      <li>vvSlots</li>
    </ul>
  </div>
  <div>
    <ul>
      <li>vvChildren</li>
      <li>vvDefaultValue</li>
      <li>vvShowValid</li>
    </ul>
  </div>
</div>

</div>

</div>

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
</style>

<!--
insert comment here!
-->
