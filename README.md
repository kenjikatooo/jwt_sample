# README

## 使用している技術

```
ruby 2.5.1
rails ~> 5.2.2
mysql
```

## 環境構築

```
$ git clone git@github.com:kenjikatooo/jwt_sample.git
$ cd jwt_sample
$ bundle
$ rails db:create db:migrate db;seed
```

## 使い方

- POST /user_token 
  - POSTMAN（またはcurlコマンド）を使ってユーザーのjwtが返ってくることを確認する
  - postするjsonの例は、以下の通り
```
{"auth": {
	"email":"test@user.com",
	"password":"test123"
	}
}
```

- GET /posts
  - ログインしている状態でデータを取得できることをテストする
  - get する際は Bearer Token に先ほどのPOSTで取得したユーザーのtokenを代入する
  - 代入することでデータが取得できるようになる
  - 完成例は以下の通り
  - https://gyazo.com/e6a36d741de50104f8cd8b3e05868582
  
