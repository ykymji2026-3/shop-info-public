# Small Salon Booking Site Portfolio

小規模サロン向けに制作した、Web予約導線つき店舗サイトのポートフォリオ版です。

この public repo はポートフォリオ公開用です。UI、画面設計、導入イメージ、技術構成のみを掲載し、実予約処理、管理画面、メール認証、Firebase / EmailJS の実装コードは含めていません。

## Target

- 個人サロン
- 美容室、ネイル、整体、リラクゼーションなどの小規模店舗
- LINE集客とWeb予約を分けて運用したい店舗
- 予約受付後に店舗側で確認してから確定したい事業者

## Public Files

```text
.
├── index.html
├── booking.html
├── style.css
├── booking.css
├── README.md
└── screenshots/
```

## Features

- 店舗紹介トップページ
- サービス・料金・アクセス情報
- Web予約フォームUI
- LINE公式アカウントへの集客・CRM導線
- クーポン配信、キャンペーン通知、空き情報案内の導線
- 予約ステータス管理を想定した設計

## Architecture

本体版では以下の技術を使用しています。

- Firebase Auth
- Firestore
- EmailJS
- verify認証
- 管理画面
- スパム対策
- HTML / CSS / JavaScript

## Spam Protection

本体版では、偽メールアドレスによる予約を減らすために、メール認証を前提とした予約受付フローを設計しています。

- 予約直後は未認証ステータスとして保存
- メール内の verify リンクで本人確認
- 認証済み予約のみ管理画面に表示
- reCAPTCHA に頼らず UX を大きく崩さない構成

## Not Included

以下は商品本体コードまたは運用情報にあたるため、この public repo には含めていません。

- APIキー
- Firebase設定
- EmailJS ID
- Firestore Rules全文
- booking.js
- admin / verify / cancel / login 関連コード
- Cloud Functions
- Firestore運用ロジック
- 実運用URL

## Future Improvements

- スクリーンショット追加
- 業種別テンプレート展開
- 店舗カラーのカスタマイズ項目追加
- 予約フォームUIの入力補助強化
- 管理画面の集計ビュー追加
- LINE配信施策のテンプレート化
