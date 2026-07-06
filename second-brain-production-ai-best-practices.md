# Lärdomar & Best Practice — Produktion, AI-workflows och Creative QA

**Syfte:**  
Den här anteckningen sammanfattar arbetssätt, lärdomar, principer och best practice från våren/sommaren 2026 kring produktion, portfolio, interna verktyg, AI-workflows, content systems och creative QA.

Den är skriven för att kunna ligga i Second Brain som ett levande referensdokument för hur Christoffer bör tänka, producera, prompta, kvalitetssäkra och kommunicera framåt.

---

## 1. Övergripande lärdom

Den stora lärdomen från våren är att Christoffers styrka inte bara ligger i att producera visuellt material, utan i att bygga system som gör produktionen snabbare, tydligare och mer konsekvent.

Det som återkommer i nästan alla projekt är detta:

> Bra produktion handlar inte bara om output. Det handlar om struktur, prioritering, kvalitetssäkring och att minska friktionen mellan idé, beslut och färdig leverans.

Det gör att Christoffer bör positionera sig mindre som “content creator” och mer som en senior producent med stark visuell förmåga, teknisk förståelse och systemtänk.

En starkare formulering av rollen är:

> Senior content producer who builds visual systems — turning product, brand and launch needs into structured, scalable, high-quality output.

---

## 2. Grundprincip: Creative judgment + production structure

En viktig insikt är att kreativ kvalitet och produktionsstruktur inte är två olika spår. För Christoffer hänger de ihop.

Struktur gör inte arbetet mindre kreativt. Struktur gör att det kreativa håller högre nivå oftare.

### Praktisk innebörd

- Tydliga briefar gör att produktionen slipper gissningar.
- Mallar gör att kvaliteten kan upprepas.
- System minskar manuellt dubbelarbete.
- QA-rutiner gör att småfel fångas innan publicering.
- AI-workflows fungerar bäst när de är inbyggda i en tydlig process, inte när de används som lösa genvägar.

### Undvik

- Att sälja in AI som gimmick.
- Att prata om “effektivisering” utan att visa vad som faktiskt blir bättre.
- Att beskriva produktionen som enbart kreativ när det verkliga värdet ligger i kombinationen av hantverk, struktur och skalbarhet.

---

## 3. Christoffers bästa positionering

Den starkaste professionella positioneringen är inte:

> Jag gör foto, video och 3D.

Det är för smalt och för output-fokuserat.

Starkare:

> Jag bygger visuella produktionssystem som hjälper varumärken skapa bättre content snabbare — utan att tappa hantverk, tydlighet eller varumärkeskänsla.

### Positioneringspelare

1. **Senior produktionserfarenhet**  
   Många år inom foto, video, 3D, byrå, frilans och in-house.

2. **Visuell kvalitet och omdöme**  
   Förmåga att se vad som är smakfullt, tydligt, premium och användbart.

3. **Produktionsstruktur**  
   Briefar, mallar, filstruktur, format, exportlogik, launch planning, asset management.

4. **AI och verktygsbyggande**  
   Inte AI för AI:s skull, utan AI som ett sätt att korta väg från behov till färdig produktion.

5. **Affärskoppling**  
   Content ska inte bara se bra ut. Det ska hjälpa lanseringar, e-com, ads, sälj, varumärke och intern effektivitet.

---

## 4. Bästa sättet att använda AI i Christoffers arbete

AI fungerar bäst för Christoffer när den används som:

- senior bollplank
- creative QA
- strukturhjälp
- promptförfattare
- textredaktör
- processdesigner
- systemtänkare
- kodbrief-generator för Claude Code
- second brain-redaktör
- dokumentationsmotor

AI fungerar sämre när den används som:

- lös copygenerator utan kontext
- allmän inspirationsmaskin
- smakdomare utan referenser
- ersättning för tydlig brief
- verktyg för att “bara göra något snyggt”

### Best practice

Ge AI tydlig roll, mål, kontext och begränsningar.

Exempel:

```text
Agera som senior art director och rekryterare. Stress-testa först. Identifiera vad som är svagt, spretigt eller otydligt. Ge sedan en konkret förbättringsplan och en prompt jag kan klistra in i Claude Code.
```

