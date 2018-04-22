# Windows

在Windows系統下運行Relajet C series需要安裝PuttY及cp210X driver。

### [下載Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

### [下載cp210X driver](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)

## 設置PuttY

1. 打開**裝置管理員**

2. 點開**連接阜\(COM和LPT\)**

3. 記下兩組**COM**![](https://relajet-co.gitbooks.io/relajet-c-series/content/assets/裝置管理員1.PNG)

4. 打開**PuttY**

5. 在**Connection type**欄位選取**Serial**

6. 在**Serial line**輸入方才記下的第一組**COM**

7. 在**Speed**欄位輸入**115200**

8. 點選**Open
   **![](https://relajet-co.gitbooks.io/relajet-c-series/content/assets/putty.PNG)

9. 打開**PuttY**重複設定第二組**COM**

設定完後按下enter出現\#字號的這一組為主控組，出現$字號的為Wifi組。

![](https://relajet-co.gitbooks.io/relajet-c-series/content/assets/#字號為主控組.png)

## 設置Wifi

1. 打開主控組\(Wifi組無須理會\)
2. 輸入
   `iot-tool -s 您的Wifi或熱點名稱 -p 您的Wifi或熱點密碼 -a 8 -e 9`
   其中特別注意的是熱點名稱及密碼中不可含有空格或標點符號。
   圖中熱點名稱以timexeexe，熱點密碼以00000000為例。
   ![](https://relajet-co.gitbooks.io/relajet-c-series/content/assets/輸入iot-tool -s 您的Wifi或熱點名稱 -p 您的Wifi或熱點密碼 -a 8 -e 9.PNG)

3. 拔除USB線並重新插入

4. 點擊右鍵執行**Restart session**
   ![](https://relajet-co.gitbooks.io/relajet-c-series/content/assets/Restart session.png)

## 確認C series IP

1. 輸入`ifconfig`** **
2. 紅
   框處IP位址依所連結之裝置不同應如以下

   * iphone熱點:172.20.10.X

   * android熱點或一般路由器:192.168.X.X

   ![](https://relajet-co.gitbooks.io/relajet-c-series/content/assets/ifconfig.PNG)

## 確認本機IP

1. 打開**命令提示字元**
2. 輸入ipconfig，記下紅框中本機IP位置
   ![](/assets/Ipconfig.png)

## 影像指令

1. 打開Relajet應用程式
2. 打開主控組
3. 輸入`/usr/bin/ffmpeg -livestream 3 -noaudio 1 -r 30 -s 1024*768 -f v4l2x -input_format h264 -vbrate 2500000 -i /dev/video0 -copyinkf -c:v copy -b:v 2500000 -g 1 -f flv rtmp://您的本機IP位置/deviceId/SkIeHXBuW/deviceKey/573b3badca6b582a03fab9a955c2d04e6f07981114c4a541dddea86c7598c814/stream`
   圖中紅框以**172.10.20.8**為例
   ![](/assets/影像控制.png)

# Enjoy your Relajet C series！

**
**

##

##



