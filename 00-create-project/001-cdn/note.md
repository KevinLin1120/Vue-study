# Create a new project with CDN

## Concept

There are 2 ways to use cdn:

1. global build
2. ES module

## Steps

### Global build

1. [get cdn link](https://vuejs.org/guide/quick-start.html#using-vue-from-cdn) + paste it into html's **head**

2. use global **Vue object** to create app.

   ```html
   <head>
     ...
     <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
   </head>

   <body>
     <div id="app">{{ msg }}</div>

     <script>
       const { createApp } = Vue;

       createApp({
         data() {
           return {
             msg: "Hello, World",
           };
         },
       }).mount("#app");
     </script>
   </body>
   ```

### ES module

1. [copy es module link](https://vuejs.org/guide/quick-start.html#using-the-es-module-build)

   ```html
   <body>
     <div id="app">{{ msg }}</div>
     <!-- type must add!!! -->
     <script type="module">
       import { createApp } from "https://unpkg.com/vue@3/dist/vue.esm-browser.js";

       createApp({
         data() {
           return {
             msg: "Hello, world!",
           };
         },
       }).mount("#app");
     </script>
   </body>
   ```

## Notice

- This method CAN NOT use Single-File Component (SFC) syntax.

## global build v.s. ES module

|                  | global build                      | ES module                         |
| ---------------- | --------------------------------- | --------------------------------- |
| **import way**   | `<script src="...vue.global.js">` | `import { createApp } from 'vue'` |
| **browser need** | Works directly                    | Needs ESM support or bundler      |
| **scope**        | Global `Vue` variable             | Module variable (no global)       |
| **best for**     | Quick demo, small page            | Large, modular projects           |
| **tree-shaking** | ❌ No                             | ✅ Yes                            |

note:
**tree-shaking**: remove useless codes
