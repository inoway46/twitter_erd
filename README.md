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
<img width="865" alt="twitter_erd_v1" src="https://user-images.githubusercontent.com/65857152/202978254-8aba20c5-f1b5-4156-9495-fbb1c55f45c7.png">

# 補足説明

- 引用リツイート
  - Retweetテーブルの`content`カラムで判別
    - nullの場合: リツイート
    - not nullの場合: 引用リツイート
