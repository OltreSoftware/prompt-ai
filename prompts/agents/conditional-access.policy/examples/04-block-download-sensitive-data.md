# Example 04 — Block Sensitive Downloads with MDCA

## Scenario

L'organizzazione vuole consentire l'accesso a SharePoint Online tramite browser ma impedire il download di documenti classificati come sensibili.

---

## User Prompt

```text
Per gli utenti esterni consenti l'accesso a SharePoint Online tramite browser ma utilizza Defender for Cloud Apps per bloccare il download dei documenti con sensitivity label Confidential.

Genera le policy necessarie.
```

---

## Expected Architecture

L'agente dovrebbe comprendere che sono necessari almeno due artefatti:

```text
ENTRA_CA_POLICY
```

per instradare la sessione verso Conditional Access App Control.

e:

```text
MDCA_SESSION_POLICY
```

per applicare il controllo sul file.

---

## Expected Pattern

```text
ENTRA_CA_POLICY
  caac=custom
```

più:

```text
MDCA_SESSION_POLICY

CONTROL=control_file_download

FILTERS
  file_label=Confidential

ACTION=block
```

---

## Learning Point

Questo scenario evidenzia una distinzione importante:

> **Conditional Access decide come gestire l'accesso.**

> **Defender for Cloud Apps può controllare cosa accade durante la sessione browser.**

Il controllo sul contenuto non deve essere rappresentato come un semplice Grant Control Entra.
