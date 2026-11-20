# Üzleti szabályok (Business Rules)

## UC-01: Új feladat létrehozása
* **BR-01 (Kötelező cím):** Minden feladatnak kötelező címet adni (nem lehet üres), hossza maximum 100 karakter lehet.
* **BR-02 (Alapértelmezett státusz):** Új feladat létrehozásakor a feladat automatikusan `TODO` státuszba kerül.

## UC-02: Feladat státuszának módosítása
* **BR-03 (Jogosultság):** Csak a projekt tulajdonosa vagy a feladathoz rendelt felhasználó módosíthatja a feladat státuszát.
* **BR-04 (Érvényes állapotok):** Egy feladat státusza kizárólag a következő három érték valamelyike lehet: `TODO`, `IN_PROGRESS`, `DONE`.
