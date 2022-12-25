# web_stack
web開発及び試験用のリポジトリ

[nodejs install]

cf: https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04-ja
    https://qiita.com/seibe/items/36cef7df85fe2cefa3ea

$ sudo apt install -y nodejs npm

$ sudo npm install n -g

$ sudo n stable

$ node -v

[docker install]

cf: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-ja

$ sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

$ sudo apt update

$ apt-cache policy docker-ce

$ sudo apt install docker-ce docker-ce-cli

$ docker --version

[docker-compose install]

$ pip install docker-compose

[docker-compose up -d 権限周り]
// linuxによってはデフォルトはrootユーザーのみで扱えるので、それ以外のユーザーでも扱えるように設定する。
$ sudo gpasswd -a $USER docker

$ newgrp docker

[余談]
pip install -U package_name でpip install でインストールするライブラリをアップデートできる

参照：
https://zenn.dev/takeo/articles/8c06f2420c328c
https://ashwin9798.medium.com/nginx-with-docker-and-node-js-a-beginners-guide-434fe1216b6b
