# README

## 環境構築（初回のみ）
```
docker-compose build
docker-compose run web rails db:create
docker-compose run web rails db:migrate
```

## 開発サーバー立ち上げ
```
docker-compose up
```
をした状態で http://localhost:3000/

## 開発中の操作
docker-compose upしていない場合はexecをrunに置き換え
### Gemfile追加
```
docker-compose exec web bundle install
```
### DBリセット
```
docker-compose exec web rails db:migrate:reset
```
