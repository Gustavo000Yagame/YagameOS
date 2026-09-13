FROM alpine:latest
WORKDIR /app

COPY yagame-server .
COPY index.html .
COPY interface.wasm .
COPY YagameOS.png .
COPY yagameos.img .

EXPOSE 8080

CMD ["./yagame-server"]
