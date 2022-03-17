# README

## 環境構築手順

### 共通

```
$ git clone git@github.com:miwa0519/sample-react-rails-todo.git
$ cd react-rails-todo
$ mkdir -p projects
$ cd projects
$ git clone git@github.com:miwa0519/sample-todo-backend.git
$ git clone git@github.com:miwa0519/sample-todo-frontend.git
```

### Docker

```
# 当リポジトリで実行
$ docker-compose build
$ npm run dc-setup
$ npm run db-setup
$ npm run dc-up
```

### local

```
$ brew install postgresql
$ cd project/todo-backend
$ bundle install --path=vendor/bundle
$ bundle exec rails db:create
$ bundle exec rails db:migrate
$ bundle exec rails db:migrate:reset && back bundle exec rails db:seed
$ cd ../todo-frontend
$ npm install
$ cd ../../
$ npm run start
```
