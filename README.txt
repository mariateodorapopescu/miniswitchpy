1

POPESCU MARIA TEODORA
332CC
TEMA 1 Retele Locale - Implementare Switch in Python

Am reusit sa implementez numai primul task, cel cu tabela de comutare.
Efectiv am luat pseudocod-ul si l-am tradus in python.
In schimb, singurul lucru cat de cat original ar fi functia de verificare
daca e adresa unicast. Dupa o documentare pe internet, am gasit formula de
verificare pentru adresa de tip unicast, daca e 0 sau 1. Deci, primul octet al adresei MAC, se deplasează la dreapta cu 0 biți, desi nu are nicio influenta asupra valorii, dar e mai mult claritatea codului.
Se realizează o operație logică "si" intre rezultatul deplasării și valoarea 1, verificand daca cel mai puțin semnificativ bit al primului octet este par sau impar. Cum poate fi 0 sau 1, 0 par, 1 impar, ei bine...