Se si desidera compilare a mano la libreria senza utilizzare la procedura d'installazione così come descritto nel file INSTALL, si può procedere come segue:

Per creare la libreria statica:
-----------------------------

    gcc -c -Wall -W -O2 -std=c99 myoptParser.c myoptLexer.c myoptSymtab.c
    ar  -r -s libmyoptParser.a myoptParser.o myoptLexer.o myoptSymtab.o

Per usare la libreria:
-------------------

    gcc -Wall -W -O2 -std=c99 -L. sample1.c -lmyoptParser -o sample1
    gcc -Wall -W -O2 -std=c99 -L. sample2.c -lmyoptParser -o sample2

    g++ -Wall -W -O2 -L. sample1.cpp -lmyoptParser -o sample1cpp
    g++ -Wall -W -O2 -L. sample2.cpp -lmyoptParser -o sample2cpp
