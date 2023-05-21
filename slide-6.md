---
transition: slide-up
---

# VvFormWrapper

VvFormWrapper gives you the validation status of a part of your form. The wrapper status is invalid if at least one of the fields inside it is invalid.
VvFormWrapper can be used recursively to create a validation tree. The wrapper status is invalid if at least one of the fields inside it or one of its children is invalid.

<div grid="~ cols-2 gap-4">

```vue
<template>
  <VvForm>
    <VvFormWrapper v-slot="{ invalid }">
      <div class="form-section-1">
        <span v-if="invalid">Validation error</span>
        <!-- form fields of section 1 -->
      </div>
    </VvFormWrapper>
    <VvFormWrapper v-slot="{ invalid }">
      <div class="form-section-2">
        <span v-if="invalid">Validation error</span>
        <!-- form fields of the section 2 -->
      </div>
    </VvFormWrapper>
  </VvForm>
</template>
```

```vue
<template>
  <VvForm>
    <VvFormWrapper v-slot="{ invalid }">
      <div class="form-section">
        <span v-if="invalid">Validation error</span>
        <!-- form fields of section -->
        <VvFormWrapper v-slot="{ invalid: groupInvalid }">
          <div class="form-section__group">
            <span v-if="groupInvalid">Validation error</span>
            <!-- form fields of the group -->
          </div>
        </VvFormWrapper>
      </div>
    </VvFormWrapper>
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
insert comment here!
-->
