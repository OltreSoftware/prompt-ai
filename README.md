# 📚 Prompt AI – Uso Didattico e Formativo

Raccolta pubblica di prompt utilizzati nei miei corsi, workshop e attività formative dedicate a **Microsoft 365 Copilot**, agli **AI Agent** e all'uso consapevole dell'intelligenza artificiale generativa.

L'obiettivo del repository è fornire esempi pratici e riutilizzabili che mostrino non soltanto *come scrivere un prompt*, ma soprattutto **come utilizzare l'AI per supportare attività e decisioni aziendali reali**.

---

## 🎯 Obiettivi

- Fornire prompt pronti da utilizzare durante corsi e workshop.
- Mostrare casi d'uso aziendali concreti.
- Evidenziare il valore strategico degli agenti Microsoft 365 Copilot.
- Creare una libreria di prompt riutilizzabile indipendentemente dal singolo corso.
- Fornire percorsi didattici specifici per i corsi nei quali i prompt vengono utilizzati.

---

## 🧭 Come è organizzato il repository

Il repository utilizza una struttura **ibrida**.

I prompt vengono mantenuti in una libreria canonica organizzata per agente o capability.

I corsi contengono invece gli scenari didattici e fanno riferimento ai prompt della libreria senza duplicarne il contenuto.

### 🤖 Prompt per agente

La cartella [`prompts`](prompts/README.md) contiene la libreria principale.

Attualmente sono disponibili prompt per:

- [🔎 Researcher](prompts/agents/researcher/README.md)
- [📊 Analyst](prompts/agents/analyst/README.md)

### 🎓 Percorsi per corso

La cartella [`courses`](courses/README.md) contiene i percorsi didattici.

Attualmente:

- [MS-4019](courses/ms-4019/README.md)

---

## 🔎 Come utilizzare i prompt

1. Individua l'agente o il corso di interesse.
2. Apri lo scenario.
3. Segui il collegamento al prompt.
4. Copia il prompt.
5. Personalizza le eventuali variabili indicate tra parentesi quadre.
6. Utilizzalo nell'agente Microsoft 365 Copilot indicato.

Ad esempio:

```text
[SETTORE]
[PERIODO]
[CLIENTE]
[OBIETTIVO]
```

devono essere sostituiti con il contesto reale dell'esercitazione.

---

## 💡 Principio della raccolta

I prompt presenti in questo repository cercano di andare oltre richieste semplici come:

> "Riassumi questo documento."

oppure:

> "Crea un grafico."

L'obiettivo è mostrare come utilizzare l'intelligenza artificiale per attività quali:

- analisi strategica;
- supporto decisionale;
- ricerca approfondita;
- analisi quantitativa;
- individuazione di trend;
- identificazione di anomalie;
- valutazione di rischi e opportunità;
- costruzione di business case;
- confronto tra scenari alternativi.

---

## 🧠 Researcher e Analyst

Una distinzione utile durante i corsi è:

### Analyst

> **What do the data tell us?**

Analyst aiuta a individuare pattern, anomalie, trend ed evidenze quantitative nei dati.

### Researcher

> **What does this mean for the business?**

Researcher aggiunge contesto, ricerca evidenze, confronta fonti e valuta possibili strategie.

### Human

> **What should we do?**

La decisione finale rimane responsabilità della persona.

In sintesi:

> **Analyst → Evidence**  
> **Researcher → Context**  
> **Human → Decision**

---

## ⚠️ Note

I prompt sono forniti principalmente a **scopo didattico e formativo**.

I risultati prodotti dall'intelligenza artificiale devono essere verificati prima di essere utilizzati per decisioni aziendali.

L'accesso alle informazioni aziendali tramite Microsoft 365 Copilot dipende dalle autorizzazioni dell'utente e dalle configurazioni dell'organizzazione.

---

## 📜 Licenza

Questo repository è distribuito con licenza [MIT](LICENSE).

I prompt possono essere utilizzati, modificati e condivisi nel rispetto dei termini della licenza.

---

## 👤 Autore

**Luca Conte**  
OltreSoftware

https://www.oltresoftware.com
