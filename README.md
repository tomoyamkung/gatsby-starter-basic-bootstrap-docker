# README

プロジェクトのパッケージマネージャーには yarn を使用。

イメージのビルドと起動：

```sh
$ pwd
/path/to/gatsby-starter-basic-bootstrap-docker

$ docker-compose up -d --build
Building gatsby
:
:
Successfully tagged gatsby-starter-basic-bootstrap-docker_gatsby:latest
Recreating gatsby-starter-bootstrap-docker ... done

➜ docker-compose ps | grep gatsby
gatsby-starter-basic-bootstrap-docker   docker-entrypoint.sh node   Up      0.0.0.0:8000->8000/tcp
```

コンテナ内で bash を実行する：

```sh
$ docker exec -it gatsby-starter-basic-bootstrap-docker bash
bash-5.0$
```

Gatsby プロジェクトの作成：

```sh
bash-5.0$ gatsby new gatsby-starter-basic-bootstrap-docker https://github.com/mik3y/gatsby-starter-basic-bootstrap.git
```

開発サーバの起動：

```sh
bash-5.0$ pwd
/home/dev/gatsby-starter-basic-bootstrap-docker/gatsby-starter-basic-bootstrap-docker

bash-5.0$ gatsby develop --host 0.0.0.0
:
:
You can now view gatsby-starter-default in the browser.
⠀
  Local:            http://localhost:8000/
  On Your Network:  http://172.22.0.2:8000/
⠀
View GraphiQL, an in-browser IDE, to explore your site's data and schema
⠀
  Local:            http://localhost:8000/___graphql
  On Your Network:  http://172.22.0.2:8000/___graphql
⠀
Note that the development build is not optimized.
To create a production build, use gatsby build
⠀
success Building development bundle - 16.326s
```
