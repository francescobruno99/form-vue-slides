---
transition: slide-up
---

# Form-vue elements

<!-- Sono quattro i componenti che abbiamo creato per poter sviluppare una form in Vue -->

|                                                                                                 |                             |
| ----------------------------------------------------------------------------------------------- | --------------------------- |
| <kbd>[VvForm](https://github.com/volverjs/form-vue#vvform)</kbd>                                | ```<form>``` tag            |
| <kbd>[VvFormWrapper](https://github.com/volverjs/form-vue#vvformwrapper)</kbd>                  | ```<fieldset>``` tag        |
| <kbd>[VvFormField](https://github.com/volverjs/form-vue/blob/develop/docs/VvFormField.md)</kbd> | ```<input>``` tag           |
| <kbd>[VvFormTemplate](https://github.com/volverjs/form-vue#vvformtemplate)</kbd>                | JSON schema                 |

```html{none|all}
<form id="signIn">
  <fieldset>
    <legend>Your credentials</legend>
    <label for="username">Username</label>
    <input id="username" name="username" type="text" placeholder="Username" required autofocus>
    <label for="email">Email</label>
    <input id="email" name="email" type="email" placeholder="example@domain.com" required>
    <button type=submit>Sign In</button>
  </fieldset>
</form>
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
</style>

<!--
insert comment here!
-->
