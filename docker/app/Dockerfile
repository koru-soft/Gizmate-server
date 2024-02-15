FROM golang:1.22.0-alpine3.19

ENV TZ /usr/share/zoneinfo/Asia/Tokyo

# 依存関係をインストール
RUN apk update && apk add --no-cache git

# air をインストール
RUN go install github.com/cosmtrek/air@latest

# アプリケーションディレクトリを作成し、作業ディレクトリとして設定
WORKDIR /app

# アプリケーションのソースコードと依存関係ファイルをコピー
COPY app/go.mod ./
COPY app/go.sum ./
COPY app/ ./

# 依存関係をダウンロード
RUN go mod download -x

# コンテナの公開するポートを指定
EXPOSE 8080

CMD ["air", "-c", ".air.toml"]
