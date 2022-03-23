FROM golang:alpine as stage1

WORKDIR /go/src/app

COPY . .

RUN go build -o /app main.go

FROM scratch

COPY --from=stage1 /app /app

CMD [ "/app" ]