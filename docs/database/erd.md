# Adatmodell (ERD) és kényszerek

## Táblák felépítése

### 1. USERS (Felhasználók)
* `id`: INT, **PK** (Primary Key - Elsődleges kulcs, automatikusan növekvő)
* `email`: VARCHAR(255), **UNIQUE** (Egyedi), **NOT NULL** (Kötelező)
* `password_hash`: VARCHAR(255), **NOT NULL** (Titkosított jelszó)

### 2. TASKS (Feladatok)
* `id`: INT, **PK** (Primary Key - Elsődleges kulcs)
* `user_id`: INT, **FK** (Foreign Key - Idegen kulcs, hivatkozás a `USERS.id` mezőre)
* `title`: VARCHAR(100), **NOT NULL**
* `status`: VARCHAR(20), **DEFAULT 'TODO'**, **CHECK** (`status IN ('TODO', 'IN_PROGRESS', 'DONE')`)

## Kapcsolatok (Relationships)
* **USERS (1) — (N) TASKS (Egy a többhöz):** Egy felhasználóhoz több feladat is tartozhat, de minden feladat pontosan egy felhasználóhoz van rendelve.
