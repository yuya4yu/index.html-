[README.txt](https://github.com/user-attachments/files/26392499/README.txt)
# Google Sheets 用 完全版セットアップ

## 含まれるファイル
- `Code.gs`
- `Index.html`
- `appsscript.json`

## 使い方
1. 保存先にしたい **Google Sheets** を開く
2. **拡張機能 → Apps Script** を開く
3. 既存の `Code.gs` をこの `Code.gs` に置き換える
4. `+` から **HTML** ファイルを追加して名前を `Index` にし、この `Index.html` を貼り付ける
5. **プロジェクト設定** で **appsscript.json マニフェストを表示** を ON にする
6. `appsscript.json` の内容をこのファイルで置き換える
7. 保存する
8. Apps Script 画面で `initializeStorage` を一度実行して権限承認する
9. Google Sheets に戻って再読み込みする
10. メニューの **SVチェック表 → サイドバーを開く** を押す

## 保存の仕組み
- チェック結果・メモは `SVチェック記録` シートへ1行ずつ保存
- 同じ **記録ID** のまま送信すると、その行を上書き更新
- 画像は Google Drive の専用フォルダへ保存
- シートには画像URLも保存

## 補足
- `CONFIG.SPREADSHEET_ID` は通常空欄のままでOKです
- このスクリプトは **Google Sheets に紐づく Apps Script** として使う想定です
- 画像が非常に多い場合は Apps Script の実行時間や容量制限に当たることがあります
