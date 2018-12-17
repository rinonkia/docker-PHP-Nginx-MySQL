
Docker環境構築にトライ
===============

現在利用中のWordpressのテーマ編集をしたいと思いました。Wordpressのテーマ作成のためのツールはたくさん出回ってますが、今回とても面白そうな記事をみつけたので、実際にDockerで環境を構築してみようと思いました。  

また、以前にもDockerを使ったPHP+Apache+MySQLの環境構築にチャレンジしましたがMySQLの接続が上手くいきませんでした。私はLaravelで主に開発の勉強をしていますが、PHPのみの環境でPDOなどを使ったコードも勉強したいと思っています。そんな私にはぴったりの記事でした。
  
  
  
作成には、以下のリンクを参考にしました。  

参考  
[docker-compose で作る nginx + PHP-FPM7 + HTTP/2 に対応したモダンな WordPress 開発環境](https://tech.recruit-mp.co.jp/infrastructure/post-12795/)

少し前にもymlファイルやnginxのconfファイルを直接叩いて勉強していました。今回のこの記事は、詳細に段階を踏んでdockerの実装方法について書かれていたので、私にはぴったりだと思いました。ついでにvimにも慣れたかったため、ymlやcomfigファイルはできる限りvimで記述しています。

よろしくお願いします！
