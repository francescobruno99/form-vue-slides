---
transition: slide-up
---

# VvForm

<p>
  <div>VvForm render a form tag and emit a submit event.</div>
  <div>Form data are validated on submit.</div>
  <div>A valid or invalid event is emitted when the form status changes.</div>
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
    <!-- ... -->
    <button type="submit">Submit</button>
  </VvForm>
</template>
```

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
VvForm serve per creare il tag form ed emettere gli eventi di invio o di errori nella validazione.
-->