Det har fungerat bättre än vaga prompts som:

```text
Gör detta bättre.
```

---

## 5. Prompting-principer som fungerat bäst

### 5.1 Be alltid om kritik före förbättring

Den bästa arbetsordningen har varit:

1. Granska hårt.
2. Identifiera svagheter.
3. Förklara varför det inte fungerar.
4. Föreslå bättre riktning.
5. Skriv färdig prompt eller färdig text.

Det hindrar AI från att bara putsa på dåliga idéer.

### 5.2 Be om “senior judgment”, inte bara “förbättra”

Bra formuleringar:

- “Agera som senior art director.”
- “Agera som senior rekryterare.”
- “Agera som creative QA.”
- “Stress-testa detta innan du förbättrar det.”
- “Var hård mot svag logik och generiska formuleringar.”
- “Prioritera tydlighet, smak och execution.”

### 5.3 Be AI skydda befintliga funktioner

När Claude Code används för appförbättringar ska prompten nästan alltid innehålla:

```text
Viktigt: ändra inte befintlig funktionalitet som redan fungerar. Gör förändringen isolerat, regressionssäkert och med tydlig QA efteråt.
```

Detta är avgörande eftersom kodassistenter ofta förbättrar en sak men råkar förstöra annat.

### 5.4 Be om hel prompt, inte lösa råd

Christoffer har fått bäst användning av AI när outputen är en färdig prompt att klistra in i Claude Code.

Bra slutbeställning:

```text
Ge mig nu en komplett prompt jag kan klistra in i Claude Code. Den ska vara tydlig, hård och praktisk. Den ska inkludera mål, constraints, implementation details, QA och vad som absolut inte får ändras.
```

---

## 6. Claude Code — Best Practice

Christoffers workflow med Claude Code har blivit starkast när ChatGPT används som strategisk briefare före Claude Code.

### Rekommenderad kedja

1. Christoffer beskriver problemet visuellt eller funktionellt.
2. ChatGPT stress-testar och strukturerar behovet.
3. ChatGPT skriver en tydlig Claude Code-prompt.
4. Claude Code implementerar.
5. Christoffer exporterar/skärmdumpar resultat.
6. ChatGPT agerar QA och skriver nästa korrigerande prompt.

### Claude Code-promptar bör alltid innehålla

- Vad problemet är.
- Varför det är ett problem.
- Vilket beteende som ska finnas efter fix.
- Vad som inte får ändras.
- Vilka filer/komponenter Claude ska inspektera.
- Hur lösningen ska QA-testas.
- Vad Claude ska rapportera efter implementation.

### Standardstruktur för Claude Code-prompt

```text
Du ska agera som senior product engineer och UX-minded production tool designer.

Problem:
[Beskriv problemet konkret]

Mål:
[Beskriv önskat beteende]

Constraints:
- Ändra inte befintliga funktioner som redan fungerar.
- Gör förändringen isolerad och regressionssäker.
- Behåll nuvarande visuella system där det fungerar.
- Undvik onödig refaktorering.

Implementation:
[Detaljerad beskrivning av funktion/UI/logik]

QA:
- Testa huvudflödet.
- Testa edge cases.
- Kontrollera att gamla funktioner fortfarande fungerar.
- Rapportera exakt vad som ändrats.
```

---

## 7. Interna verktyg — viktiga principer

Christoffers Content Hub, Launch Hub, Ad Creator och bildverktyg ska inte ses som små interna hobbyverktyg. De är början på ett produktionssystem.

### Grundprincip

> Verktygen ska minska friktion, minska manuella fel och göra det lättare att producera konsekvent material i flera format.

### Viktiga designprinciper

- UI ska vara lugnt, tydligt och produktionsmässigt.
- Funktioner ska kännas som professionella verktyg, inte experiment.
- Export ska aldrig försämra bildkvalitet om originalet håller hög kvalitet.
- Presets ska spara tid, inte skapa låsning.
- Manuella justeringar behövs där kvalitet kräver kontroll.
- Allt ska kunna användas snabbt under verklig launch-stress.

