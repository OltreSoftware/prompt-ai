# Scenario 1 — Strategic Commercial Analysis

## 🎯 Obiettivo didattico

Mostrare come Analyst e Researcher possano essere utilizzati insieme per supportare una decisione strategica.

---

# 🏢 Scenario

L'azienda vuole capire:

- quali servizi stanno crescendo;
- quali stanno diminuendo;
- quali generano maggiore marginalità;
- se i trend osservati internamente riflettono cambiamenti più ampi del mercato.

La decisione da supportare è:

> **Su quali servizi dovrebbe investire maggiormente l'azienda nei prossimi 12-24 mesi?**

---

# Step 1 — 📊 Analyst

Utilizzare:

➡️ [Sales Performance Analysis](../../../prompts/agents/analyst/sales-performance-analysis.md)

Fornire ad Analyst un dataset commerciale contenente, ad esempio:

```text
Cliente
Settore
Servizio
Fatturato
Margine
Anno
```

---

## Cosa deve individuare Analyst

- servizi in crescita;
- servizi in contrazione;
- marginalità;
- concentrazione del fatturato;
- dipendenza da clienti;
- anomalie;
- trend significativi.

---

## 🔍 Cosa osservare durante la demo

Analyst parte dai **dati aziendali strutturati** e produce evidenze quantitative.

Il punto della demo non è il grafico.

Il punto è:

> **Quale segnale emerge dai dati?**

Esempio:

> "I servizi di cybersecurity mostrano una crescita costante mentre alcuni servizi infrastrutturali tradizionali risultano in contrazione."

Questa è un'evidenza interna.

Non sappiamo ancora **perché** stia accadendo.

---

# Step 2 — 🔎 Researcher

Utilizzare:

➡️ [Strategic Market Analysis](../../../prompts/agents/researcher/strategic-market-analysis.md)

Utilizzare come contesto anche le evidenze emerse dall'analisi precedente.

Ad esempio:

```text
Analyst ha evidenziato una crescita significativa dei servizi di cybersecurity e una contrazione di alcuni servizi infrastrutturali tradizionali.

Verifica se questi segnali siano coerenti con l'evoluzione del mercato.
```

---

## Cosa deve individuare Researcher

Researcher cerca di determinare se i segnali individuati da Analyst siano:

- fenomeni interni;
- fenomeni temporanei;
- trend di mercato;
- cambiamenti strutturali;
- opportunità;
- rischi.

---

# 💡 Messaggio della demo

> **Analyst trova il segnale nei dati.**

> **Researcher cerca di capire cosa significa quel segnale.**

La combinazione diventa:

```text
DATI INTERNI
     │
     ▼
  ANALYST
     │
     │ Evidenza
     ▼
 RESEARCHER
     │
     │ Contesto
     ▼
  DECISIONE
```

---

# 🎓 Takeaway

Analyst risponde principalmente alla domanda:

> **"Cosa sta succedendo nei nostri dati?"**

Researcher aiuta invece a rispondere:

> **"Perché potrebbe stare succedendo e cosa significa per la nostra strategia?"**
