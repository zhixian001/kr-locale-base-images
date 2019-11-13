FROM debian:buster

ENV LANG="ko_KR.UTF-8" \
    LANGUAGE="ko_KR.UTF-8" \
    LC_ALL="ko_KR.UTF-8"

RUN sed -i 's/deb.debian.org/ftp.kr.debian.org/g' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y locales && \
    rm -rf /var/lib/apt/lists/* && \
    echo "ko_KR.UTF-8 UTF-8" >> /etc/locale.gen && \
    locale-gen && \
    localedef -i ko_KR -c -f UTF-8 -A /usr/share/locale/locale.alias ko_KR.UTF-8
