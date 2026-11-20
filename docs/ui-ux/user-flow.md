# UI/UX Tervezés – User Flow

## Tevékenység: Új feladat felvétele a Kanban táblára

1. **Belépés:** A felhasználó megnyitja a Taskflow főoldalát, ahol a Kanban tábla látható három oszloppal (*Todo, In Progress, Done*).
2. **Indítás:** A felhasználó rákattint a *Todo* oszlop tetején található **`+ Új feladat`** gombra.
3. **Adatbevitel:** Megjelenik egy felugró ablak (modal), ahol a felhasználó begépeli a feladat címét a szövegmezőbe.
4. **Mentés:** A felhasználó rákattint a **`Mentés`** gombra.
5. **Visszajelzés:** A rendszer elküldi az adatot a szervernek (`POST /api/tasks`), bezárja a felugró ablakot, és az új feladatkártya azonnal megjelenik a *Todo* oszlopban.
