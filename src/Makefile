CFLAGS = -lfl -g -lm

acalc: objs
	gcc -o acalc *.o $(CFLAGS)

objs: *.c *.l *.y
	bison -d acalc.y
	flex flex.l
	gcc -c *.c $(CFLAGS)

.PHONY: clean

clean:
	-rm -rf *.o *.tab.* lex.yy.c acalc

