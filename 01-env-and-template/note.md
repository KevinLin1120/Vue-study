# 00 Vue

## Why 2nd choice?

- 可切檔案用

## Why `;()` ?

- 當程式跟別的程式放在一起，就會壞掉，所以加上 `;`

## Vue 模板來自哪？

- Mustache 模板系統

## 如果怕 Vue 未載入成功時，顯示 template `{{}}`

- 在 el 加入 `v-clock` attribute

- css 加入 `[v-clock] {display: none;}`，Vue 正式啟動後，會把該 attr 拔掉

## 引入 Vue 至舊專案的步驟

1. 資料寫在 js / html

2. 資料寫在 json

3. 資料開發 api
