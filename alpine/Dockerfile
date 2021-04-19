FROM julia:1.6-alpine
ARG SBT_VERSION

ENV SFST_VERSION ${SFST_VERSION:-1.4.7e}

RUN apk --update add curl wget tar bash make g++ readline-dev ncurses-dev git git-bash-completion

RUN \
 curl -fsL https://www.cis.uni-muenchen.de/~schmid/tools/SFST/data/SFST-${SFST_VERSION}.tar.gz | tar xfz - && \
 cd SFST/src && make && make install && echo Installed fst-infl in `which fst-infl`

RUN apk add ncurses
