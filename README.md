# Aroki Testing Feed — Giaxina

Feed personale **non firmato** di connettori Aroki per il test. Nessun modulo è certificato per la distribuzione: ogni contenuto è "Testing only".

## Importare in Aroki

1. Apri **Profilo → Fonti** nel bridge build.
2. Incolla l'URL esatto dell'indice raw:

   `https://raw.githubusercontent.com/Giaxina/testing-modules-ar/main/index.json`

3. Abilita **Consenti raccolta non firmata** (Allow unsigned collection) e conferma l'avviso.
4. L'app convalida struttura JSON, host HTTPS, checksum e limiti delle richieste, ma non può provare chi ha modificato un repository non firmato.

L'indice è generato con `tools/build-unsigned-index.py` (keyless, per feed personali/test).
Non è il repository ufficiale firmato `kas021/AROKI-Connectors` e non lo sostituisce.

## Connettori

| ID | Nome | Versione | Stato |
| --- | --- | --- | --- |
| animeunity-browse | AnimeUnity | 0.2.0 | active (beta, test) |

## Regole del progetto

- Nessun JavaScript, WebView, credenziali, proxy o comportamento eseguibile nei manifest.
- Nessuna pubblicazione firmata: i candidati ufficiali passano dal flusso `kas021/AROKI-Connectors` (candidate branch → workflow **Publish Aroki connector**, gestito dal maintainer).
- Le modifiche qui vengono versionate: `familyID` resta l'identità, `version` cresce sempre.
