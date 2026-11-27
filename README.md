[![Preview](/media/preview.png)](https://github.com/tiltful/shortify)

[![Stars](https://custom-icon-badges.demolab.com/github/stars/tiltful/shortify?logo=star)](https://github.com/tiltful/shortify/stargazers')
[![Open issues](https://custom-icon-badges.demolab.com/github/issues-raw/tiltful/shortify?logo=issue)](https://github.com/tiltful/shortify/issues)
[![License](https://custom-icon-badges.demolab.com/github/license/tiltful//shortify?logo=law)](https://github.com/DenverCoder1/custom-icon-badges/blob/main/LICENSE?rgh-link-date=2023-03-15T18%3A10%3A26Z "license MIT")
[![Powered by Go](https://custom-icon-badges.herokuapp.com/badge/-Powered%20by%20Go-0d1620?logo=go)](https://go.dev/ "Powered by GO")
[![Powered by Postgres](https://custom-icon-badges.herokuapp.com/badge/-Powered%20by%20PosgreSQL-0d1620?logo=postgres)](https://github.com/postgres/postgres "Powered by Postgres")
___

## 🧩 Installation
```
git clone https://github.com/tiltful/shortify.git 
cd shortify
go build
```

## ⚙ Configuration
### Setup environment variables
#### Linux/MacOS
```shell
chmod +x ./dotenv.sh
./dotenv.sh
```
#### Windows
```shell
.\dotenv.ps1
```
#### Makefile
```shell
make env
```

Open `config/config.yml` and fill in the values

## 🚀 Launch
Run `go run cmd/grpc_server/main.go` or `make start`.

## 🧹 Linters
Run `golangci-lint run cmd/... internal/... pkg/... --config=./.golangci.yml` or `make lint`.

## 🧪 Tests
Run `go test ./internal/... -v` or `make test`.

## 🏇 Benchmarks
Run `go test ./internal/... -bench=. -benchmem` or `make bench`.
___

## 🌐 Deployment
Run `docker-compose up -d`.
___

## 🔎 Example of usage
### Creating a short link

`grpc://{{base_url}}/url_v1.UrlV1/Post?url=https://example.com`
```
# Response
{
    "short_url": "{{base_url}}/abc123_ABC"
}
```
### Getting the original link

`grpc://{{base_url}}/url_v1.UrlV1/Get?hash=abc123_ABC`
```
# Response
{
    "url": "https://example.com"
}
```

## 🤝 Contributing

Contributions are what make the open source community an amazing place to learn, be inspired, and create.
Any contributions you make are **greatly appreciated**.

1. [Fork the repository](https://github.com/tiltful/shortify/fork)
2. Clone your fork `git clone https://github.com/tiltful/shortify.git`
3. Create your feature branch `git checkout -b AmazingFeature`
4. Stage changes `git add .`
5. Commit your changes `git commit -m 'Added some AmazingFeature'`
6. Push to the branch `git push origin AmazingFeature`
7. Submit a pull request

## ❤️ Credits

Released with ❤️ by [Tilt](https://github.com/tiltful).