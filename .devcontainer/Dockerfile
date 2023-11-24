FROM alpine:3.18

# Essentials
RUN apk add -U tzdata git curl
ENV TZ=Europe/Berlin
RUN cp /usr/share/zoneinfo/$TZ /etc/localtime

# Install Clang
RUN apk add -U clang
	
# Install Rust
RUN curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH=$PATH:/root/.cargo/bin

RUN rustc --version