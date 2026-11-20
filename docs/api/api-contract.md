# API Szerződés (Interface)

## Kapcsolat a rétegek között
A felhasználói felület (**Frontend**) és az adatbázist kezelő szerver (**Backend**) között egy **REST API** (HTTP protokollon keresztül, JSON adatformátummal) teremt kapcsolatot.

## Végpontok (Endpoints)

| Művelet | Javasolt API metódus és útvonal | Sikeres válasz | Megjegyzés |
| :--- | :--- | :--- | :--- |
| Feladatok listázása | `GET /api/tasks` | `200 OK` | Visszaadja a bejelentkezett felhasználó összes feladatát JSON listában. |
| Új feladat létrehozása | `POST /api/tasks` | `201 Created` | A kérés törzsében (Body) kötelező megadni a `title` mezőt. |
| Feladat státuszának módosítása | `PATCH /api/tasks/{id}` | `200 OK` | Részleges módosítás: csak a `status` mezőt frissíti (pl. `DONE`-ra). |
| Feladat törlése | `DELETE /api/tasks/{id}` | `204 No Content` | Véglegesen törli az adott azonosítójú feladatot az adatbázisból. |
