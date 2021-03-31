# bookster
Proiect individual EAP


Scopul acestui proiect este de a a studia si de a aprofunda principiile programarii orientate pe obiecte. 
Astfel, am ales ca tema crearea unui program care ofera servici de imprumut al cartilor, serviciu asemanator platformei Bookster.

Pana in punctul finalizarii primei etape din acest proiect, am aplicat concepte, precum:
-clase cu atribute private si diferite metode de acces;
-clase de serviciu care evidentiaza operatiile efectuate asupra array-urilor folosite;
-clasa Main din care apelam serviciile dorite;
-interfata cu metode abstracte folosite pentru legarea clasei de servicu cu Main
-diferite functii si optiuni oferite de Java(Comparable, override, regex, throw etc.)

Fisiere necesare primei etape din proiect sunt:

Carte.java
-clasa simpla in care retinem informatii de baza in ideea identificarii eficiente a acestora
-variabile folosite: String isbn(international standard book number: reprezinte codul unic al unei carti)
                     double pret(costul achizitionarii)
                     int anPublicatie(reper pentru aparitia anumitor editii ale unei carti)
- metode set si get pentru fiecare variabila
- override metodei toString(atunci cand vrem sa afisam un obiect nu mai e nevoie sa scriem de fie are data metoda)

ListaCarti.java
-clasa de serviciu
-variablie folosite: int contor(tine minte numarul de carti introduse pana in momentul respectiv)
                     int max(variabila de tip final care retine numarul maxim de carti care pot fi introduse)
                     Carte[] lista(retine toate obiectele de tip Carte)


-contine toate metodele necesare pentru gestionarea cartilor din sistem:
          - int gaseste(String isbn): cauta o carte dupa codul ei;
                                      metoda de folos pentru celelalte metode;
                                      
          - boolean formatISBN(String isbn): verifica daca formatul codului unic este respectat;
                                             de asemenea folositain in celelalte metode;
                                             
          -void adauga(): adaugam o carte, mai exact codul, pretul si anul publicarii acesteia;
        
          -void edit(): in functie de codul ISBN introdus de utilizator, pooate altera pretul si anul publicarii cartii respective;
           
          -void sort(): sorteaza cartile in ordine descrescatoare in functie de anul publicarii;
           
          -void sterge(): elimina o carte din sistem;
          
          -void afisare(): listeaza toate cartile introduse pana in acel moment;
          
InterfataCarte.java
-interfata implementata in ListaCarti.java;
-sunt notate toate metodele abstracte, care au fost ulterior implementate in clasa de serviciu;

Meniu.java
-clasa sablon in care putem implementa toate optiunile utilizatorului la rularea programului
-variabile utilizate: String[] itemMeniu (vector care retine interogarile posibile)
                      int contor (retine numarul interogarilor adaugate)
-constrcutor folosit ulterior in Main;

Main.java
-reuniunea tuturor fiserelor mentionate pana acum;
           
           
