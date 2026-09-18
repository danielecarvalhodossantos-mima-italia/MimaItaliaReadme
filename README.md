# MimaItaliaReadme
Readme pubblico di Mima Italia

Mima Italia (www.mima-italia.it) | Marketplace di matching famiglie/operatori di assistenza
Progetto full-stack progettato, sviluppato e portato in produzione in autonomia, senza supporto di un team tecnico.
Cosa fa:
Piattaforma di matching two-sided che connette famiglie in cerca di assistenza (anziani, disabilità, babysitting) con operatori qualificati (OSS, ASA, educatori, babysitter). Il matching avviene sulla piattaforma; il pagamento del servizio resta tra le parti, Mima genera ricavi tramite commissione per lo sblocco del contatto con il candidato scelto.

Stack tecnico
Frontend: React, Chakra UI
Backend: Node.js su Cloud Functions (serverless)
Database: Firestore (NoSQL)
Autenticazione: Firebase Auth
Pagamenti: Stripe
Mappe/geolocalizzazione: Leaflet + OpenStreetMap
Hosting/CI: Firebase Hosting, GitHub Actions
Il mio ruolo
Full Stack Dev: architettura dati, sviluppo frontend e backend, sicurezza, deploy, monitoring dal primo commit alla produzione con utenti reali attivi su più città italiane.
Problemi tecnici rilevanti risolti
Integrità dei pagamenti: diagnosticato, tramite analisi log dei webhook, un fallimento silenzioso nelle notifiche di pagamento (nessun errore visibile in superficie); ripristinato il flusso e aggiunto monitoring per prevenire regressioni.
Scalabilità query geospaziali: identificato un troncamento silenzioso dei risultati di ricerca in aree ad alta densità, causato da un limite sulle query su indice geospaziale; risolto con una migrazione della struttura dati che supporta letture concorrenti senza downtime.
Autenticazione cross-platform: isolato un bug di login specifico ai WebView in-app (rilevato tramite user-agent detection) che bloccava l'accesso agli utenti provenienti da campagne pubblicitarie, con impatto diretto sul tasso di conversione dell'acquisizione a pagamento.
Performance e SEO multi-pagina: migliorate le Core Web Vitals (LCP, INP) e risolti conflitti di indicizzazione su decine di landing page città (canonical tag, prerendering).
Migrazione dati senza downtime: gestita l'evoluzione dello schema dati su una collection con migliaia di documenti attivi, mantenendo piena retrocompatibilità durante la transizione.
Nota
Il codice sorgente di produzione non è pubblico per ragioni di sicurezza (gestisce pagamenti e dati personali di utenti reali). Questo repository documenta l'architettura e il lavoro tecnico svolto a scopo di portfolio.

