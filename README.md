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
<img width="916" alt="twitter_erd_v2" src="https://user-images.githubusercontent.com/65857152/202984148-d762cbb2-ec2c-432e-aa95-0f20624ee094.png">

# 補足説明

- 引用リツイート
  - Retweetテーブルの`content`カラムで判別
    - nullの場合: リツイート
    - not nullの場合: 引用リツイート
