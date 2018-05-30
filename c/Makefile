all: basic

mlpnnets.o: mlpnnets.c mlpnnets.h
	gcc -Wall -c mlpnnets.c -lm

basictests.o: basictests.c mlpnnets.h
	gcc -Wall -c basictests.c -lm

testiris.o: testiris.c mlpnnets.h
	gcc -Wall -c testiris.c -lm
 
basic: mlpnnets.o basictests.o
	gcc -o basic mlpnnets.o basictests.o -lm

iris: testiris.o mlpnnets.o
	gcc -o iris testiris.o mlpnnets.o -lm

adult: testadult.o mlpnnets.o
	gcc -o adult testadult.o mlpnnets.o -lm

clean:
	rm -f *.o
	rm -f *.gch
	rm -f basic
	rm -f iris
	rm -f adult
