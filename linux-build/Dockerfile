# Dockerfile
FROM python:3.9-slim

# 必要なパッケージをインストール
RUN apt-get update && apt-get install -y \
    build-essential \
    python3-dev \
    && rm -rf /var/lib/apt/lists/*

# PyInstallerをインストール
RUN pip install pyinstaller

# 作業ディレクトリを作成
WORKDIR /app

# スクリプトをコンテナにコピー
COPY main.py .

# PyInstallerを実行してexeファイルを作成し、その後にexeファイルを実行
CMD ["sh", "-c", "pyinstaller --onefile main.py && ls -l ./dist && ./dist/main"]