---

## 8. Ad Creator — specifika lärdomar

Ad Creator är ett av de tydligaste exemplen på hur Christoffer kan skala produktion.

### Styrka

Verktyget löser ett verkligt produktionsproblem: att skapa många annonsformat snabbt utan att varje format blir manuellt layoutarbete.

### Viktiga förbättringsprinciper

- Zoom och pan måste kännas som professionella designverktyg.
- Exportkvalitet får inte degradera produktbilder.
- Safe frames och formatlogik måste vara pålitliga.
- Linked text och stage exports sparar mycket tid.
- Verktyget ska kunna hantera både snabb produktion och exakt finjustering.

### Kvalitetsrisker

- Bildexport kan förstöra fina detaljer som strängar, greppbräda och metall.
- För hård nedskalning kan ge mjukhet och artefakter.
- Canvas-baserad export kan ge sämre resultat om resolution, pixel ratio eller encoding inte hanteras rätt.
- JPG/PNG-komprimering måste styras medvetet.

### QA-check för Ad Creator

- Kontrollera 100% crop på strängar, bandstavar, logotyp och konturer.
- Jämför export mot originalbild.
- Testa 1:1, 4:5, 9:16 och 16:9 separat.
- Kontrollera både skärmvisning och faktisk nedladdad fil.
- Undvik att skala ner mer än nödvändigt.
- Behåll högre pixelstorlek när plattformen tillåter det.

---

## 9. Launch Hub — specifika lärdomar

Launch Hub bör byggas som en praktisk kontrollcentral, inte bara en visuell lista.

### Ett launch-kort bör snabbt visa

- Produkt/projekt
- Lanseringsdatum
- Status
- Viktigaste asset-gap
- Produktbild om den finns
- Nästa beslut eller nästa leverans
- Vem som blockerar eller äger frågan

### Viktig princip

> En launch-vy ska minska behovet av Slack-frågor.

Om kortet inte hjälper Christoffer se vad som är oklart, vad som saknas och vad som behöver göras härnäst, är det för dekorativt och för lite produktionsnyttigt.

---

## 10. Product Image Scaler / bildverktyg — lärdomar

Produktbilder är ett område där kvalitet snabbt kan förstöras av tekniska detaljer.

### Viktig princip

> Produktbilder måste behandlas som högkvalitativa original, inte som generiska webbfiler.

### Risker

- För aggressiv komprimering.
- Fel färgrymd.
- Fel pixel ratio.
- Canvas-export som inte respekterar originalupplösning.
- Upprepad öppning/export i flera verktyg.
- Automatiserad resizing utan visuell QA.

### Best practice

- Arbeta från högsta tillgängliga original.
- Exportera i större dimension än minsta plattformskrav om det ger bättre kvalitet.
- Kontrollera detaljer i 100% zoom.
- Ha separata exportprofiler för e-com, ads och social.
- Bevara transparent PNG där friläggning kräver det.
- Använd JPG endast där filstorlek/format kräver det.

---

## 11. Portfolio / CV — viktigaste lärdomar

Portfolion ska inte försöka visa allt. Den ska snabbt visa varför Christoffer är värdefull.

### Svaghet som återkom

Många versioner blev för mastiga, för spretiga eller för “inzoomade”. Det betyder inte att innehållet var svagt, utan att hierarkin inte var tillräckligt hård.

### Starkare princip

> En rekryterare eller CMO ska förstå Christoffers värde på 10–20 sekunder.

### Startsidan måste svara snabbt på

1. Vem är han?
2. Vad gör han?
3. Varför är det affärsmässigt relevant?
4. Vilka bevis finns?
5. Vad ska jag klicka på först?

### Undvik

- För långa texter.
- För många likvärdiga case.
- För mycket intern terminologi.
- Rubriker som låter smarta men inte säger något konkret.
- “Creative production” utan tydlig affärskoppling.

### Starka formuleringar

```text
I build visual content systems for product-led brands.
```

```text
Senior production across photography, video, 3D and AI-assisted workflows — built to support launches, e-commerce and brand growth.
```

```text
From product cutouts to launch campaigns, I create the visual systems that make content faster, sharper and easier to reuse.
```

