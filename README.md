# 【Unity】Visualize-Electric-Field
👇 youtube link<br>
<kbd><a href="http://www.youtube.com/watch?v=HrMNcW8Fh9E" target=_blank><img src="https://img.youtube.com/vi/HrMNcW8Fh9E/maxresdefault.jpg" width="700" style="border:2px #ccc solid;padding:5px;"></a></kbd><br> 
# 一、操作
<img src="/picture/configuration.png" width="375" /><br>
打開 ```electric_line.bat``` (勾windows以不進入全螢幕)並單擊play開始<br>
若捷徑無法打開，請至資料夾點 ```.\certification\electtric_line.exe``` <br>

上下左右鍵：可控制右邊電荷位置<br>
backspace鍵：右邊電荷回到原點<br>
單擊電荷按鈕：可改變電荷量(+9e~-9e)<br>
中間橫桿：控制產生電力線的間距(delta distance)<br>
自動刷新：靜待約十秒將自動刷新<br>
escape鍵：退出遊戲(可能有延遲<br>

# 二、設計&問題

### 橫桿設計<br>
在最初的版本是將產生間距調成一點零，但發現有些較相近的兩電荷量<br>
(如-2e,+3e時)，會產生重疊的問題，因為課本使用的方法誤差會累積的<br>
，為消除誤差，所以設計了橫桿，調至越左邊將獲得越精確的圖形。<br>

### 負電荷問題<br>
當設計負電荷時，因為電力線原本會從無線遠處指向電荷，但若從無限遠<br>
指向電荷會造成電荷密度不均勻的問題，所以折衷作法是將電力線反著射<br>
出，在間距夠近時兩者會近似，但如果間距過大時，因為a點的電場指向b<br>
點，不代表b點的電場會指向a點，所以畫出來的圖挳能會不精確。<br>

### 相同電荷不對稱現象<br>
因為當兩電荷相異(+1e,-1e)時，如果相同角度下發射兩條線會重疊，所以<br>
設計時將兩電荷差了15度的角度(electron1:0,30,60..,eletron2:15,45,75...)<br>
，所以在電性相同時(-1e,-1e)時，兩者不對稱時屬正常現象。<br>

# 三、鍵盤&滑鼠偵測
左下方的鍵盤滑鼠偵測是使用python做的<br>
程式碼也附在 ```/mouse_keyboard_detector``` 裡<br><br>
<kbd><img src="/picture/detector.png" width="375" /></kbd>
