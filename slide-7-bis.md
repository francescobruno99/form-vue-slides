---
transition: slide-up
---

# VvFormField custom

<div grid="~ cols-2 gap-4">

```vue
<template>
  <VvForm>
    <VvFormField
      v-slot="{ ... }"
      name="username"
    >
      <label for="username">Username</label>
      <input
        id="username"
        type="text"
        :value="modelValue"
        :aria-invalid="invalid"
        :aria-errormessage="invalid ? 'username-alert' : undefined"
        @input="onUpdate"
      />
      <small v-if="invalid" role="alert" id="username-alert">
        {{ invalidLabel }}
      </small>
    </VvFormField>
  </VvForm>
</template>
```

- modelValue: <em>field model value</em>
- onUpdate: <em>field update function</em>
- errors: <em>field errors</em>
- invalid: <em>field is invalid</em>
- invalidLabel: <em>field validation errors (string[])</em>
- formData: <em>form data</em>
- formErrors: <em>form errors</em>

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
VvFormField custom
-->
