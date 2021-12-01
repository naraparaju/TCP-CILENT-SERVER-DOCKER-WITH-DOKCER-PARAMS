#FROM ubuntu:bionic
FROM gcc:latest as builder
ADD . /usr/src
WORKDIR /usr/src
EXPOSE 5555
RUN g++ -static medium_server.cpp -o medium_server

FROM alpine:latest
COPY --from=builder /usr/src /bin

# comment this and un - comment other if you would like to run your # program manually from shell
CMD ["./bin/medium_server"] 
#CMD ["/bin/bash"]