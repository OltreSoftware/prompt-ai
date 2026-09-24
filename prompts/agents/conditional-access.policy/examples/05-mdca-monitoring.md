# Example 05 — MDCA Monitoring

## Scenario

Prima di applicare restrizioni, l'organizzazione vuole osservare il comportamento degli utenti durante le sessioni.

---

## User Prompt

```text
Voglio utilizzare Defender for Cloud Apps per osservare le attività degli utenti su una applicazione prima di introdurre blocchi.

Non voglio ancora applicare restrizioni.

Genera la configurazione logica necessaria.
```

---

## Expected Behaviour

L'agente non dovrebbe automaticamente interpretare il requisito come:

```text
monitor_only
```

se l'obiettivo è osservare attività successive al login.

Dovrebbe valutare:

```text
caac=custom
```

e una:

```text
MDCA_SESSION_POLICY
```

con:

```text
ACTION=audit
```

quando appropriato.

---

## Learning Point

Esiste una differenza tra:

```text
monitorare il login
```

e:

```text
monitorare le attività durante la sessione
```

Il requisito espresso dall'utente deve quindi essere interpretato semanticamente prima di scegliere il controllo.
