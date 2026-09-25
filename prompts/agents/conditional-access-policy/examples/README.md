# 🧪 Conditional Access Policy Agent — Usage Examples

Questa directory contiene esempi operativi per il **Conditional Access Policy Agent**.

Gli esempi mostrano come trasformare requisiti aziendali espressi in linguaggio naturale in policy strutturate.

---

## Scenari

### 1 — Block Legacy Authentication

Bloccare i protocolli di autenticazione legacy.

➡️ [Block Legacy Authentication](01-block-legacy-authentication.md)

---

### 2 — MFA Outside Trusted Networks

Richiedere MFA quando l'accesso avviene fuori dalle reti aziendali.

➡️ [MFA Outside Trusted Networks](02-mfa-outside-trusted-networks.md)

---

### 3 — Require Compliant Device

Richiedere MFA e dispositivo conforme per determinati scenari.

➡️ [Require Compliant Device](03-require-compliant-device.md)

---

### 4 — Block Sensitive Downloads

Utilizzare Defender for Cloud Apps per controllare il download di documenti sensibili.

➡️ [Block Sensitive Downloads](04-block-download-sensitive-data.md)

---

### 5 — MDCA Monitoring

Utilizzare Conditional Access App Control per osservare attività prima dell'enforcement.

➡️ [MDCA Monitoring](05-mdca-monitoring.md)

---

### 6 — Authentication Strength for Administrators

Applicare una Authentication Strength agli amministratori.

➡️ [Admin Authentication Strength](06-admin-authentication-strength.md)

---

# 🎯 Learning Objective

Gli esempi evidenziano tre aspetti differenti:

```text
Natural Language
       │
       ▼
Policy Intent
       │
       ▼
Logical Validation
       │
       ▼
Structured DSL
```

L'agente non deve limitarsi a tradurre il requisito.

Deve anche individuare:

- prerequisiti;
- incompatibilità;
- rischi;
- oggetti mancanti;
- necessità di policy multiple;
- verifiche necessarie prima dell'enforcement.
