# 🏎️ IMR-KiCad-Libraries

Libreria ufficiale **Impulse Modena Racing** per **KiCad**, contenente **symbol**, **footprint** e **modelli 3D** dei componenti utilizzati nei pcb del team.

---

## ⬇️ Download e installazione

### 🔹 Opzione 1 – Clonare la repository (consigliato)

Apri il terminale o prompt dei comandi e clona la libreria:

```bash
git clone https://github.com/bradadano/IMR-KiCad-Libraries.git
````

Posizionala dove preferisci:

* **Linux:**
  `/home/<user>/Documents/KiCad/Libraries/IMR-KiCad-Libraries`
* **Windows:**
  `C:\Users\<user>\Documents\KiCad\Libraries\IMR-KiCad-Libraries`
  
---

## ⚙️ Configurazione in KiCad

### 1. Imposta la variabile d’ambiente

Apri **KiCad → Preferenze → Configura percorsi (Configure Paths)**
Aggiungi una nuova variabile:

| Nome variabile | Percorso                                                                    |
| -------------- | --------------------------------------------------------------------------- |
| `IMR_LIB`      | `/home/<user>/Documents/KiCad/Libraries/IMR-KiCad-Libraries` *(Linux)*      |
| `IMR_LIB`      | `C:\Users\<user>\Documents\KiCad\Libraries\IMR-KiCad-Libraries` *(Windows)* |

---

### 2. Aggiungi le librerie

#### **Symbol Libraries**

1. Vai su **Preferenze → Gestione librerie di simboli (Manage Symbol Libraries)**
2. Clicca su **Aggiungi libreria (Add existing library)**
3. Inserisci il percorso:

   ```
   ${IMR_LIB}/Symbols/<nome_file>.kicad_sym
   ```

#### **Footprint Libraries**

1. Vai su **Preferenze → Gestione librerie di footprint (Manage Footprint Libraries)**
2. Clicca su **Aggiungi libreria (Add existing library)**
3. Inserisci:

   ```
   ${IMR_LIB}/Footprints/IMR_Footprints.pretty
   ```

#### **3D Models**

1. Vai su **Preferenze → Configura percorsi (Configure Paths)**
2. Assicurati che esista la variabile `IMR_LIB`
3. KiCad troverà automaticamente i modelli 3D in:

   ```
   ${IMR_LIB}/3DModels/
   ```

---

## 💻 Aggiornamento della libreria

Per aggiornare la libreria all’ultima versione:

```bash
cd /percorso/della/libreria/IMR-KiCad-Libraries
git pull
```

---

## 🧩 Suggerimenti

* Se lavori in un progetto condiviso, puoi copiare la cartella `IMR-KiCad-Libraries` all’interno della directory del progetto e usare percorsi relativi:

  ```
  ${KIPRJMOD}/Libraries/IMR-KiCad-Libraries/Footprints/IMR_Footprints.pretty
  ```
* Se vuoi contribuire alla libreria, crea un branch e invia una pull request con le modifiche.

---
