FROM alpine:3.10 as builder

RUN apk --no-cache add \
    cmake \
    build-base \
    git

RUN git clone https://github.com/tevador/RandomX.git

WORKDIR /RandomX/build

RUN cmake -DARCH=native .. \
    && make

FROM alpine:3.10

COPY --from=builder /RandomX/build /RandomX

RUN apk --no-cache add gcc && \
    ln -s /RandomX/randomx-benchmark /bin/randomx-benchmark \
    && randomx-benchmark --help

ENTRYPOINT ["randomx-benchmark"]
CMD ["--help"]