---

## 12. Portfolio-case — rekommenderad struktur

Varje case bör vara byggt för snabb förståelse.

### Rekommenderad case-struktur

1. **Case title**  
   Kort, konkret, produktionsnära.

2. **One-line summary**  
   Vad var projektet och varför spelade det roll?

3. **My role**  
   Vad ägde Christoffer?

4. **Challenge**  
   Vad var problemet?

5. **Solution**  
   Vad byggdes/producerades?

6. **Output**  
   Vilka assets, format, filmer, bilder, system?

7. **Result / business value**  
   Vad blev bättre? Snabbare? Tydligare? Mer skalbart?

8. **System learning**  
   Vad kan återanvändas nästa gång?

### Viktig princip

> Visa inte bara vad som gjordes. Visa vad det löste.

---

## 13. Case-titlar — lärdomar

Bra case-titlar ska vara korta, konkreta och visa vilken typ av problem som löstes.

Exempel på bättre riktning:

- **E-commerce Visual Rollout**
- **Launch Content System**
- **Arc TILT Tremolo Launch**
- **Product Image Workflow**
- **Ad Creator System**
- **Visual Launch Kit**
- **Content Hub Prototype**

Undvik titlar som blir för långa eller för akademiska:

- “E-commerce Relaunch — Visual Content & Quality Standard”
- “Creative Production Framework for Multi-Channel Asset Delivery”

Sådana titlar låter större än de behöver och blir mindre mänskliga.

---

## 14. Copywriting — lärdomar

Den bästa copy-stilen för Christoffer är:

- konkret
- mänsklig
- rak
- lite torrt självsäker
- produktionsnära
- utan AI-fluff
- utan corporate-polish

### Undvik formuleringar som

- “passionate about storytelling”
- “leveraging creativity and technology”
- “seamless workflows”
- “elevating brands through content”
- “innovative solutions”
- “at the intersection of art and technology”

De är för generiska och säger inte tillräckligt.

### Föredra formuleringar som

```text
I turn unclear content needs into structured production systems.
```

```text
I build the assets, templates and workflows that help product launches move faster without looking cheaper.
```

```text
My work sits between craft and structure: product photography, film, 3D, launch content, asset systems and AI-assisted production tools.
```

---

## 15. Visual QA — återkommande principer

Christoffers visuella QA bör alltid titta efter:

- Är hierarkin tydlig?
- Syns produkten snabbt?
- Känns det premium eller bara “snyggt”? 
- Är kontrasten för hård eller för platt?
- Finns det onödiga visuella element?
- Har bilden rätt tyngd och balans?
- Är bakgrunden stödjande eller konkurrerande?
- Är texten lätt att läsa i rätt format?
- Fungerar asseten i faktisk kanal, inte bara i designläget?

### Hård regel

> Om en visuell effekt inte hjälper produkt, budskap eller känsla — ta bort den.

---

## 16. Produktbakgrunder / texture plates — lärdomar

För Strandberg-produktbilder har bakgrunderna fungerat bäst när de är premium, återanvändbara och inte för illustrativa.

### Bra bakgrundslogik

- Bakgrunden ska stödja gitarrens finish.
- Den ska kännas fysisk, inte AI-slumpad.
- Den ska fungera bakom frilagda produktbilder.
- Den ska gå att återanvända över format.
- Den ska ha subtil variation utan att störa konturen.

### Undvik

- För mycket dramatik.
- För starka mönster nära kroppen.
- AI-typiska “coola” abstrakta former.
- Bakgrunder som känns mer kampanj än produktpresentation när syftet är e-com/ads.

### Exempel på stark riktning

För svart bas / svart produkt:

- matt mörk grafit
- subtil relief
- låg kontrast
- mjuka svepande former
- kontrollerad edge-light-känsla
- inga tydliga symboler eller gimmickmönster

---

## 17. Strandberg content — strategisk lärdom

Strandberg behöver inte bara fler assets. Strandberg behöver tydligare asset-system.

### Skillnaden

**Fler assets:**  
Mer material produceras, men det blir fortfarande lätt rörigt.

