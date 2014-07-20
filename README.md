BabaAPI
=======

http://api.takumibaba.com/

## 概要

Babascript の API 版に近いもの
人に対して簡単にアクセスできるような仕組み
そのメディエータとなるようなWebサービスとして。
hubotとかで作ってしまいたい
が、viewが必要になりそうな要素もあるので...

## できること(予定)

- 基本情報を得る
  - 電話番号
  - メールアドレス
  - etc..
- 状態をゲットする
  - 何してるか
  - 寝てるか起きてるか
- 何か行動させる
  - 〇〇やれ
- メッセージを送る
  - twitter
  - メール
  - チャット
  - etc...
- 金を送る
  - Web Pay 的な
  - 
- アマゾンで何かを届ける
- 電話する
  - Twillio 使ったりする
- baba が持つコンピュータリソースを使う？

- http request
- websocket
- 認証状況に応じて、得られる情報が異なる
  - facebook友達なら、電話番号も得られるとか


## Routing

- /message
  - GET (receive message)
    - request
      - query
        - id
    - response
      - text
  - POST(send message)
    - request
      - body
        - text
        - from
    - response
      - id
      - createdAt

- /phone
  - GET
  - POST

- /status
  - GET
    - request
      - query...

- /etc
  - TBD
  
