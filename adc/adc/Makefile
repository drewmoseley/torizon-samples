DEPS = adc.h iio_utils.h
OBJ = adc.o iio_utils.o

%.o : %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

adc: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS)

install: adc
	mkdir -p $(WORKDIR)
	cp adc $(WORKDIR)/

clean:
	rm -f *.o
	rm -f adc
