# Scenario 3 — Microsoft 365 Copilot Business Case

## 🎯 Obiettivo didattico

Mostrare come Researcher e Analyst possano contribuire a due dimensioni differenti della stessa decisione di investimento.

---

# 🏢 Scenario

L'organizzazione sta valutando l'adozione di Microsoft 365 Copilot.

La domanda iniziale potrebbe sembrare:

> **"Quanto costa Copilot?"**

Ma una decisione aziendale richiede almeno due valutazioni differenti:

1. **L'investimento ha senso strategicamente?**
2. **L'investimento è economicamente sostenibile?**

Researcher e Analyst possono contribuire alle due dimensioni.

---

# Step 1 — 🔎 Researcher

Utilizzare:

➡️ [Microsoft 365 Copilot Adoption Strategy](../../../prompts/agents/researcher/copilot-adoption-strategy.md)

---

## Researcher deve valutare

- casi d'uso;
- benefici;
- rischi;
- governance;
- sicurezza;
- readiness;
- prerequisiti;
- gestione del cambiamento;
- possibili scenari di adozione.

---

## 🔍 Cosa osservare durante la demo

Researcher non dovrebbe partire dall'assunto:

> "Copilot deve essere adottato."

Deve invece confrontare scenari differenti:

```text
NON ADOTTARE
      │
      ├── PILOTA
      │
      └── ADOZIONE ESTESA
```

e valutare evidenze a favore e contro ciascuna opzione.

---

# Step 2 — 📊 Analyst

Fornire ad Analyst un dataset contenente variabili economiche come:

```text
Dipendenti
Costo orario
Ore risparmiate
Costo licenza
Adozione prevista
```

Utilizzare:

➡️ [Business Case ROI](../../../prompts/agents/analyst/business-case-roi.md)

---

## Analyst deve verificare

- costo annuale;
- beneficio potenziale;
- ROI;
- break-even;
- payback period;
- scenari;
- sensitivity analysis.

---

# 🔍 Cosa osservare durante la demo

Il valore della sensitivity analysis è particolarmente importante.

Ad esempio:

> "Il business case è positivo soltanto se il risparmio medio supera una determinata soglia di tempo per utente."

Questo permette di trasformare una discussione generica sulla produttività in una **condizione quantitativamente verificabile**.

---

# 💡 Messaggio della demo

Researcher risponde:

> **"L'investimento ha senso strategicamente?"**

Analyst risponde:

> **"A quali condizioni l'investimento è economicamente sostenibile?"**

La decisione finale rimane responsabilità del decision maker.

---

# 🧠 Pattern

```text
                 INVESTMENT DECISION
                         │
             ┌───────────┴───────────┐
             │                       │
             ▼                       ▼
        RESEARCHER                ANALYST
             │                       │
       Strategic Value          Economic Value
             │                       │
       Risks / Benefits          ROI / Payback
             │                       │
             └───────────┬───────────┘
                         │
                         ▼
                   HUMAN DECISION
```

---

# 🎓 Takeaway

Questo scenario evidenzia bene la complementarità tra i due agenti:

> **Researcher → Strategic Evidence**

> **Analyst → Quantitative Evidence**

> **Human → Decision**

Il valore non deriva quindi dall'utilizzo isolato dell'agente, ma dalla capacità di utilizzare strumenti differenti nelle diverse fasi del processo decisionale.
