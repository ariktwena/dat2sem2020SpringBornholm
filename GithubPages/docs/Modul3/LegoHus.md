# Et lego hus
I har i de sidste uger arbejdet i grupper. For at give jer chancen for at checke, at I også kan bygge et lille web-program selv, så skal I lave dette system alene.

Senere i semesteret skal I lave et system for Fog Tømmerhandel, som kan bruges til at håndtere salg af carporte. Et af de elementer der er i disse systemer er *styklister* - tabeller over hvilke dele (brædder, skruer, fundament blokke, mv) der skal bruges for at bygge en carport. 

Styklisten afhænger af hvor stor carporten skal være, samt nogle regler for hvordan en carport bygges.

I dette lille enmands projekt skal vi ikke beregne styklister for carporte, men for væggene i et lego hus 🙂. Som en hjælp til at forstå problemstillingen bedre, kan I evt. [downloade dette program](https://www.lego.com/en-us/ldd/download) til at modellere legohuset i. 

### Aflevering
Der afleveres et link til dit github projekt på Moodle. Deadline er søndag den 31. marts kl. 23.55. 
#### [Link til afleveringsside](https://cphbusiness.mrooms.net/mod/assign/view.php?id=128716).


### Kravsspecifikation

Der skal laves et system hvor man kan registrere sig som kunde. 

Til det [kan benyttes den skabelon vi har lavet](https://github.com/jonbertelsen/LogInSample).


#### Kundekrav (user-stories eller funktionelle krav)

**US-1.** Som kunde vil jeg gerne kunne oprette en ordre på et lego hus, sådan at jeg kan få en stykliste for huset. Ordren skal indeholde længde og bredde af lego husets vægge (angives i antal "prikker" huset skal være på hver led), samt hvor mange klodser man ønsker det skal være højt.

**US-2** Som kunde vil jeg gerne kunne se mine tidligere ordrer, sådan at jeg kan se hvad jeg tidligere har bestilt.

**US-3** Som kunde vil jeg gerne kunne se om min ordre er afsendt, sådan at jeg kan planlægge hvornår jeg skal lege med lego.

**US-4** Som kunde vil jeg gerne kunne se styklister for mine tidligere ordrer.

#### Styklister
Vi vil antage, at vi bygger lego husene af tre typer klodser: 
a) brikker med 2x4 prikker, 
b) brikker med 2x2 prikker, og 
c) brikker med 1x2 prikker.

Et hus der er 13x9 prikker og 4 klodser højt *kan* se sådan ud:

![](legowalls01.jpg)

og kan laves med følgende stykliste (som ikke er den der er på tegningen): 


| type | side 1 | side 2 | side 3 | side 4 | ialt | ialt x højde |
| ---- | ------ | ------ | ------ | ------ | ---- |------------ |
| 2x4  | 3      | 1      | 3      | 1      | 8    |32           |
| 2x2  |        |        |        |        |      |             |
| 1x2  | 1      | 1      | 1      | 1      | 4    |16           |

### Firma krav
**US-5**. Det skal være muligt for en ansat at se hvilke ordrer, der er i systemet. 

**US-6** Det skal være muligt for en ansat at markere en ordre som afsendt. 

## Kvalitetskrav til afleveret system (ikke-funktionelle krav)
1. Det færdige system skal ligge som IntelliJ projekt på github.

2. Det færdige system skal være struktureret efter 3-lags modellen -  præsentationslag, forretningslag og datalag.

3. Det forventes, at der er en facade mellem præsentations og forretningslag og evt. mellem forretningslaget og datamappers.

4. Det forventes, at der *IKKE* kaldes forretningslogik (eller datamappers) fra JSP siderne.

5. Det forventes, at session og requests attributter anvendes korrekt.

6. Vi vil anse det for en fejl, hvis der bruges *redirect* hvor der burde bruges *forward*.

7. Det forventes at styklisterne ikke gemmes i databasen, men beregnes i forretningslaget.

8. Du skal håndtere exceptions, så fejlmeddelelser vises på en jsp side.

### Grønne, Gule og Røde krav
#### Grøn
- Det forventes, at du opfylder kundekrav US-1 & US-2. Altså at man kan oprette en ordre og få en stykliste for denne. 
- Kravene til systemets kvalitet, som nævnt ovenfor, skal opfyldes.
- Du skal fange exceptions i servletten.

#### Gul
- Det forventes, at du har kundekrav US-4 med. 
- Det forventes også, at du bygger i "forbandt" - at klodserne i lagene er forskudt i forhold til hinanden. Her kan du [blive inspireret til flotte forbandt mønstre](https://www.randerstegl.dk/dk/mursten/fuldmuret-byggeri/forbandter-fuger).
- Kravene til systemets kvalitet, som nævnt ovenfor, skal opfyldes.
- Du skal lave en specialiseret exception, som du kaster fra datalaget og fanger i en servlet.

#### Rød
- Det forventes, at du også har kundekrav US-3 med i din løsning.
- Det forventes også, at du på den ene langside gør plads til et vindue (vælg selv en fast størrelse), og på den anden langside gør plads til en dør (vælg selv en fast størrelse.)
- Kravene til systemets kvalitet, som nævnt ovenfor, skal opfyldes.
- Det forventes, at du bruger en front-controller som vist i det vedlagte oplæg.
