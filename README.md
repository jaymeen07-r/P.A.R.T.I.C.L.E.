# P.A.R.T.I.C.L.E.
Programmable Atomic Radial Task Interface &amp; Command Logic Engine

> **A radial, quantum-inspired command system that turns numbers into actions and memory into structure.**

PARTICALE is a personal operating layer built around a **central core** connected to **150 atomic nodes (atoms)**. Each atom represents a command, file, folder, link, or task, uniquely addressable using a **numeric keypad–driven code system**. The system supports **runtime allocation**, **rollback**, and a **secure personal vault**, making it both flexible and secure by design.

---

## ✨ Core Idea

* A **central core** connects to all atoms using a single line (quantum-style radial structure)
* **150 atoms** positioned at random radii (240–320)
* Each atom is mapped to a **unique numeric code**
* Codes are entered via **numpad input**, enabling muscle-memory–based execution
* Certain reserved codes act as **system controllers**

This project is not just a launcher—it is a **human-centric command kernel**.

---

## 🧬 Atom Classification & Code System

| Category                 | Code Length | Quantity     | Purpose                |
| ------------------------ | ----------- | ------------ | ---------------------- |
| System Master            | 3 digits    | 2            | Runtime control        |
| Standard Atom            | 2 digits    | Multiple     | Common actions         |
| Advanced Atom            | 3 digits    | Multiple     | Semi-critical actions  |
| Absolute Master (Tier-3) | 5 digits    | **Only one** | Secured personal vault |

### 🚫 Invalid Codes

* No 1-digit codes
* No 4-digit codes
* No duplicate codes

---

## 🔐 Reserved System Codes

### `001` – Core Initializer (System Master)

* Runtime creation & update of atoms
* Asks for:

  * Atom number (2 or 3 digits)
  * Friendly name
  * Description
  * Type (URL / folder / file / task / script / workflow)
  * Target value
* Dynamically updates the atom registry without restart

### `002` – Rollback / Removal Controller (System Master)

* Rollback or delete existing atoms
* Supports soft-delete (recommended)
* Cannot remove:

  * `001`
  * `002`
  * Tier-3 (5-digit) atom

---

## 🛡 Tier-3 Atom – Absolute Master (5-Digit)

* **Exactly one 5-digit code**
* Reserved for **personal file structure**
* Protected by **password authentication**
* Completely isolated from system masters (`001`, `002`)

### Tier-3 Capabilities

* Access secured folders
* Launch private scripts
* Navigate personal workflows

### Tier-3 Restrictions

* Cannot create or delete atoms
* Cannot modify system registry
* Cannot trigger rollback

This creates a **dual-root security model**:

* System Root (001 / 002)
* Personal Root (Tier-3)

---

## 🗂 Atom Types Supported

Each atom represents exactly one intent:

* 🌐 `url` – Open a website
* 📁 `folder` – Open a directory
* 📄 `file` – Open a file
* ⚙ `task` – Execute a command
* 🧠 `script` – Run a script
* 🔮 `workflow` – Reserved for future expansion

---

## 📦 Project Structure (Suggested)

```
qacc/
│
├── core/
│   ├── input_handler.py
│   ├── router.py
│   ├── executor.py
│   ├── security.py
│
├── registry/
│   ├── atoms.json
│   ├── deleted_atoms.json
│   ├── tier3_vault.json
│
├── visual/
│   ├── renderer.py   # (optional – Pygame / Canvas)
│
├── main.py
└── README.md
```

---

## ⚙ Runtime Input Flow

```
Numpad Input
   ↓
Digit Buffer
   ↓
Code Match
   ↓
Route Action
```

### Routing Logic (Simplified)

* `001` → Core Initializer
* `002` → Rollback System
* `5-digit` → Tier-3 Password Check → Unlock Vault
* `2/3-digit` → Execute Atom

---

## 🔄 Persistence

* Atom data stored in JSON (initial phase)
* Includes:

  * Position (radius, angle)
  * Metadata
  * Creator
* Rollback atoms are stored separately

Future upgrade: **SQLite / encrypted storage**

---

## 🔮 Roadmap

* Visual quantum renderer (animated core & atoms)
* Encrypted Tier-3 vault (Argon2 / bcrypt)
* Workflow engine
* Audit logs
* Auto-lock vault timer
* Integration with **V.A.S.U.**

---

## 🧠 Philosophy

> *"The fastest interface is the one your brain already remembers."*

PARTICALE blends **visual memory**, **numeric muscle memory**, and **secure execution** into a single abstraction layer—designed for developers, thinkers, and power users.

---

## 📜 License

Personal / Experimental use.
Commercial or redistribution use to be defined.

---

**Author:** Jaymeen Vaghela
**Status:** Active development 🚀
