## 統整助教的回饋與修正紀錄

***

📌 --- `label for` & `input id` 互相對應，和 `v-for` 的 `key` 一樣很容易被遺忘，下次記得檢查補上

📌 --- `key` 值的首選是可以區別每筆資料**獨一無二的值**，若有 `id` 可用就以 `id` 優先

📌 --- 登入按鈕的 disabled 切換方式，除了用 ref 操控元素之外，也可以嘗試透過資料狀態驅動它

但是**不建議共用資料狀態**

比方說在 [ab1b186](https://github.com/QuantumParrot/2023-Hexschool-Vue-Live-Weekly-Task-02/commit/ab1b1864cd922035353e077d7147bb4bd9f23019) 的修改記錄裡，我讓登入按鈕與 Loader 共用 isLoading

只是在這次的作業裡剛好可行，將來可能會遇到更複雜的邏輯處理，獨立設置資料狀態會比較理想

📌 --- 在根元件的生命週期 `mounted` 裡接了兩支 API：驗證登入＆取得資料

邏輯上它們是有先後順序的，必須先驗證登入成功，才能取得產品的資料

因此會建議 `getProductData()` 寫在 `checkStatus()` 裡，當驗證結果回傳並綁定表頭之後再來呼叫下一個 API

***

最後更新：2023.01.11

