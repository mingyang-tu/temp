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
