# Run 一隻 hello world 程式

Ps. 本篇以 Node.js 為教學範例，日後會補上 python, C

### 步驟
- 請下載 RelaJet 編譯好的 Node.js binary
- 請將 node10 放進 SD card
- 上電
- `cd /mnt/sdcard/` -> 打開 SD card 根目錄
- `touch app.js` -> 創建 app.js 檔案
- `vi app.js` -> 編輯 app.js
- 按下 i , 並輸入 `console.log('hello world')`
- 按下 :wq! -> 存檔並離開
- `node app.js` -> 啟動 Node.js app
- 這時候就會看到 `hello world` 即大功告成!