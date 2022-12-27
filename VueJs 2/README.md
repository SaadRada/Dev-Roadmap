# VueJs 2

![vuejs 2](https://miro.medium.com/max/1400/1*IPTRjl2GyBeNrBnbvB714A.jpeg)

Vue (pronounced /vjuː/, like view) is a progressive framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable. The core library is focused on the view layer only, and is easy to pick up and integrate with other libraries or existing projects. On the other hand, Vue is also perfectly capable of powering sophisticated Single-Page Applications when used in combination with modern tooling and supporting libraries.

created by evan you on 2014

**Why Vue js?**

- Lightweight
- Virtual DOM
- Reusable Components
- Directives
- Event Hamdling
- Animations
- Watchers
- CLI
- Routing
- Unit Testing with CLI
- Mixins

## create project

- intall vue js
  ```
  npm install vue
  ```
- create vue project

  ```
  vue create app-name
  ```

## Vue Instance

```
var app = new Vue({
  el: '#app',
  data: {
    name: 'Rada Saad',
    isSalary: true,
    age: 21,
    html: '<h1>Big Text</h1>'
  },
  methods: {
    sayHello() {
      return 'Hello'
    }
  }
})
```

## Directives

- **v-text**
  Updates the element’s textContent. If you need to update the part of textContent, you should use {{ Mustache }} interpolations.
  ```
  <span v-text="msg"></span>
  <!-- same as -->
  <span>{{msg}}</span>
  ```
- **v-html**
  Updates the element’s innerHTML. Note that the contents are inserted as plain HTML - they will not be compiled as Vue templates. If you find yourself trying to compose templates using v-html, try to rethink the solution by using components instead.
  ```
  <div v-html="html"></div> // Big Text with h1 element style
  ```
