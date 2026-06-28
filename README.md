# Auto Send

點下連結之後就可以在 LINE 當前的聊天室發送指定訊息。

## 1. 準備要傳送的文字

先準備好你想讓別人自動送出的文字，例如：

```txt
完全法克
```

## 2. 將文字轉成 Base64

把去任何可以把文字轉換成Base64的網站，例如https://www.base64encode.org/ ，將文字轉換成Base64

轉成 Base64 後是這樣：

```txt
5a6M5YWo5rOV5YWL
```

## 3. 將 Base64 放進網址參數

把 Base64 內容放到網址的 `msg` 參數中。

格式：

```txt
https://liff.line.me/2010525282-22yCgSgG/?msg=Base64內容
```

範例：

```txt
https://liff.line.me/2010525282-22yCgSgG/?msg=5a6M5YWo5rOV5YWL
```

## 4. 從 LINE 聊天室開啟連結

將產生好的 LIFF 連結貼到 LINE 聊天室中，並~~騙人~~從 LINE 裡面開啟。

例如 :
```txt
免費貼圖按此領取⬇
https://liff.line.me/2010525282-22yCgSgG/?msg=5a6M5YWo5rOV5YWL
```
開啟後會自動執行：

```txt
讀取 msg 參數
↓
Base64 解碼
↓
傳送文字訊息到目前聊天室
↓
關閉 LIFF 視窗
```

## 5. 注意 Base64 特殊字元

Base64 可能包含以下字元：

```txt
+
/
=
```

雖然有做轉換了，但不確定有沒有缺漏特殊符號。

所以建議先測試一下會不會傳出亂碼，不會的話再拿去騙人。

## 6. 注意事項

如果網址中沒有 `msg` 參數，頁面不會傳送任何訊息，會被人發現，所以請小心。
