# Example 02 — MFA Outside Trusted Networks

## Scenario

L'organizzazione vuole richiedere MFA quando gli utenti accedono fuori dalle reti aziendali.

---

## User Prompt

```text
Per tutti gli utenti richiedi MFA quando l'accesso avviene fuori dalle nostre reti aziendali.

Le Named Location aziendali sono:

ITALIA
HQ-FI
VPN-CORP

Escludi gli account Emergency Access.
```

---

## Expected Pattern

```text
NETWORK
  include=AnyNetwork
  exclude=List(
    NamedLocation("ITALIA"),
    NamedLocation("HQ-FI"),
    NamedLocation("VPN-CORP")
  )

GRANT =
  allow require_all=[
    mfa
  ]
```

---

## Learning Point

La policy non significa:

> "Le reti aziendali sono sicure."

Significa semplicemente:

> "Il requisito MFA aggiuntivo viene applicato quando l'accesso non proviene dalle Named Location indicate."

La posizione di rete non deve essere considerata da sola una prova di affidabilità dell'identità o del dispositivo.
