FROM buildpack-deps:jessie

ENV RUST_VERSION=1.15.0
ENV RUST_ARCHIVE=rust-${RUST_VERSION}-x86_64-unknown-linux-gnu

RUN curl -sSLO https://static.rust-lang.org/dist/${RUST_ARCHIVE}.tar.gz \
	&& tar -xzf ${RUST_ARCHIVE}.tar.gz \
	&& ./${RUST_ARCHIVE}/install.sh --without=rust-docs \
	&& rm -rf \
		${RUST_ARCHIVE} \
		${RUST_ARCHIVE}.tar.gz
