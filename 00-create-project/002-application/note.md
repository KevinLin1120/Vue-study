# Create a new application project with **vite**

## Create project

1. open the terminal and type `npm create vue[@latest] APP-NAME`

2. Select features to include in your project

   ![](./note%20imgs/application%20options.png)

3. Select experimental features to include in your project

   ![](./note%20imgs/optoinal%20options.png)

   Note: this is **totally optional**

4. DONE!

## Start the app

1. cd to the proj root directory

2. `npm install` to get all package we need

3. use `npm run dev` (ref in package.json)

4. go into the url: [link](localhost:5173)

   Note: ref from

5. DONE!

### Change server port

In **vite.config.js**, add server setting config

```JavaScript
...
export default defineConfig({
  plugins: [
    ...
  ],
  resolve: {
    ...
  },
  server: {
    host: true, // or '0.0.0.0' -> Let local network other devices can access
    port: 8080,
  }
})
```

note: server post is default **5173**

## Project Structure

```text
my-vue-app/
├── node_modules/
├── public/
│   └── favicon.ico
├── src/
│   ├── assets/
│   ├── components/         # 可重用元件
│   ├── views/              # 路由頁面元件
│   │   ├── Home.vue
│   │   ├── About.vue
│   │   └── NotFound.vue
│   ├── router/             # 路由設定
│   │   └── index.js        # router 實例和路由規則
│   ├── App.vue
│   └── main.js
├── .gitignore
├── index.html
├── package.json
├── vite.config.js
└── README.md

```
