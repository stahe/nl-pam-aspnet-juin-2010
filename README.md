# [Ontwikkeling van een drielaagse webapplicatie met ASP.NET 2.0, C#, Spring.Net en NHibernate (2010)](https://stahe.github.io/nl-pam-aspnet-juin-2010/)

Dit document beschrijft de stapsgewijze ontwikkeling van **SimuPaie**, een .NET-applicatie die bedoeld is om de loonberekening voor kinderopvangmedewerkers te simuleren. De rode draad is tweeledig: **het opzetten van een duidelijke softwarearchitectuur** en **het implementeren van de oplossing met de toenmalige .NET-technologieën**. Het document beschrijft met name een **drielaagse architectuur**, bestaande uit een gegevenslaag (DAO), een bedrijfslaag en een presentatielaag, die allemaal zijn geïntegreerd via **Spring IoC**.

## Doelstellingen van de cursus

De casestudy heeft tot doel te laten zien hoe een onderhoudbare webapplicatie kan worden ontworpen door de verantwoordelijkheden duidelijk te scheiden:

- **Laag 1 - DAO**: toegang tot gegevens die in de database zijn opgeslagen.
- **Laag 2 - Bedrijfslogica**: loonberekeningen en functionele regels.
- **Laag 3 - UI**: interactie met de gebruiker en weergave van de resultaten.
- **Integratie** van de lagen via **.NET-interfaces** en **afhankelijkheidsinjectie met Spring IoC**.

Het document beschrijft ook de verwerkingscyclus van een gebruikersverzoek: het verzoek wordt door de applicatie ontvangen, indien nodig doorgestuurd naar de bedrijfslogica-laag en vervolgens naar de gegevenslaag, waarna een passend antwoord naar de klant wordt teruggestuurd.

## Opeenvolgende versies van de applicatie

De ondersteuning beperkt zich niet tot één enkele implementatie. Er worden verschillende varianten van SimuPaie aangeboden om diverse architecturale en interface-benaderingen te illustreren:

1. een **ASP.NET-versie met één formulier** in een eenlaagse architectuur;
2. een gelijkwaardige versie, uitgebreid met **Ajax**;
3. een **ASP.NET-versie met drie lagen** met **NHibernate** voor gegevenstoegang;
4. een **versie met meerdere weergaven en één pagina**;
5. een server-side versie gericht op **webservices**;
6. een ASP.NET-clientversie die gebruikmaakt van deze service;
7. een **versie met meerdere weergaven en meerdere pagina’s**;
8. een clientversie van de webservice;
9. een drielaagse variant die meer gebruikmaakt van Spring-klassen, waardoor het gebruik van NHibernate wordt vergemakkelijkt;
10. een **FLEX**-clientversie.

## Vereisten

Dit document is vooral bedoeld voor een **gemiddeld** niveau. Het veronderstelt basiskennis van:

- **ASP.NET**
- **C# 2008**: klassen, interfaces, overerving, polymorfisme
- **Spring IoC / afhankelijkheidsinjectie**
- **drielaagse webarchitectuur** en het **MVC**-model.

## Besproken tools en technologieën

De casestudy is gebaseerd op een samenhangend geheel van tools en frameworks:

- **Visual C# 2008**
- **Visual Web Developer Express 2008**
- **SQL Server Express 2005**
- **Spring.Net / Spring IoC**
- **NHibernate**
- **NUnit** voor unit-tests.

## Wat deze repository te bieden heeft

Dit materiaal is met name interessant voor lezers die:

- inzicht willen krijgen in de implementatie van een **n-laags architectuur** in een .NET-omgeving;
- willen zien hoe de presentatie, de bedrijfslogica en de gegevenstoegang van elkaar kunnen worden **gescheiden**;
- het gebruik van **Spring.Net** voor het samenstellen van componenten willen ontdekken;
- de integratie van **NHibernate** in een ASP.NET-webtoepassing willen bestuderen;
- een leertraject willen volgen dat loopt van een eenvoudige versie naar meer geindustrialiseerde versies.

## Inhoud van het lesmateriaal

Het document beschrijft de algemene architectuur van de applicatie en illustreert vanaf de eerste pagina, aan de hand van een schema, de rol van de gebruiker, de applicatie, de drie lagen en Spring IoC bij de coördinatie van het geheel. Het dient dus zowel als **cursus architectuur**, **ontwerpgids** als **werkbasis voor een praktische implementatie**.

