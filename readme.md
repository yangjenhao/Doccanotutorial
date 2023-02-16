# Doccano 使用
> [name=JenHao]

> [time=Mon, Dec 26, 2022 4:21 PM]

> screen -r doccano
> screen -r doccanotask
---
套件官網 [https://github.com/doccano/doccano](https://)
## 安裝Python環境(環境版本可參考官網提供的)
1.
```
conda create -n doccano python=3.8
```
2.
```
conda activate doccano
```
## 安裝doccano
3.
```
pip install doccano
```
## 終端初始化doccano並且創建管理員用戶
4.
```
doccano init
# 設置管理員帳號密碼 帳號：admin 密碼：pass
doccano createuser --username admin --password pass
```
## 啟動服務 (在一個窗口啟動doccano的WebServer，保持窗口)
5.
```
# port自行設置 不要同樣，好了之後點網址
doccano webserver --port yourport_name

#yourport_name : 8000 or other
```
## 然後保持上面終端，再打開一个新的終端，進入doccano的python環境，並且輸入以下啟用任務：
6.
```
(在另一個窗口啟動doccano的任務隊列)
doccano task
```
## 進入第5步驟的網址會長這樣
7. 點右上角login
![](https://i.imgur.com/W1UrxJn.png)
8. 輸入自己設置的帳號密碼
![](https://i.imgur.com/ZWffBjz.png)
9. 登入後長這樣，點擊Create
![](https://i.imgur.com/7AKAd5P.png)
10. 選擇你要的NLP任務
![](https://i.imgur.com/gkkIO0I.png)
11. 創建好可以自行看說明書，自己摸索
![](https://i.imgur.com/DqLKYW0.png)



---
導入數據。在Datasets一欄點擊Actions、Import Dataset從文件導入文本數據。

根據文件格式（File format）給出的示例，選擇適合的格式導入自定義數據文件。
導入成功後即跳轉至數據列表。
標註數據。點擊每條數據最右邊的Annotate按鈕開始標記。標記頁面右側的標籤類型（Label Types）開關可在實體標籤和關係標籤之間切換。

實體標註：直接用鼠標選取文本即可標註實體。
關係標註：首先點擊待標註的關係標籤，接著依次點擊相應的頭尾實體可完成關係標註。
導出數據。在Datasets一欄點擊Actions、Export Dataset導出已標註的數據。
## Note.加入新標註人員
```
http://localhost:yourport_name/admin/

#yourport_name : 8000 or other
```

## ref web
```
https://blog.csdn.net/yaohaishen/article/details/125788735
```