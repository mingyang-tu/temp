# 名詞解釋

- PPA (Power / Performance / Area)：衡量效能好壞的指標。

- line buffer：LCD 的畫面掃描是「由上而下、一列一列」進行的。當 TCON 在處理影像時，有些運算必須參考「上下相鄰像素」的資訊。此時，就要把其他行存進記憶體 (SRAM 或 DDR)，稱為 line buffer。

- register：通常指用來給別人調參數的記憶體。

- VRR (Variable Refresh Rate，可變更新率)：當螢幕更新率（FPS）改變時，顯示器的反應時間（Overdrive, OD）也需要調整，否則會出現殘影或過衝（Overshoot）。

- eDP (Embedded DisplayPort)：TCON 輸入的對接接口。
- PSR

- offline IP：需要其他 frame 存在 DDR 後續做處理的 IP。例如：overdrive, unwraping, 3DNR 等。
- inline IP：只就現有 frame 做處理的 IP。

- VESA（視訊電子標準協會, Video Electronics Standards Association）

- spatial smoothing / temporal smoothing：在空間域 / 時間域進行平滑處理。

- crosstalk：crosstalk 是指螢幕中某區域的畫面影響到鄰近區域亮度的現象。

## DSC（顯示串流壓縮 Display Stream Compression）

影像壓縮傳輸（Display Stream Compression）簡稱 DSC，是將影像數據壓縮後進行傳輸，達成低頻寬就可輸出高解析度內容，並且經壓縮後畫面表現上視覺無失真、低延遲的技術。

DSC 使用**預測編碼**以及建立**歷程顏色索引**來壓縮影像數據。
預測編碼概念上就是傳送端先利用周邊的像素資訊預測目標像素資訊，再將預測出來的像素資訊與原本的像素資訊進行運算，得出一個誤差值。這個誤差值作為數據傳送給接收端後，接收端執行同樣的步驟預測出目標像素並加上這個誤差值使其更接近原本的像素。如此一來就只需傳送誤差值，減少數據量。
歷程顏色索引原文為 Index Color History（ICH），就是將常出現的像素資訊儲存為索引。傳輸時僅需要索引數據，也不須傳輸大量資料，達成壓縮目的。ICH 適合用在圖形化的畫面或有大面積單一顏色的畫面上。
