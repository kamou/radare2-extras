LIBEXT=$(shell r2 -H LIBEXT)
LIBR_PLUGINS=$(shell r2 -H LIBR_PLUGINS)

all:
	for a in asm anal bin ; do $(MAKE) -C $$a ; done

clean:
	for a in asm anal bin ; do $(MAKE) -C $$a clean ; done

install:
	mkdir -p $(LIBR_PLUGINS)
	cp -f {asm,anal,bin}/*.$(LIBEXT) ${LIBR_PLUGINS}/

uninstall:
	rm -f $(LIBR_PLUGINS)/*lua53*.$(LIBEXT)
