# 初期設定でやっていること

権限周りを解決するため以下コマンドで対処
```
export user=$(id -u):$(id -g)
```

コンテナを立てるためdockerファイル内で以下コマンドで立てる
```
docker-compose up --build -d
```

### laravel設定

PHPのパッケージ管理システムをインストールする
```
composer install
```

### インストール完了後envファイルをコピーする
```
cp .env.example .env
```

### アプリケーションを暗号化するためのキーを生成する
```
php artisan key:generate
```

### データベースの作成

```
php artisan migrate
```
