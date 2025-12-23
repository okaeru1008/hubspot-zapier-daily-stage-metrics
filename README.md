# hubspot-zapier-daily-stage-metrics


# HubSpot × Zapier 日次ステージ件数取得

## やりたいこと
- HubSpotのDealをステージ別に集計
- 毎日1回、Googleスプレッドシートに保存
- 縦：日付 / 横：ステージ / セル：件数

## 環境
- Zapier（UI新仕様）
- HubSpot（Deals）
- Google Sheets

## 今日やったこと（YYYY-MM-DD）
- Zapierで Schedule by Zapier をTriggerに設定
- HubSpot連携で以下を確認
  - Standard actions に Search / List Deals が出てこない
  - Find Deal は1件取得のみで用途に合わない
  - Custom actions (Beta) も環境的にうまく動かず

## 試したこと
- Find Deal → 不可（複数件取得できない）
- Search Deals → UIに表示されない
- List Deals → UIに表示されない
- Custom actions（List CRM Objects）→ 失敗

## 現在の結論
- Zapier標準UIではステージ別件数取得が困難
- 次回は以下を検討する
  - Webhooks by Zapier + HubSpot API
  - もしくは別集計手段（HubSpot側レポート / エクスポート）

## 次やること
- HubSpot Private App Token を発行
- Deal Stage ID を確認
- API経由で /crm/v3/objects/deals/search を叩く

## chatGPT
https://chatgpt.com/c/6949d59f-5404-8322-ae10-5b5683ec96d6
