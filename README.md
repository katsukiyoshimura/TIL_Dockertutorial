概要
Dockerは「アプリ開発の環境の構築を自動化するツール」でありコンテナ技術を使いやすくまとめたソフトウェア
コンテナは「大きい単位で環境をパッケージとしてまとめたもの」。アプリ開発に必要なものが一通り揃ったお道具箱のイメージ

コマンド
docker build -t <イメージ名>               :コンテナイメージの作成
docker run 　                            :コンテナをスタートさせる
docker ps                                :動いているコンテナ一覧を表示する
docker stop <the-container-id>　　　　　   :コンテナを停止させる
docker rm <the-container-id>　　　　　　    :コンテナを削除する
docker push YOUR-USER-NAME/getting-started:Docker Hubへのプッシュ。Git pushと同じと認識

コンテナのファイルシステム
コンテナの変更は他のコンテナには影響しない

named Volume 
指定したファイルシステムをホストマシンに保存する
データを残す手順 (named volumes)
1. docker volume create でvolumeを作成
2. 動いているコンテナは削除
3. docker run -dp 3000:3000 -v todo-db:/etc/todos で残したいコンテナを作成
4. 変更を加え、コンテナを削除
5. 3のコマンドをもう一度実行
(volumeを作成しデータが格納されているディレクトリにアタッチ（「マウント」と呼ばれる）することで、データを永続化することができる)

Bind mount
ホスト上の正確なマウントポイントを制御)

