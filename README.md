
## 🔧 Wymagania techniczne

- Node.js 18+ (zalecane)
- Możesz używać dowolnych bibliotek npm, chyba że opis wymaga czegoś innego
- Każde zadanie powinno mieć osobny plik `.js` lub folder z `README` i ewentualnie `package.json`

---

## 📌 Zadania

### ✅ Zadanie 1 – [orders.json](https://files.lazienka-rea.com.pl/files/orders.json)

Stwórz funkcję `summarizeOrders`, która zlicza liczbę klientów, sumę przychodów i średnią wartość zamówienia.
```javascript
{
  customers: ["Anna", "John"],
  totalRevenue: 450,
  averageOrderValue: 150
}
```

---

### ✅ Zadanie 2 – [inventory.json](https://files.lazienka-rea.com.pl/files/inventory.json)

1. Napisz funkcję `groupByCategory`, która grupuje SKU według kategorii.
2. Zaimplementuj walidator, który zgłasza błąd, jeśli produkt nie ma wariantów.

---

### ✅ Zadanie 3 – [products.json](https://files.lazienka-rea.com.pl/files/products.json)


Dostajesz tablicę produktów (SKU, name, price, link, imageLink, availability).

Stwórz moduł Node.js, który:
1. Pobierze dane z pliku products.json.
2. Zbuduje plik XML zgodny z minimalnym schematem Google Merchant (tag <rss><channel><item>…).
3. Zapisze wynik jako feed.xml.
---

### ✅ Zadanie 4 – [feed.xml](https://files.lazienka-rea.com.pl/files/feed.xml)

Zaimplementuj CLI:

```bash
node transform.js feed.xml out.json --minPrice=50 --inStock
```
Wymagania:
* Streamuj XML (SAX) – nie ładuj całego do pamięci.
* Konwertuj tylko produkty z price >= minPrice i availability="in_stock".
* Zwrot JSON w formacie: { sku, name, price, currency, availability } (jedna linia = jeden obiekt).

### ✅ Zadanie 5 – [.env](https://files.lazienka-rea.com.pl/files/.env)

1. Pobierz (HTTP GET) publiczny feed XML dostawcy A oraz plik JSON z cenami promocyjnymi dostawcy B (URL-e przekazywane w pliku .env).
2. Deduplikuj produkty po sku (przy kolizji – zachowaj wyższą cenę).
3. Połącz dane tak, by każdy wynikowy rekord zawierał: sku, name, finalPrice, source.
4. Zapisz wynik do report.csv.


---

#### Na koniec wszystko przygotuj w repo na GitHubie i przygotuj link.