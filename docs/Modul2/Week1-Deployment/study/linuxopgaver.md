# Linuxopgaver
Disse opgaver skal laves individuelt. 

## Opgave 1 
Log ind på din Droplet via ssh og brug dit eget brugernavn

## Opgave 2
- Brug nano og opret en tom tekst-fil ved navn `klasseliste.txt`.
2. Kopier navnelisten herunder ind i tekstfilen og gem den:

```
Benjamin S.	cph-bhdgs190@cphbusiness.dk
Frederik J.	cph-fj1hg08@cphbusiness.dk
Mari H.	cph-mhgfs823@cphbusiness.dk 
Martin H.	cph-mh8gfs24@cphbusiness.dk 
Matt T.	cph-mt3sdfg12@cphbusiness.dk 
Pelle R	cph-prsdfg128@cphbusiness.dk 
Jon B.	jodfghbe@cphbusiness.dk	
Nikolaj H. nbhhghgd@cphbusiness.dk 
```

- Opret en tom folder ved navn Lister og flyt `klasselisten.txt` derned.

## Opgave 3 
Kopier `klasselisten.txt`  fra din Droplet til din egen laptop ved hjælp af FileZilla.

## Opgave 4

- Lav en ændring i filen (tilføj et navn mere) og kopier den tilbage til din Droplet.
- Vis indholdet af filen på din Droplet ved hjælp af `cat` og tjek om ændringen er kommet med over.


## Opgave 5

- Lav en kopi af `klasselisten.txt` og kald den `gammelliste.txt`.
- Fjern underviserne fra listen i `gammelliste.txt` og gem filen.
- Find ud af hvordan du kan kopiere `gammelliste.txt` til din egen laptop ved hjælp af kommandoen ´scp`(i stedet for at brug FileZilla).
- Brug den indbyggede brugervejledning i Linux (man) og find ud af hvordan man anvender `scp`.

## Opgave 6

- Brug kommandoen `grep` til at søge alle filer igennem fra /opt/tomcat folderen og led efter filer, som indeholder ordet "dat2user". 
- Brug kommandoen `find` til at finde alle filer af typen `xml`, som ligger i - eller under /opt/tomcat.