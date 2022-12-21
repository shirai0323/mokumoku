# README

## 環境構築
```
$ bundle install
$ bin/rails db:setup
$ yarn install
$ bin/rails s
```

## 事業をエンジニアリングしよう提案編の回答は以下に記述してください

## 選択した事業側の課題
サービス登録者数の内、男性60%に対して、女性は40%。一方で、サービス内のもくもく会に参加した人の比率は、男性90%：女性10%と大きな差が出ています。もっと女性が使いやすいようなサービス設計にする必要があるのではないか？

## 提案内容
登録時点では40%の女性が登録してくれているが、
・オフラインで情報の少ない異性と会う
・初学者や初めて利用しようする方にとって主催者や参加者の性別がわからない為不安(女性が自分だけかもしれない)
などと女性が安心してサービスを利用するにはハードルが高いため、
もくもく会への参加率が女性10%とという数字に出てしまっている。
その為、女性でも安心してサービスを利用できるように女性限定のもくもく会を開催＆参加できるようにする。

## 実装方針
- ユーザーモデルにgenderカラム(male,female)を追加し性別を選択できるようにする
- genderがfemaleのみ女性限定もくもく会を主催できるようにする
- genderがfemaleのみ女性限定もくもく会に参加できるようにする
  - genderがmaleの場合女性限定もくもく会に参加しようとすると「女性限定のもくもく会の為、参加できません」とフラッシュメッセージを表示する
