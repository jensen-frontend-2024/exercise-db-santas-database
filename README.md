# Övning - Tomtens Databas

I denna övning ska vi börja planera, och senare skapa, en databas som tomten kan använda för att hålla koll på barn, deras önskningar och adresser.

Uppgiften kommer att utgå ifrån några user stories och en liten kravlista på data som ska ingå i databasen. En User Story är egentligen bara en kravbeskrivning på en specific feature som applikationen ( i det här fallet databasen ) ska uppfylla och dessa user stories är skrivna utifrån tomtens perspektiv.

Uppgiften innehåller olika delar och vi behöver olika kunskaper för att kunna läsa de olika delarna. Det betyder att vi inte kan läsa hela uppgiften på en gång. Följande kunskaper behövs för varje del:

**Del 1 - Kunskap om ER-diagram, entiteter, attribut och relationer.**

**Del 2 - Kunskap om ett databasprogram _( SQLite Studio i vårt fall )_.**

**Del 3 - Kunskap om grundläggande SQL.**

### User Stories

1. Som tomte vill jag ha ett register över barn där jag kan se deras namn och addresser.

2. Som tomte vill jag kunna ha barnens önskelistor samlade.

3. Som tomte vill jag kunna se önskelistan tillsammans med barnets namn och address.

### Instruktioner del 1 - ER-Diagram

Ni ska skapa ett tydligt och strukturerat ER-diagram som omfattar alla user stories från ovan. Tänk igenom vilka entiter som ska finnas samt vilka attribut som ska finnas på varje entitet. Tänk också igenom vilka relationer som ska finnas mellan de olika entiteterna.

### Instruktioner del 2 - Skapa databasen

1. Använda dig av SQLite studio
2. Utgå ifrån ditt ER-Diagram och skapa de nödvändiga tabellerna, kolumner och relationer.
3. Fyll på de olika tabellerna med data som syns längre ner i uppgiften.

### Instruktioner del 3 - Skriva queries

Skriv queries som motsvarar det som efterfrågas i user stories. Försök att spara undan de i Views.

Vad är en view då?

En view i SQLite är en virtuell tabell som skapas baserat på resultatet av en SELECT-fråga. Viewen fungerar som en sparad fråga som du kan använda för att förenkla komplexa databasfrågor eller för att presentera data på ett visst sätt utan att ändra den underliggande tabellen.

Här är ett exempel:

```sql
CREATE VIEW view_all_students AS
SELECT * FROM students;
```

View som skapas av detta kommer att läggas under "Views" under databasen i databas-fönstret till vänster i SQLite studio.

### Kravlista för data / Läggs in senare..

Följande data ska ingå i databasen.

**Personer som ska existera i databasen**

- Karl Månstråle, Bjärsgård, 27100 Rydsgård, Sweden
- Winston Churchy, 4 Tennison Rd, CB4EA Cambridge, UK
- Fairy Godmother, Main st 1, Main, 41110 Maine, USA
- Trompe Le Donne, Vita stugan 1, 1000 Washington DC, USA

**Karl önskar sig:**

- Stenbock
- Gunghäst
- Käpphäst
- Garnnystan

**Winston önskar sig:**

- Nordafrika
- Levanten
- Istanbul
- Fred på jorden

**Fairy Godmother önskar:**

- Skiva med Marcus och Martinus
- Fred på jorden
- Polkagrisar

**Trompe Le Donne önskar:**

- Ledigt
- Lugn och ro
- Inskränkningar i pressfriheten
- Nya golfklubbor
