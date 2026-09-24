# Scenario 2 — Cost Optimization

## 🎯 Obiettivo didattico

Mostrare come combinare analisi quantitativa e ricerca strategica per valutare opportunità di riduzione dei costi.

---

# 🏢 Scenario

L'azienda vuole ridurre i costi operativi senza introdurre rischi o inefficienze maggiori del beneficio economico ottenuto.

La domanda non è semplicemente:

> **"Dove possiamo spendere meno?"**

ma:

> **"Dove possiamo ottimizzare i costi senza compromettere il valore prodotto?"**

---

# Step 1 — 📊 Analyst

Utilizzare:

➡️ [Cost Optimization](../../../prompts/agents/analyst/cost-optimization.md)

Fornire ad Analyst un dataset contenente i costi aziendali.

---

## Analyst deve identificare

- categorie di costo in crescita;
- anomalie;
- fornitori rilevanti;
- variazioni nel tempo;
- possibili aree di ottimizzazione;
- impatto economico di differenti scenari di riduzione.

---

## 🔍 Cosa osservare durante la demo

Analyst può evidenziare, ad esempio:

> "La categoria Software Subscription è cresciuta del 28% negli ultimi due anni."

oppure:

> "Tre fornitori rappresentano il 65% dell'incremento complessivo dei costi."

Queste sono **evidenze quantitative**.

Non sappiamo ancora se sia opportuno intervenire.

---

# Step 2 — 🔎 Researcher

Selezionare una delle categorie individuate da Analyst.

Utilizzare:

➡️ [Cost Alternatives Analysis](../../../prompts/agents/researcher/cost-alternatives-analysis.md)

Researcher analizzerà:

- alternative disponibili;
- costi;
- rischi;
- lock-in;
- complessità di migrazione;
- impatto operativo;
- competenze necessarie;
- time-to-value.

---

# 💡 Messaggio della demo

Analyst risponde principalmente alla domanda:

> **"Dove potrebbe esistere un'opportunità di ottimizzazione?"**

Researcher aiuta invece a rispondere:

> **"Quale alternativa ha più senso e quali conseguenze potrebbe avere?"**

---

# 🧠 Pattern

```text
COST DATA
    │
    ▼
 ANALYST
    │
    │ Opportunity
    ▼
RESEARCHER
    │
    │ Alternatives + Risks
    ▼
 DECISION
```

---

# 🎓 Takeaway

Una riduzione dei costi non è automaticamente una buona decisione.

Analyst può identificare **dove intervenire**.

Researcher può aiutare a valutare **se e come intervenire**.

La decisione finale deve considerare contemporaneamente:

- beneficio economico;
- rischio;
- impatto operativo;
- sostenibilità del cambiamento.
