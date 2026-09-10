# リズム読譜 — 横画面PWA版

元の `rhythm game_15.html` の機能・デザインを踏襲し、
ゲーム画面だけ横画面に最適化しています。

## 主な変更
- PWA化（manifest + Service Worker）
- PWAの推奨表示方向を landscape に設定
- 横画面では最大幅制限を解除
- 両手モードの右手ボタン：画面右下
- 両手モードの左手ボタン：画面左下
- 親指で押しやすい大きさ・角丸・下端配置
- 楽譜は中央〜上部を広く使用
- 元のBPM、レベル、10小節、音声、判定、結果、見直し、ベストスコア等は維持

## 起動
PWAのService Workerは `file://` では動かないため、HTTPSまたはlocalhostで配信してください。

例:
`python3 -m http.server 8000`

その後、同一端末のブラウザで `http://localhost:8000` を開きます。
本番PWAとして使う場合はHTTPSでホスティングしてください。
