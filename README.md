# AI BUSINESS OWNER LP（再現＋改修版）

元ネタ：`~/Desktop/AIで事業を作る・自動化する・売却する｜無料オンライン講座.pdf`
表示スタイル参考：https://deploy-ai-hitorikigyou-v2.vercel.app

## 構成
- `index.html` … LP本体（CSSインライン、JSなし）
- `images/`
  - `silver-play-button.jpg` … 銀の盾（PDFの合成画像から切り出し）
  - `youtube-analytics.jpg` … YouTubeアナリティクス（同上）
  - `voice-01-line-stamp.png` / `voice-02-coconala.png` / `voice-04-game.png`
    … 実践者の報告LINE画面（見出し文字を焼き込んでいた上部をトリミング済み）
  - `fv-thumb.jpg` … FVモックアップのPC画面に映す背景（参考LPから取得。枠が中央に来るよう1200×764に再構成／タイトル文字はHTML側で重ねている）
  - `phone-bg.jpg` … FVモックアップのスマホ画面の背景（同画像の無地テクスチャ部分を切り出し）
  - `suya.jpg` … 講師写真（参考LPから取得）
  - `_unused/` … 削除した「今の暮らし」セクションの画像3点

## セクション（上から）
FV＋CTA → なぜAIで事業を作ると自由を目指せるのか → AIで事業を作った結果 →
同じ考え方を実践した方の結果 → 無料講義でわかること＋CTA → 講師プロフィール →
ラストCTA → フッター

## 参考LPから取り込んだ表示ルール
- 見出し `.h2` … 濃いインク色＋teal 3pxアンダーライン（`<em>`で囲んだ範囲）
- 実績/実践者の結果 `.rs` … 左teal罫のグループ見出し＋「ラベル｜右に大きな数字」の行、
  画像は枠付き figure ＋ グレーの figcaption
- 講師プロフィール `.pf` … 写真（100×125）＋肩書→名前→タグの横並び＋teal 3px下線、
  紹介文2段落、`PROFILE` 箇条書き8項目。文章・肩書・写真は参考LPと同一
- フッター … `#2B2B2B` 背景／`#BBB` テキスト／下線リンク
- FVビジュアル `.mock` … ノートPC＋スマホのモックアップ。筐体・スタンド・スマホは
  すべてCSSで描画（画像はPC画面の中身のみ）
- CTA `.btn` … padding 17px・角丸9px・`box-shadow: 0 5px 0 #049E44`（縦幅を圧縮）
  グレーの `.entry` ボックスに入れる（補足文は非表示）

## 要差し替え
- CTAボタン3か所の `href="#"` → LINE公式アカウントの友だち追加URL

## 設定済みリンク
- 特商法 … https://xenomagic.com/tokushoho.html
- プライバシーポリシー … https://xenomagic.com/privacy.html

## 公開URL
https://kumokawa1105-alt.github.io/ai-business-owner-lp/

リポジトリ: https://github.com/kumokawa1105-alt/ai-business-owner-lp （Public / GitHub Pages）

## 確認
```
open index.html          # ローカル
```

## 修正を公開に反映する
```
git add -A
git commit -m "修正内容"
git push
```
push の約1分後に公開URLへ自動反映されます（GitHub Actions の pages build が走る）。
ブラウザにキャッシュが残る場合は スーパーリロード（Cmd+Shift+R）。
