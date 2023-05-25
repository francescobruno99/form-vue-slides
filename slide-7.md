---
transition: slide-up
---

# VvFormField

<p>
  <div>VvFormField allow you to render a form field or a @volverjs/ui-vue input component inside a form.</div>
  <div>It automatically bind the form data through the name attribute. For nested objects, use the name attribute with dot notation.</div>
  <div>To render a @volverjs/ui-vue input component, use the type attribute.</div>
</p>

<div grid="~ cols-2 gap-4">

```vue
<script lang="ts" setup>
const onSubmit = (formData) => {
  // ...
};
const onInvalid = (errors) => {
  // ...
};
</script>

<template>
  <VvForm @submit="onSubmit" @invalid="onInvalid">
    <VvFormField type="text" name="username" label="Username" />
    <VvFormField type="text" name="email" label="Email" />
    <VvButton icon="SignIn" label="Sign in" type="submit" />
  </VvForm>
</template>
```

| <em>input type="..."</em>                               | <em>UI-Vue component</em> |
| ------------------------------------------------------- | ------------------------- |
| <kbd>text</kbd> / <kbd>tel</kbd> / <kbd>url</kbd> / ... | <kbd>VvInputText</kbd>    |
| <kbd>select</kbd>                                       | <kbd>VvSelect</kbd>       |
| <kbd>checkbox</kbd>                                     | <kbd>VvCheckbox</kbd>     |
| <kbd>radio</kbd>                                        | <kbd>VvRadio</kbd>        |
| <kbd>textarea</kbd>                                     | <kbd>VvTextarea</kbd>     |
| <kbd>combobox</kbd>                                     | <kbd>VvCombobox</kbd>     |

</div>

<style>
h1, th {
  background-color: #2B90B6;
  background-image: linear-gradient(75deg, #27c57e 10%, #e6b457 40%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

td, th {
  padding: 0px !important;
}
</style>

<!--
VvFormField serve per creare i campi di input della form di compilazione.
In questo esempio l'attributo type di VvFormField identifica il tipo di campo di cui abbiamo bisogno.
-->
