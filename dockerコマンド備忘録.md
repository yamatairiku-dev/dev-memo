# GitHubのリポジトリ"todo-simple-app"の"main"ブランチをリポジトリ内のDockerfileを使ってimage作成
# リファレンス https://docs.docker.jp/engine/reference/commandline/build.html
docker build -t todo-simple-app https://github.com/yamatairiku-dev/todo-simple-app.git#main

# アプリの起動ポートを指定してcontainer起動
docker run --env PORT=80 --name mytodoapp --hostname mytodoapp -p 3030:80 --detach mytodoapp


# Azureにdocker containerでデプロイ
# リファレンス https://docs.microsoft.com/ja-jp/dotnet/architecture/cloud-native/deploy-containers-azure
# Azure login
az login
# Azure コンテナリポジトリにログイン
az acr login --name myhogehogetodoapp