**Asset-system:**  
Materialet planeras, produceras, namnges, exporteras och återanvänds enligt tydliga regler.

### Christoffers värde

Christoffer kan bidra med:

- launch kits
- produktbildstandard
- annonsmallar
- formatpaket
- e-com visuellt underlag
- Storyblok/SharePoint-struktur
- content hub
- intern dokumentation
- AI-baserade produktionshjälpmedel

Detta är mer strategiskt än att bara “ta fram content”.

---

## 18. Intern kommunikation — lärdomar

En återkommande lärdom är att Christoffer bör kommunicera mer beslutande och mindre valideringssökande.

### Svag kommunikation

```text
Vad tycker ni om att vi kanske gör så här?
```

### Starkare kommunikation

```text
Jag föreslår att vi gör så här. Det löser X, minskar Y och ger oss Z. Om ingen ser en blocker kör jag vidare enligt detta.
```

### Best practice

- Presentera färdiga förslag.
- Be om beslut, inte allmän input.
- Gör ansvar tydligt.
- Ställ inte öppna frågor när du egentligen behöver ett ja/nej.
- Var tydlig med vad som är blockerat.
- Säg vad som händer om inget beslut tas.

---

## 19. Launch-beställningar — viktig arbetsregel

För att Christoffer ska kunna leverera bra på 60% eller i lean team krävs tydliga content-beställningar.

### Grundregel

> Ingen tydlig beställning, ingen full produktion.

Det betyder inte att vara rigid. Det betyder att skydda kvalitet och tid.

### En content-beställning bör innehålla

- Produkt/projekt
- Lanseringsdatum
- Primära kanaler
- Required assets
- Nice-to-have assets
- Format
- Deadlines
- Ägare/godkännare
- Copy/messaging-status
- Produktbildstatus
- Eventuella blockers

### Bra formulering internt

```text
För att jag ska kunna planera produktionen behöver jag en tydlig asset-beställning: vilka format, vilka kanaler, deadline och vem som godkänner. Annars riskerar vi att producera fel saker eller behöva göra om i slutet.
```

---

## 20. Affärskoppling — viktigaste sättet att beskriva output

Christoffer bör nästan alltid koppla content till ett affärs- eller produktionsvärde.

### Istället för

```text
I created product photos and campaign assets.
```

### Skriv

```text
I created a reusable visual asset package for launch, e-commerce and paid social — reducing manual layout work and giving the team consistent material across channels.
```

### Bra värdeord

- reusable
- scalable
- launch-ready
- format-ready
- production-safe
- channel-specific
- faster handoff
- fewer manual steps
- clearer ownership
- consistent product presentation

---

## 21. Vad som gör output senior

Senior output kännetecknas inte av att det är mer avancerat. Det kännetecknas av att det är mer avvägt.

### Senior output är

- tydlig
- genomförbar
- konsekvent
- kanalmedveten
- lätt att använda
- fri från onödiga effekter
- byggd för verkliga deadlines
- begriplig för andra i teamet
- kopplad till ett tydligt syfte

### Junior output är ofta

- överdesignad
- för förklarande
- för beroende av personens egen kontroll
- full av visuella idéer utan prioritering
- imponerande i mockup men svår i produktion

---

## 22. AI-baserad creative QA — standardcheck

När Christoffer ber AI granska något visuellt/textmässigt bör denna check användas.

```text
Agera som senior creative QA. Stress-testa detta innan du förbättrar det.

Granska utifrån:
- tydlighet
- hierarki
- smaknivå
- varumärkeskänsla
- produktionsbarhet
- kanalrelevans
- onödig komplexitet
- generiska formuleringar
- visuella detaljer som stör
- vad en CMO/rekryterare/kund förstår på 10 sekunder

Ge först en hård diagnos. Ge sedan konkret förbättringsförslag. Avsluta med en färdig prompt eller färdig version jag kan använda.
```

---

## 23. AI-baserad copy QA — standardcheck

