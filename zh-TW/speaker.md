# 如何連接喇叭

## 準備
* 首先，請準備一個 0.5W, 8 歐姆的喇叭
* 紅色線接在板子上的 SPA+, 地線接在 SPA-
* 以下是示意圖
![](https://relajet-co.gitbooks.io/relajet-c-series/content/assets/speaker.jpg)

## 測試
* 請先用電腦在 SD card 中放入 wav 音檔（假設放了這個 playback-test-EVA-AIR.wav)
* 將 SD card 插入，並上電
* 進去 Linux 主控的串口
* 輸入 `aplay -Dhw:0,0 /mnt/sdcard/playback-test-EVA-AIR.wav`
* 這時候喇叭聽到聲音即可代表串接成功

## 小秘訣

* 參照 pinmux 圖

![](https://relajet-co.gitbooks.io/relajet-c-series/content/assets/c-series-pinmux.png)
* 板子右邊的 pin 排的 SPA+, SPA- 接入都有一樣的效果