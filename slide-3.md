---
transition: slide-up
preload: false
---

# Form HTML

<img v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }" src="/assets/form-sample.png" class="img-form-sample my-5 m-auto" >

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

.img-form-sample {
  border-radius: var(--slidev-code-radius) !important;
}
</style>

<!--
insert comment here!
-->