```text
Agera som senior redaktör. Gör texten mer konkret, mänsklig och direkt.

Ta bort:
- AI-generiska formuleringar
- corporate fluff
- vaga adjektiv
- upprepningar
- överförklaringar
- text som försöker låta smart men inte säger något

Behåll:
- min intention
- min röst
- konkret produktionsverklighet
- tydlig affärskoppling

Ge mig en färdig version.
```

---

## 24. AI-baserad portfolio QA — standardcheck

```text
Agera som senior rekryterare, CMO och art director.

Granska portfolion utifrån:
- förstår man vem jag är inom 10 sekunder?
- syns mitt seniora värde snabbt?
- är hierarkin tillräckligt hård?
- är texterna för mastiga?
- känns layouten premium eller spretig?
- är casen kopplade till affärsnytta?
- känns det som en person med omdöme eller bara många outputs?

Var hård. Föreslå sedan exakt vad som ska ändras.
```

---

## 25. AI-baserad Claude Code promptmall

```text
Du ska agera som senior product engineer, UX designer och production-tool specialist.

Jag bygger ett internt produktionsverktyg. Funktionen fungerar i stort, så du ska inte göra bred refaktorering eller ändra befintlig logik i onödan.

Problem:
[Beskriv problemet]

Mål:
[Beskriv exakt önskat beteende]

Viktiga constraints:
- Bevara all befintlig funktionalitet som redan fungerar.
- Gör förändringen isolerad och lätt att testa.
- Undvik onödiga visuella ändringar.
- Ändra inte dataformat eller exportlogik om det inte är nödvändigt.
- Prioritera robusthet framför snabb kosmetisk lösning.

Implementation:
[Beskriv UI, state, interaktion, edge cases]

QA efter implementation:
- Testa huvudflödet.
- Testa edge cases.
- Kontrollera att gamla funktioner fortfarande fungerar.
- Kontrollera visuella regressions.
- Sammanfatta vilka filer som ändrades och varför.
```

---

## 26. Beslut kring portfolio-ton

Christoffers portfolio bör inte kännas som en designer som försöker imponera med stil. Den bör kännas som en senior producent som har kontroll.

### Ton

- lugn
- konkret
- självsäker
- produktionsnära
- premium utan att vara pyntad
- tydligt affärskopplad

### Bör undvikas

- för mycket animation
- för många färger
- överarbetade case-kort
- långa introtexter
- smarta men oklara headlines
- för mycket tekniskt snack i första vyn

### Bör prioriteras

- stark första mening
- få men tydliga case
- tydlig rollbeskrivning
- bevis på systemtänk
- konkreta outputs
- affärs- och processvärde

---

## 27. Bra formuleringar att återanvända

```text
I build visual content systems for product-led brands.
```

```text
I turn product launches into structured asset systems across e-commerce, paid social and brand channels.
```

```text
My work combines photography, video, 3D and AI-assisted workflows — built around launch needs, product clarity and repeatable quality.
```

```text
I create the assets, templates and workflows that help teams move faster without making the brand feel cheaper.
```

```text
From cutouts and campaign stills to launch films and internal tools, I build production systems that make visual output easier to plan, create and reuse.
```

```text
I work best where craft meets structure: product content, launch systems, visual QA and scalable production workflows.
```

---

## 28. Vanliga fallgropar att bevaka

### 28.1 Att göra allt för stort

Många idéer blir starkare när de smalnas av. Ett case behöver inte visa allt. En funktion behöver inte lösa varje tänkbart scenario.

Fråga:

> Vad är minsta starka versionen?

### 28.2 Att överförklara

När text blir för lång tappar den auktoritet. Särskilt i CV, portfolio och interna presentationer.

Fråga:

> Vilken mening gör störst jobb?

### 28.3 Att låta AI skriva för generiskt

AI vill gärna skriva “smooth”, men Christoffers material blir bättre när det är mer konkret och mindre polerat.

Fråga:

> Skulle detta kunna stå i vem som helst portfolio? Om ja, skriv om.

### 28.4 Att bygga funktioner utan QA-logik

Varje ny appfunktion bör ha tydliga testfall.

Fråga:

> Hur vet jag att detta inte förstörde något annat?

### 28.5 Att fråga efter input när ett beslut behövs

I lean team skapar öppna frågor ofta mer otydlighet.

