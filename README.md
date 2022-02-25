# アプリケーション名
Fight Club（仮）

# アプリケーション概要
格闘技関連のYouTube動画に個人的な見どころを添えて投稿する。

トップページではYouTube動画を埋め込み、見どころの文章とともに一覧表示する。

# URL
準備中…

# テスト用アカウント
準備中…

# 利用方法
- アカウントを作成する
- 投稿画面から、投稿したいYouTubeのURLを記載、それに対する見どころなどを記述し、投稿ボタンを押す。

# 目指した課題解決	
格闘技に興味はあるが、身近に話せる人がいない方に向けて交流の場を提供する。

# 洗い出した要件	
- ユーザー登録、ログイン機能(devise)
- ユーザ編集機能
- ゲストログイン機能
- 動画共有機能
  - URL投稿機能
  - 文章投稿機能
  - 複数タグ付機能
- 投稿編集機能
- 投稿削除機能
- YouTube埋め込み表示機能
- 投稿詳細表示機能
- いいね機能
  - いいね数表示機能
  - いいね数ランキング機能
- コメント機能
  - コメント数表示機能
- フォロー機能
  - フォロー一覧機能
  - フォロワー一覧機能
- 通知機能
  - コメント通知
  - フォロー通知
  - いいね通知
- レスポンシブ対応

# 実装した機能についての画像やGIFおよびその説明
準備中…

# 実装予定の機能
- ゲストログイン機能
- いいね機能
- フォロー機能

# テーブル設計

## users テーブル

| Column             | Type   | Options                   |
| ------------------ | ------ | ------------------------- |
| nickname           | string | null: false               |
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false               |
| date_of_birth      | date   | null: false               |

### Association

- has_many :items
- has_many :orders

## items テーブル

| Column             | Type       | Options                        |
| ------------------ | ---------- | ------------------------------ |
| title              | string     | null: false                    |
| description        | text       | null: false                    |
| category_id        | integer    | null: false                    |
| condition_id       | integer    | null: false                    |
| delivery_charge_id | integer    | null: false                    |
| prefecture_id      | integer    | null: false                    |
| days_to_ship_id    | integer    | null: false                    |
| price              | integer    | null: false                    |
| user               | references | null: false, foreign_key: true |

### Association

- belongs_to :user

# ローカルでの動作方法
準備中…