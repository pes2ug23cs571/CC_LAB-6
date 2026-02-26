FROM ubuntu:22.04

RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    apt-get update -o Acquire::Retries=3 && \
    apt-get install -y g++ && \
    apt-get clean

WORKDIR /app

COPY app.cpp .

RUN g++ app.cpp -o app

CMD ["./app"]
