# Example 06 — Authentication Strength for Administrators

## Scenario

L'organizzazione vuole applicare un metodo di autenticazione più forte agli amministratori.

---

## User Prompt

```text
Crea una Conditional Access Policy per gli amministratori che richieda una Authentication Strength resistente al phishing.

Applica la policy a tutte le risorse.

Escludi gli account Emergency Access.

Non conosco ancora il nome della Authentication Strength configurata nel tenant.
```

---

## Expected Behaviour

L'agente non deve inventare il nome della Authentication Strength.

Deve utilizzare un placeholder.

---

## Expected Pattern

```text
auth_strength(
  TODO("AUTH_STRENGTH_NAME_OR_ID")
)
```

La policy dovrebbe inoltre contenere:

```text
STATE=report_only
```

e appropriate:

```text
VALIDATION
WARNINGS
```

---

## Learning Point

Questo scenario mostra un principio importante dell'agente:

> **Quando manca un'informazione tenant-specific, l'agente non deve inventarla.**

Deve invece produrre una configurazione strutturalmente valida utilizzando un placeholder esplicito.
