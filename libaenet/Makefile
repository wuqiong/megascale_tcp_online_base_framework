include ../config.mk
include ../server.mk


SRC = ae.c anet.c
OBJ = ${SRC:.c=.o}
CFLAGS = -Wno-parentheses -Wno-switch-enum -Wno-unused-value

TARGET = libae_net.a

all: $(OBJ)
	$(AR) -rc $(TARGET) $(OBJ)
	cp $(TARGET) $(MYLIB)

%.o: %.c
	$(CC) -c $(CFLAGS) $< -o $@


clean:
	rm -f $(OBJ) libae_net.a

.PHONY: clean
