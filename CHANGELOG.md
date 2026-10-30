# Changelog

## 1.0.1 — 2026-10-29
- Fix: il salvataggio della configurazione falliva sempre su PrestaShop 9 ("Token di sicurezza non valido"): il token è ora validato con il meccanismo del core (UserTokenManager su PS 9, hash legacy su PS 8).
- Fix: la modifica di un negozio andava in errore su PrestaShop 9 (`meta_title` deve essere un array).
- Fix: il segnaposto del campo di ricerca non è più troncato; il pulsante "Vicino a me" va su una riga propria.

## 1.0.0 — 2026-10-27
- Prima versione, port di `m2-storelocator` 1.2.0 per PrestaShop 8/9.
- Negozi gestiti dal back office (tabella `tc_storelocator_store`, associazione ai negozi PrestaShop per il multistore): indirizzo, coordinate, contatti e orari per giorno.
- Configurazione: attivazione, titolo, URL della pagina, **mappa a scelta (OpenStreetMap di default, oppure Google Maps con chiave API e Map ID)**, zoom, HTML prima/dopo, SEO.
- Pagina front-office con elenco lato server, mappa caricata allo scroll, ricerca, "vicino a me", fumetto con "Indicazioni stradali"; Leaflet 1.9.4 incluso (nessuna CDN).
- Hook di estensione `actionTcStorelocatorStoreFormModifier` e `actionTcStorelocatorStoreSave` per `tcstorepickup`.
- Traduzione italiana.
