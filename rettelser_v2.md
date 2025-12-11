# Rettelser og Anbefalinger

## 1. Uoverensstemmelser mellem Tekst og Implementation
Baseret på jeres egne noter, er der steder hvor rapporten beskriver systemet forkert. Dette bør rettes for at undgå forvirring til eksamen.

| Sektion | Problem | Løsningsforslag |
| :--- | :--- | :--- |
| **Asset Nodes** | Teksten siger Asset Nodes leverer fuld OHLCV data eller metrics. Noten siger de kun leverer en metric, og OHLCV håndteres globalt. | Omskriv til at forklare at Asset Nodes definerer *hvilket* asset der handles, men at selve backtesteren henter den fulde data globalt for at sikre synkronisering. |
| **AI-Nodes Output** | Teksten nævner `now(ai).0` notation. Noten siger I bruger SelectorNodes. | Ret teksten til at forklare, at man kobler en Selector Node på AI-Noden for at udtrække forudsigelsen (f.eks. "Selector Node extracts index 0 from AI output"). |
| **Logic Nodes** | Teksten beskriver separate Logic Nodes. Noten siger logik er indbygget i Condition Nodes. | Slet eller omskriv afsnittet om "Logic". Forklar i stedet under "Conditions", at disse noder kan håndtere sammensatte udtryk (AND/OR) internt. |

## 2. Mangler ift. Studieordning
Disse punkter er nødvendige for at opfylde læringsmålene fuldt ud.

| Krav | Status | Anbefaling |
| :--- | :--- | :--- |
| **"Vurdering af skalerbarhed og QoS"** | **Mangler** | Tilføj et afsnit i `Discussion` (eller `Evaluation`). Diskuter hvordan jeres arkitektur (Microservices, Docker) muliggør skalering. F.eks. "The stateless nature of the Backtest Service allows horizontal scaling by deploying multiple instances behind a load balancer..." |
| **"Systematisk evaluering af brugergrænseflade"** | **Mangler** | Tilføj et kort afsnit i `Evaluation` om UI. Udfør en hurtig "Heuristic Evaluation" (Nielsen's 10 Heuristics) på jeres eget interface. Nævn 3-4 styrker/svagheder fundet ved denne metode. |

## 3. Begrebsafklaring
For at sikre at alle læsere (også censor uden finans-baggrund) er med.

| Begreb | Sted | Handling |
| :--- | :--- | :--- |
| **Bar** | `contribution.tex` (Selectors) | Tilføj parentes: "...previous bar (time step/candlestick)..." |
| **Beta** | `contribution.tex` (LMT afsnit) | Tilføj kort forklaring: "...lower beta (market sensitivity)..." |

## 4. Småting
*   Tjek `sections/conclusion.tex` for typo: "allowed for a an environment".
*   Sørg for konsistens i overskrifter (fjern punktummer i slutningen af overskrifter i `contribution.tex`).
