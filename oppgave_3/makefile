INCLDIR = ./include
CC = gcc
CFLAGS = -O2
CFLAGS += -I$(INCLDIR)

OBJDIR = obj

_DEPS = oppgave_3.h
DEPS = $(patsubst %,$(INCLDIR)/%,$(_DEPS))

_OBJS = oppgave_3.o createReservation.o getReservationNumberN.o searchReservation.o deleteReservation.o addFood.o printReceipt.o
OBJS = $(patsubst %,$(OBJDIR)/%,$(_OBJS))

$(OBJDIR)/%.o: %.c $(DEPS)
		$(CC) -c -o $@ $< $(CFLAGS)


oppgave_3: $(OBJS)
		$(CC) -o $@ $^ $(CFLAGS)

.PHONY: clean
clean:
		rm -f $(OBJDIR)/*.o *~ core $(INCLDIR)/*