# cheatcoin: Makefile; T13.656-T13.816; $DVS:time$

dnet	 = ../dnet
dfstools = ../dus/programs/dfstools/source
dfslib	 = $(dfstools)/dfslib
dar		 = ../dus/programs/dar/source
ldusinc	 = ../ldus/source/include/ldus

sources = \
	address.c					\
	block.c						\
	crypt.c						\
	hash.c						\
	log.c						\
	main.c						\
	memory.c					\
	netdb.c						\
	pool.c						\
	sha256.c					\
	storage.c					\
	sync.c						\
	transport.c					\
	wallet.c					\
	$(dnet)/dnet_crypt.c		\
	$(dnet)/dnet_database.c		\
	$(dnet)/dnet_main.c			\
	$(dnet)/dnet_threads.c		\
	$(dnet)/dnet_connection.c	\
	$(dnet)/dnet_stream.c		\
	$(dnet)/dnet_packet.c		\
	$(dnet)/dnet_command.c		\
	$(dnet)/dnet_log.c			\
	$(dnet)/dnet_files.c		\
	$(dnet)/dnet_tap.c			\
	$(dfslib)/dfslib_crypt.c	\
	$(dfslib)/dfslib_random.c	\
	$(dfslib)/dfslib_string.c	\
	$(dfstools)/lib/dfsrsa.c	\
	$(dar)/lib/crc_c.c			\


headers = \
	address.h						\
	block.h							\
	crypt.h							\
	hash.h							\
	log.h							\
	main.h							\
	memory.h						\
	netdb.h							\
	pool.h							\
	sha256.h						\
	state.h							\
	storage.h						\
	sync.h							\
	transport.h						\
	wallet.h						\
	$(dnet)/dnet_crypt.h			\
	$(dnet)/dnet_database.h			\
	$(dnet)/dnet_history.h			\
	$(dnet)/dnet_threads.h			\
	$(dnet)/dnet_connection.h		\
	$(dnet)/dnet_stream.h			\
	$(dnet)/dnet_packet.h			\
	$(dnet)/dnet_command.h			\
	$(dnet)/dnet_log.h				\
	$(dnet)/dnet_files.h			\
	$(dnet)/dnet_tap.h				\
	$(dnet)/dthread.h				\
	$(dfslib)/dfslib_crypt.h		\
	$(dfslib)/dfslib_random.h		\
	$(dfslib)/dfslib_string.h		\
	$(dfslib)/dfslib_types.h		\
	$(dfstools)/include/dfsrsa.h	\
	$(dar)/include/crc.h			\
	$(ldusinc)/atomic.h				\
	$(ldusinc)/list.h				\
	$(ldusinc)/rbtree.h				\


flags = -std=gnu11 -O3 -DDFSTOOLS -DCHEATCOIN -DNDEBUG -g -lpthread -lcrypto -lm -Wall -Wmissing-prototypes -Wl,--export-dynamic


all: xdag

xdag: $(sources) $(headers) Makefile
	gcc -o xdag $(sources) $(flags)

clean:
	rm xdag

install: xdag
	sudo cp xdag /usr/local/bin/xdag
	sudo cp xdag /usr/local/sbin/xdag
