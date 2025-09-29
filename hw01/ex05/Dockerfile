FROM ubuntu:22.04

WORKDIR /app

COPY . /app

WORKDIR /app/libmicrohttpd-1.0.1

RUN apt-get update
RUN apt-get install -y gcc make


RUN ./configure
RUN make
RUN make install
RUN ldconfig

WORKDIR /app

RUN make

ENTRYPOINT ["./main"]

CMD ["8888"]

