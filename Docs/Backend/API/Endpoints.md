| Metódus | Útvonal | Hozzáférés | Leírás |
| --- | --- | --- | --- |
| POST | `/api/users/register` | nyilvános | felhasználó regisztráció |
| POST | `/api/users/login` | nyilvános | felhasználó belépés (email + jelszó)|
| POST | `/api/staff/login` | nyilvános | személyzet belépés (username + jelszó)|
| GET | `/api/categories` | nyilvános | kategóriák listája |
| GET | `/api/food-items` | nyilvános | étlap, szűrés: `?category=&q=&maxPrice=` |
| GET | `/api/food-items/:id` | nyilvános | étel adatlap |
| POST | `/api/orders` | nyilvános | rendelés leadása, válaszban a `tracking_token` |
| GET | `/api/orders/track/:token` | token | rendelés állapota, becsült idő, tételek |
| GET | `/api/me` | felhasználó | profil lekérése |
| PUT | `/api/me` | felhasználó | profil módosítása |
| GET | `/api/me/orders` | felhasználó | korábbi rendelések |
| GET | `/api/staff/orders` | személyzet | aktív rendelések, `?status=` szűrővel |
| PATCH | `/api/staff/orders/:id` | személyzet | státusz léptetése, becsült idő megadása |
| POST | `/api/admin/food-items` | admin | étel létrehozása |
| PUT | `/api/admin/food-items/:id` | admin | étel módosítása |
| DELETE | `/api/admin/food-items/:id` | admin | étel „törlése" (`is_available = false`) |
| POST/PUT/DELETE | `/api/admin/categories[/:id]` | admin | kategóriakezelés |
| GET/POST/PUT/DELETE | `/api/admin/staff[/:id]` | admin | munkatársi fiókok kezelése |
| GET | `/api/display/:token` | titkos token | konyhai kijelző: aktív rendelések listája |