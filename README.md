# docker-compose-python-build-example

docker-composeでpythonを実行ファイルにするサンプル

- `linux-build/`：Linux環境用のdocker-compose設定
- `windows-build/`：Windows環境用のdocker-compose設定

## Usage

Windowsの場合

```
$ cd ./windows-build
$ docker-compose up --build
$./dist/main.exe

# Hello, World!
```

Linuxの場合
```
$ cd ./linux-build
$ docker-compose up --build
$ wsl
$./dist/main

# Hello, World!
```
