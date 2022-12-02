# 対象の機能

- ユーザを表示する
- ツイートする
- ツイートに返信する
- リツイートする(引用リツイートも)
- フォローする
- フォロー一覧を表示する
- フォロワー一覧を表示する
- リストにユーザーを追加する
- リスト一覧を表示する

# ER図
<img width="916" alt="twitter_erd_v2" src="https://raw.githubusercontent.com/inoway46/twitter_erd/8f5e07d269437532737e5ebf1be6943398aa5e35/twitter_erd_v3.png">

# 補足説明

## 各ツイートタイプのレコード内容
- ツイート
  - tweet_type = 'tweet'
  - reacted_tweet_id = null
  - content = ツイート内容

- リプライ
  - tweet_type = 'reply'
  - reacted_tweet_id = id(返信先)
  - content = リプライ内容

- リツイート
  - tweet_type = 'retweet'
  - reacted_tweet_id = id(元ツイート)
  - content = null

- 引用リツイート
  - tweet_type = 'retweet'
  - reacted_tweet_id = id(元ツイート)
  - content = 引用者のツイート内容
