
Docker環境構築にトライ
===============

とても面白そうな記事をみつけ、現在利用中のWordpressのテーマ編集をしたくて、Dockerに触れてみることにしました。Wordpressのテーマ作成のためのツールはたくさん出回ってますが、先進的な技術も勉強したいので、あえてDockerを選びました。
また、以前にもDockerを使ったPHP+Apache+MySQLの環境構築にチャレンジしましたがMySQLの接続が上手くいきませんでした。私はLaravelで主に開発の勉強をしていますが、PHPのみの環境でPDOなどを使ったコードも勉強したいと思っています。そんな私にはぴったりの記事でした。
  
  
  
作成には、以下のリンクを参考にしました。  

参考  
[docker-compose による nginx + HTTP/2 + PHP-FPM7 + MySQL 環境の構築方法](https://tech.recruit-mp.co.jp/infrastructure/post-12795/)

先に述べた、Docker環境構築の挑戦時にymlファイルやnginxのconfファイルを直接叩いて勉強していました。今回のこの記事は、その時と違って詳細かつ段階を踏んでdockerの実装を行なっています。私にはぴったりだと思い挑戦してみました。ついでにvimにも慣れたかったため、ymlやcomfigファイルはできる限りvimで記述しています。

***

### Version

さくらインターネットと同環境を用意

 - `nginx:1.13.5-alpine`
 - `php:7.1.9-fpm-alpine`
 - `mysql:5.7.19`

### Structure

```
gataponMacBook-pro:static-hp-docker gatapon$ tree
.
├── app
│   └── Dockerfile
├── data
│   └── html
│       ├── img.jpg
│       ├── index.php
│       ├── main.css
│       └── main.js
├── db
│   └── initial.sql
├── docker-compose.yml
├── readme.md
└── web
    ├── Dockerfile
    └── default.conf
```
