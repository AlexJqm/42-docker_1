FROM debian

RUN apt-get update && apt-get upgrade -y && apt-get install -y clang binutils make vim git

WORKDIR /home/checkers

RUN 	git clone https://github.com/cl4k/InitChecker.git init && \
	git clone https://github.com/anisg/fillit_checker.git fillit && \
	git clone https://github.com/alelievr/libft-unit-test.git libft-unit && \
	git clone https://github.com/jtoty/Libftest.git libftest && \
	git clone https://github.com/jgigault/42FileChecker.git 42filechecker

WORKDIR /home/games

RUN	git clone https://github.com/samtay/snake.git && \
	git clone https://github.com/samtay/tetris.git

# docker build -t 42-env .
# docker run --rm -ti 42-env sh
