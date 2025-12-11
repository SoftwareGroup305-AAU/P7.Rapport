# Rettelser og Kommentarer

## Kritiske Mangler (Niveau 1)
Disse ting skal fikses, da de enten er direkte fejl i rapporten eller indikerer manglende indhold ift. studieordningen.

| Fil | Linje (ca.) | Fejl/Mangel | Kommentar |
| :--- | :--- | :--- | :--- |
| `sections/contribution.tex` | 31 | `\todo{Det her er ikke rigtigt. Vi bruger SelectorNodes :)}` | **SKAL SLETTES/RETTES.** Teksten beskriver en implementation, som jeres todo siger er forkert. |
| `sections/contribution.tex` | 40 | `\todo{add to appendix}` | Manglende reference til appendix. |
| `sections/contribution.tex` | 45 | `\todo{Burde sættes i forlængelse af introduktionen...}` | En intern note til jer selv. Skal slettes. |
| `sections/contribution.tex` | 63 | `\todo{Burde sættes i forlængelse af introduktionen...}` | En intern note til jer selv. Skal slettes. |
| `sections/contribution.tex` | 70 | `\todo{abbreviation consistency}` | Tjek om I skriver "LSTM" eller "Long Short-Term Memory" konsekvent. |
| `sections/method.tex` | 4-6 | `\todo{Afsnittet skal være mere detaljeorienteret...}` | **Kritisk.** Det ligner at hele introen til metode-afsnittet mangler at blive skrevet færdig, eller at noten bare er glemt. |
| `sections/contribution.tex` | 15 | "previous bar" | **Forklaring mangler.** Som diskuteret tidligere, bør I kort forklare hvad en "bar" er i denne kontekst (candlestick/tidsenhed) for læsere uden finans-baggrund. |
| `sections/contribution.tex` | 86 | "lower beta" | **Forklaring mangler.** Forklar kort hvad Beta-værdien dækker over (volatilitet ift. markedet). |

## Vigtige Rettelser (Niveau 2)
Ting der forbedrer læsbarheden og det faglige niveau.

| Fil | Linje (ca.) | Fejl/Mangel | Kommentar |
| :--- | :--- | :--- | :--- |
| `sections/contribution.tex` | 12 | `\todo{AssetNodes retriever kun en "metric"...}` | Tjek om teksten faktisk er opdateret til at matche denne note, og slet noten. |
| `sections/contribution.tex` | 25 | `\todo{Er ikke med i backtesteren...}` | Hvis "Logic" noder ikke er med i backtesteren, skal I overveje om afsnittet skal omskrives eller om det skal nævnes som "Future Work" eller "Design vs Implementation". |
| `sections/conclusion.tex` | 12 | "...allowed for a an environment..." | **Typo.** Dobbelt "a an". Skal være "allowed for an environment". |

## Kosmetiske Rettelser (Niveau 3)
Sproglige justeringer.

| Fil | Linje (ca.) | Fejl/Mangel | Kommentar |
| :--- | :--- | :--- | :--- |
| `sections/contribution.tex` | 64 | "Communication Strategy" | Overskriften har et punktum til sidst i `\subsection{Communication Strategy}.`. Det bør fjernes for konsistens. |
| `sections/contribution.tex` | 71 | "LSTM Implementation." | Overskriften har et punktum til sidst. Fjern for konsistens med de andre overskrifter. |

## Generel Feedback til Studieordning (Niveau 1 - Strategisk)

**Quality of Service (QoS) & Skalerbarhed:**
Rapporten mangler et tydeligt afsnit om *systemets* performance.
*   **Forslag:** Tilføj et afsnit i `Evaluation` (eller `Experiments`), hvor I måler responstider på API'et eller diskuterer, hvordan systemet håndterer store mængder data (f.eks. "Data Warehouse" performance). Hvis I ikke kan nå at måle det, så skriv et afsnit i `Discussion` om teoretisk skalerbarhed (Microservices, Docker, Async processing).

**UI Evaluering:**
Studieordningen kræver "systematisk evaluering af brugergrænseflade".
*   **Forslag:** Hvis I ikke har lavet en brugertest, så lav en "Heuristic Evaluation" (Nielsen's Heuristics) af jeres eget interface og skriv om det. Det tæller som en systematisk evaluering.
