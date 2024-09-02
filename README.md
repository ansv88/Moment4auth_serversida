# Webbtjänst (API) för registrering och inloggning
Det här repot innehåller kod för ett enklare REST API byggt med Express. APIet är byggt för att kunna registrera en användare samt logga in till en skyddad sida.

## Länk
En liveversion av APIet finns tillgänglig på följande URL:
[https://moment4auth-serversida.onrender.com]

## Installation, databas
APIet använder en MongoDB-databas. Alla id:n för objekten automatgenereras av MongoDB.
Klona källkodsfilerna, kör kommando npm install för att installera nödvändiga npm-paket. 

## Användning
Nedan finns beskrivet hur man når APIet med olika ändpunkter:

|Metod  |Ändpunkt            |Beskrivning                                                                       |
|-------|--------------------|----------------------------------------------------------------------------------|
|GET    |/api/protected      |Hämtar all tillgänglig arbetslivserfarenhet.                                      |
|POST   |/api/register       |Registrerar en ny användare. Kräver att ett objekt skickas med.                   |
|POST   |/api/login          |Loggar in en registrerad användare.                                               |

Ett objekt returneras/skickas som JSON med följande struktur:
```
  {
    _id: ObjectId('66ce5fcbe00d276d229ce1e2')
    username: "Tomten"
    password: "$2b$10$NMUQlug9rMd4gkvT4YhL.eaB1pM2OlAcusFQhm/yEdLn5VJdEqBQ2"
    created: 2024-08-27T23:22:51.298+00:00
  }
```