Fråga:

> Behöver jag feedback, beslut eller bara informera?

---

## 29. Standard för bra Second Brain-noteringar

Second Brain blir mest användbart när anteckningar inte bara sparar information, utan också gör informationen användbar senare.

### Bra anteckning innehåller

- sammanfattning
- beslut
- varför det spelar roll
- praktiska konsekvenser
- viktiga datum
- personer/ägare
- nästa steg
- återanvändbara formuleringar
- länkar till källor/filer

### Mindre bra anteckning

- rå textdump
- lös chattlogg
- otydliga citat
- screenshots utan tolkning
- PDF utan sammanfattning
- idéer utan beslut eller användning

### Rekommenderad struktur

```md
# Titel

## Sammanfattning

## Varför detta är viktigt

## Viktiga detaljer

## Beslut / slutsatser

## Praktisk användning

## Frågor att följa upp

## Relaterade länkar / filer
```

---

## 30. Hur Second Brain bör användas med AI

Second Brain ska inte bara vara arkiv. Det ska vara ett system som gör AI bättre.

### Lägg in

- personliga preferenser
- återkommande arbetsprinciper
- projektbeslut
- varumärkesriktlinjer
- stilregler
- tekniska lösningar
- promptmallar
- casebeskrivningar
- content-system
- viktiga arbetsrelationer
- vad som tidigare fungerat / inte fungerat

### Syftet

När Claude eller ChatGPT läser Second Brain ska den kunna agera mer som en produktionspartner med kontext, inte som en allmän AI.

---

## 31. Bra saker att fortsätta lägga in i Second Brain

- Portfolio-texter och versioner som fungerat.
- Case-strukturer.
- Promptar som gav bra Claude Code-resultat.
- Interna arbetsregler kring launch content.
- Standarder för produktbilder.
- Exportinställningar som fungerar.
- Färg- och stylingprinciper för Strandberg-assets.
- Beslut kring Content Hub.
- Feedback från CEO/CMO/stakeholders.
- Skillnaden mellan vad Christoffer äger och inte äger.
- Personlig positionering och CV-copy.
- Vanliga misstag i layout, copy och appfunktioner.

---

## 32. Viktigaste strategiska slutsatsen

Christoffers framtida styrka ligger i kombinationen:

```text
Senior visual production + systems thinking + AI-assisted workflows + business-aware content structure.
```

Det är mer distinkt än att bara vara fotograf, videoproducent, 3D-generalist eller content creator.

Den röda tråden bör vara:

> Jag gör inte bara visuellt material. Jag bygger sättet materialet blir till, kvalitetssäkras och återanvänds.

---

## 33. Kort version att använda som intern profil

```text
Christoffer är en senior content producer med bakgrund inom foto, video, 3D och in-house produktion. Hans styrka ligger i att kombinera visuellt hantverk med produktionsstruktur, systemtänk och AI-assisterade workflows.

Under 2026 har fokus utvecklats från enbart assetproduktion till att bygga återanvändbara produktionssystem: Content Hub, Launch Hub, Ad Creator, produktbildsflöden, launch kits, portfolio-struktur och Second Brain-dokumentation.

Den viktigaste arbetsprincipen är att kvalitet inte ska bero på ad hoc-insatser. Den ska byggas in i briefar, mallar, format, exportlogik, QA och tydligt ägarskap.
```

---

## 34. Framtida arbetsregel

När ett nytt projekt, case, verktyg eller contentbehov dyker upp, börja alltid med dessa frågor:

1. Vad är det verkliga problemet?
2. Vem behöver använda outputen?
3. Vilket beslut eller vilken handling ska outputen hjälpa?
4. Vilka format krävs?
5. Vad kan återanvändas?
6. Vad måste kvalitetssäkras?
7. Vad är minsta starka versionen?
8. Vilken del bör systematiseras för nästa gång?

---

## 35. Slutprincip

Det starkaste arbetssättet framåt är inte att göra mer. Det är att göra rätt saker mer strukturerat.

> Färre lösa outputs. Fler tydliga system. Mindre gissning. Mer kvalitet inbyggd från början.
