FROM golang:1.11-alpine3.8

# gcc and libc-dev are required by testing package.
RUN apk update && apk upgrade && \
    apk add --no-cache git curl && \
    apk add --no-cache gcc libc-dev && \
    curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh

WORKDIR /go/src/github.com/deraru/gogocha

COPY . /go/src/github.com/deraru/gogocha

EXPOSE 8080

CMD go run main.go
