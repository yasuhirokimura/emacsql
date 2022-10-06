-include ../.config.mk

.POSIX:
CC = cc
LDLIBS = -ldl -lm -lsqlite3
CFLAGS = -O2 -Wall -Wextra -Wno-implicit-fallthrough \
    -DSQLITE_THREADSAFE=0 \
    -DSQLITE_DEFAULT_FOREIGN_KEYS=1 \
    -DSQLITE_ENABLE_FTS5 \
    -DSQLITE_ENABLE_FTS4 \
    -DSQLITE_ENABLE_FTS3_PARENTHESIS \
    -DSQLITE_ENABLE_RTREE \
    -DSQLITE_ENABLE_JSON1 \
    -DSQLITE_SOUNDEX

emacsql-sqlite: emacsql.c
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ emacsql.c $(LDLIBS)

clean:
	rm -f emacsql-sqlite
