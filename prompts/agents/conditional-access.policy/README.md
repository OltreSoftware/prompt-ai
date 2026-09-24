# 🔐 Conditional Access Policy Agent

**Type:** Custom Declarative Agent  
**Platform:** Microsoft 365 Copilot  
**Technologies:** Microsoft Entra Conditional Access, Microsoft Defender for Cloud Apps  
**Author:** Luca Conte / OltreSoftware

---

## 🎯 Purpose

Conditional Access Policy Agent è un agente dichiarativo progettato per trasformare requisiti espressi in linguaggio naturale in una rappresentazione strutturata di policy per:

- Microsoft Entra Conditional Access;
- Microsoft Defender for Cloud Apps;
- Conditional Access App Control.

L'agente utilizza un **mini-DSL** progettato per rappresentare in maniera leggibile:

- utenti e gruppi;
- target resources;
- network;
- client applications;
- device platforms;
- risk conditions;
- device filters;
- grant controls;
- session controls;
- Conditional Access App Control;
- policy MDCA di accesso e sessione.

---

## 🧠 Design Principle

L'agente non deve semplicemente tradurre una frase in una configurazione.

Deve anche verificare la **coerenza logica della policy**.

Ad esempio:

```text
"Fuori dalla rete aziendale richiedi MFA e dispositivo conforme."
```

può essere trasformato in:

```text
ENTRA_CA_POLICY "Require MFA and compliant device outside trusted networks"

STATE = report_only

SUBJECTS
  include=AllUsers
  exclude=Group(TODO("EMERGENCY-ACCESS-GROUP"))

TARGET
  type=resources
  include=AllResources

NETWORK
  include=AnyNetwork
  exclude=NamedLocation(TODO("TRUSTED-NETWORK"))

CONDITIONS:
  client_apps = Any

GRANT =
  allow require_all=[
    mfa,
    device_compliant
  ]
```

---

## 🛡️ Safety by Design

Le policy generate dall'agente sono considerate **proposte di configurazione**.

Per impostazione predefinita:

```text
STATE = report_only
```

L'agente non deve:

- creare policy;
- modificare policy;
- abilitare policy;
- applicare automaticamente configurazioni.

Prima dell'enforcement devono essere eseguite verifiche appropriate, incluse:

- Conditional Access What If;
- Sign-in logs;
- test con utenti o gruppi pilota;
- verifica degli account Emergency Access;
- verifica dei client interessati;
- verifica delle dipendenze e delle licenze.

---

## 🏗️ Architecture

L'agente distingue tre tipi di artefatto:

```text
ENTRA_CA_POLICY
MDCA_ACCESS_POLICY
MDCA_SESSION_POLICY
```

Questa distinzione è importante perché Microsoft Entra Conditional Access e Microsoft Defender for Cloud Apps svolgono ruoli differenti.

### Microsoft Entra Conditional Access

Determina **se e a quali condizioni l'accesso può avvenire**.

### Defender for Cloud Apps Access Policy

Può controllare **quali sessioni possono accedere alle applicazioni**.

### Defender for Cloud Apps Session Policy

Controlla **cosa può fare l'utente durante una sessione browser proxy tramite Conditional Access App Control**.

---

## 📚 Agent Instructions

Le istruzioni complete dell'agente sono disponibili qui:

➡️ [Agent Instructions](agent-instructions.md)

---

## 🧪 Usage Examples

Sono disponibili diversi scenari operativi:

➡️ [Usage Examples](examples/README.md)

Gli esempi includono:

1. blocco della legacy authentication;
2. MFA fuori dalle reti trusted;
3. richiesta di dispositivo conforme;
4. controllo download tramite Defender for Cloud Apps;
5. monitoraggio MDCA;
6. Authentication Strength per amministratori.

---

## ⚠️ Disclaimer

Gli esempi presenti in questo repository sono forniti a scopo didattico.

Le Conditional Access Policy possono avere un impatto significativo sull'accesso ai servizi Microsoft 365 e alle applicazioni aziendali.

Le configurazioni devono essere validate prima dell'attivazione in ambienti di produzione.
