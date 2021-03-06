Med Power BI kan du skapa relationer mellan flera tabeller, inklusive tabeller som kommer från helt olika datakällor. Du kan visa dessa relationer för alla datamodeller i vyn **Relationer** i Power BI Desktop.

![](media/7-5-table-relationships-and-dax/dax-relationships_1.png)

## <a name="dax-relational-functions"></a>DAX relationella funktioner
DAX har **relationella funktioner** som gör att du kan interagera med tabeller som har etablerade relationer.

Du kan returnera värdet för en kolumn, eller alla rader i en relation, med hjälp av DAX-funktioner.

**TABLE**-funktionen följer som exempel relationer och returnerar värdet för en kolumn, medan **RELATEDTABLE** följer relationer och returnerar en hel tabell som har filtrerats för att bara inkludera relaterade rader.

![](media/7-5-table-relationships-and-dax/dax-relationships_2.png)

**RELATED**-funktionen fungerar på *många-till-en*-relationer, medan **RELATEDTABLE** är avsedd för *en-till-många*-relationer.

Du kan använda relationella funktioner för att skapa uttryck som innehåller värden från flera tabeller. DAX returnerar ett resultat med dessa funktioner, oavsett hur lång relationskedjan är.

> Videoinnehåll tillhandahållet av [Alberto Ferrari, SQLBI](http://www.sqlbi.com/learning-dax)
> 
> 

