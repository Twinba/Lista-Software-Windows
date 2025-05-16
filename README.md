📄 Script Esportazione Lista Software
Questo script permette di generare un file di testo contenente una lista completa di tutti i programmi installati sul tuo PC, prima di procedere alla formattazione. È un utile strumento per avere un inventario dei software da reinstallare dopo aver ripristinato il sistema.

## ⚙️ Funzionalità principali

- ** 🗂️ Esportazione completa**: elenca tutti i programmi installati sui drive C: e D:
  - Software a 64 bit e 32 bit
  - Programmi di terze parti 
  - App di Windows/Microsoft Store
- **ℹ️ Informazioni dettagliate** per ogni programma:
  - Nome
  - Versione
  - Editore/Publisher
  - Data di installazione (quando disponibile)
  - Percorso di installazione
- ** 📝 Formato semplice**: file di testo (.txt) facilmente consultabile
- ** 📅 Nome file organizzato**: include data e ora di esecuzione in formato europeo (GGMMAAAA_HHMM)
- ** 🔌 Nessuna dipendenza**: utilizza solo componenti nativi di Windows

## ⚠️ Limitazioni conosciute

- Alcuni programmi installati potrebbero non avere informazioni complete nel registro di sistema
- Programmi portatili (non installati tramite installer) potrebbero non essere rilevati
- Lo script non può rilevare la configurazione personalizzata dei programmi# Script Esportazione Lista Software

## 📘 Guida all'utilizzo

### 🧰 Prerequisiti
- Sistema operativo Windows (8, 10 o 11)
- Diritti di amministratore (consigliati per risultati completi)

### 💾 Installazione
1. Salva il file `esporta_software.bat` sul tuo computer
2. Posizionalo nella cartella dove desideri salvare l'elenco dei programmi

### ▶️ Esecuzione
1. **Metodo standard**:
   - Fai doppio clic sul file `.bat` per eseguirlo
   - Se ricevi un avviso di sicurezza, clicca su "Esegui comunque"

2. **Per risultati completi** (consigliato):
   - Fai clic destro sul file `.bat`
   - Seleziona "Esegui come amministratore"
   - Questo garantisce che vengano rilevate anche le app di Windows installate per tutti gli utenti

3. **Processo**:
   - Si aprirà una finestra della console che mostrerà l'avanzamento
   - Attendi il completamento dell'operazione (può richiedere da pochi secondi a qualche minuto)
   - Al termine apparirà un messaggio di conferma

4. **Risultato**:
   - Il file di testo verrà creato nella stessa cartella del file .bat
   - Il nome sarà nel formato `lista_software_GGMMAAAA_HHMM.txt` (es. `lista_software_21042025_1530.txt`)
   - Premi un tasto qualsiasi per chiudere la finestra di conferma

### 🔍 Visualizzazione della lista
- Naviga alla cartella dove hai eseguito lo script
- Apri il file .txt generato con qualsiasi editor di testo (es. Blocco note, Notepad++, VS Code)

## 📑 Struttura del file generato

Il file di output è organizzato in sezioni:

```
LISTA DEI PROGRAMMI INSTALLATI - Generata il 21/04/2025 15:30:45
=======================================================================

PROGRAMMI INSTALLATI (Da registro di sistema)
-----------------------------------------------------------------------
Nome: Adobe Acrobat Reader DC
Versione: 23.006.20320
Editore: Adobe Inc.
Data installazione: 20250115
Percorso installazione: C:\Program Files\Adobe\Acrobat Reader DC\
-----------------------------------------------------------------------
...

APP MICROSOFT STORE (UWP)
-----------------------------------------------------------------------
Nome: Microsoft.WindowsCalculator
Versione: 11.2204.1.0
Editore: CN=Microsoft Corporation, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
Percorso installazione: C:\Program Files\WindowsApps\Microsoft.WindowsCalculator_11.2204.1.0_x64__8wekyb3d8bbwe
-----------------------------------------------------------------------
...

RIEPILOGO
-----------------------------------------------------------------------
Totale programmi trovati: 142
File salvato in: C:\Users\Utente\Desktop\lista_software_21042025_1530.txt
```

## 🛠️Risoluzione problemi

### ❌ Lo script si chiude immediatamente
- Eseguilo da Prompt dei comandi:
  1. Apri il Prompt dei comandi (cmd.exe)
  2. Naviga alla cartella dello script con `cd percorso\della\cartella`
  3. Esegui lo script digitando il nome del file

### ❓ Alcune app non vengono rilevate
- Esegui lo script come amministratore
- Le app installate in altre unità diverse da C: e D: non verranno elencate

### 🧪 Errori durante l'esecuzione
- Assicurati che PowerShell sia disponibile sul tuo sistema (preinstallato su Windows 10 e 11)
- Verifica che la policy di esecuzione di PowerShell non blocchi gli script:
  - Se necessario, esegui PowerShell come amministratore e digita:
    `Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process`

## 🔒 Note importanti

- Questo script è sicuro e **non modifica** alcun file di sistema
- I risultati sono generati in tempo reale al momento dell'esecuzione
- Assicurati di conservare il file generato in un luogo sicuro (es. dispositivo USB esterno) prima di formattare il PC
- Lo script non recupera le chiavi di licenza dei programmi, solo le informazioni di installazione
