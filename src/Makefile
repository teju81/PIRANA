IDIR = ../include
LDIR = ../lib
LIBS=-lglut -lGL -lGLU -lm -lassimp
CC=gcc
CFLAGS=-I$(IDIR)
ODIR=.
_DEPS = frustum.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))
_OBJ= animation.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

%(ODIR)/%.o: %.c $(DEPS)
	$(CC) - c -o $@ $< $(CFLAGS)

animation: $(OBJ)
	gcc -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~core $(INCDIR)/*~
