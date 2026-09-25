# Example 01 — Block Legacy Authentication

## Scenario

L'organizzazione vuole impedire l'utilizzo dei protocolli di autenticazione legacy.

---

## User Prompt

```text
Crea una Conditional Access Policy che blocchi l'autenticazione legacy per tutti gli utenti.

Escludi gli account di emergenza.
```

---

## Expected Concepts

L'agente dovrebbe identificare:

```text
ExchangeActiveSync
OtherClients
```

come client applications interessate.

La policy dovrebbe essere inizialmente:

```text
report_only
```

---

## Expected Pattern

```text
ENTRA_CA_POLICY

SUBJECTS
  include=AllUsers
  exclude=Emergency Access

TARGET
  include=AllResources

client_apps =
  List(
    ExchangeActiveSync,
    OtherClients
  )

GRANT=block
```

---

## Learning Point

Il termine:

```text
Legacy
```

è un alias del DSL.

L'agente deve tradurlo nei client type appropriati invece di trattarlo come una condizione nativa generica.
