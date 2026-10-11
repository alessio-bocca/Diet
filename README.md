# Dieta CREA (beta)

App web per iPhone basata sulle tabelle CREA: alimenti, pasti, dieta settimanale, lista della spesa.
I dati restano sul dispositivo; il repository contiene solo l'app.

## Installazione (GitHub Pages)
1. Repository **pubblico** con questi file nella radice: `index.html`, `manifest.webmanifest`, `sw.js`, `apple-touch-icon.png`, `icon-512.png`.
2. Settings → Pages → Deploy from a branch → `main` / `(root)`.
3. Da Safari apri l'indirizzo `https://UTENTE.github.io/REPOSITORY/` → Condividi → Aggiungi alla schermata Home.
4. Usa sempre l'icona sulla Home (ha un archivio dati separato da quello di Safari).

## Backup
- **File**: Utente → Dati e backup → Esporta (cifratura opzionale). Salvalo in File o iCloud Drive.
- **Versioni automatiche**: 15 copie locali, ripristinabili dalla stessa schermata.
- **GitHub privato**: crea un secondo repository **privato** (con README), poi un token *fine-grained*
  (GitHub → Settings → Developer settings → Fine-grained tokens): accesso solo a quel repository,
  permesso *Contents: Read and write*. In app: Dati e backup → GitHub → incolla `utente/repository` e il token.
  Ogni backup è un commit di `dieta-crea/backup.json`: la cronologia di GitHub è la cronologia dei tuoi backup.
  Il token resta solo sul tuo telefono. Non usare mai il repository pubblico dell'app per i dati.

## Aggiornamenti
Carica il nuovo `index.html` (Add file → Upload files, sovrascrive). L'app mostra "App aggiornata · Ricarica".
Per tracciare le versioni crea una *Release* con tag `v0.7.0` e incolla le note da `CHANGELOG.md`:
l'app mostra l'ultima release in Utente → Informazioni.

## Segnalare un problema
Utente → Informazioni → Segnala un problema apre una Issue precompilata con versione e dispositivo.

## Note
Stime nutrizionali generali: non sostituiscono il parere di un medico o di un dietista.
