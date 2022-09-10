# RDB関連
## 開発用としてインストール ORM(Object-Relational Mapping)
npm install -D sequelize-cli
## 初期化
npx sequelize-cli init
## DBマイグレーション
npx sequelize-cli db:migrate
## 初期データ投入
npx sequelize-cli db:seed:all