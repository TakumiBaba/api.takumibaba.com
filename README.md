API server for communiating with baba
=======

http://api.takumibaba.com/

## 概要

Babascript の API 版に近いもの
人に対して簡単にアクセスできるような仕組み
そのメディエータとなるようなWebサービスとして。
hubotとかで作ってしまいたい
が、viewが必要になりそうな要素もあるので...

## function

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
- アマゾンで何かを届ける
- 電話する
  - Twillio 使ったり

- http request
- websocket
- 認証状況に応じて、得られる情報が異なる
  - facebook友達なら、電話番号も得られるとか

## Implementation

- node.js
- with express

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

- /call
  - GET
    -  query
    -  from
  - POST

- /status
  - GET
    - request
      - query...

- /etc
  - TBD


## call

voice call service wih takumi baba

##  README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
