# Example 03 — MFA and Compliant Device

## Scenario

L'organizzazione vuole applicare controlli più forti quando gli utenti lavorano fuori sede.

---

## User Prompt

```text
Quando gli utenti accedono fuori dalle reti aziendali richiedi sia MFA sia un dispositivo conforme.

Applica la policy a tutti gli utenti e a tutte le risorse.

Escludi gli account Emergency Access.
```

---

## Expected Pattern

```text
GRANT =
  allow require_all=[
    mfa,
    device_compliant
  ]
```

---

## Expected Prerequisites

L'agente dovrebbe evidenziare almeno:

```text
Microsoft Intune or supported compliance provider

Device registration

Device compliance configuration
```

---

## Learning Point

La parola:

```text
sia
```

implica una relazione logica:

```text
AND
```

e quindi:

```text
require_all
```

non:

```text
require_one
```
