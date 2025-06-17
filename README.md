# 🍹 Kolekcja ulubionych przepisów do koktajli

## 📝 Opis projektu

Aplikacja społecznościowa do dzielenia się przepisami na koktajle. Pozwala użytkownikom tworzyć, edytować i przeglądać
przepisy, oceniać je oraz zapisywać swoje ulubione. Projekt powstał z myślą o pasjonatach domowego miksowania i
kulinariów.

---

## 🔧 Funkcjonalności

### 👤 Użytkownicy

- Rejestracja i logowanie
- Edycja danych profilowych
- Obsługa sesji, autoryzacja i middleware

### 🍸 Przepisy

- Dodawanie przepisów (nazwa, opis, składniki, zdjęcie, instrukcja)
- Edycja i usuwanie własnych przepisów
- Przeglądanie listy koktajli i szczegółowych widoków
- Zapisywanie ulubionych przepisów
- Komentowanie i ocenianie

### 🖥️ Interfejs

- Responsywny wygląd dopasowany do ekranów mobilnych
- Przejrzysta nawigacja
- System powiadomień i komunikatów flash

---

### Struktura projektu

```Kolekcja-ulubionych-przepisów-do-koktajli/
├── controllers/         # Kontrolery obsługujące logikę biznesową
│   ├── przepisController.js   # Logika związana z przepisami
│   └── userController.js      # Logika związana z użytkownikami
│
├── middleware/          # Własne middleware aplikacji
│   ├── auth.js          # Middleware autoryzacji użytkownika
│   └── upload.js        # Obsługa przesyłania zdjęć (multer)
│
├── models/              # Modele danych dla MongoDB (Mongoose)
│   ├── Przepis.js       # Model przepisu koktajlu
│   └── User.js          # Model użytkownika
│
├── public/              # Statyczne pliki (CSS, JS, obrazy)
│
├── routes/              # Definicje tras
│   ├── przepisy.js      # Routing związany z przepisami
│   └── users.js         # Routing związany z użytkownikami
│
├── screenshots/         # Zrzuty ekranu aplikacji do README
│
├── views/               # Szablony EJS do renderowania widoków
│   ├── layouts/         # Układy bazowe HTML
│   ├── partials/        # Header, footer, komunikaty flash
│   ├── przepisy/        # Widoki listy i detali przepisów
│   └── users/           # Widoki rejestracji, logowania, profilu
│
├── .env                 # Zmienne środowiskowe
├── app.js               # Główny plik aplikacji Express
└── package.json         # Plik konfiguracyjny projektu
```

---

### Wykorzystane Biblioteki

- express - framework webowy dla Node.js
- mongoose - ODM (Object Data Modeling) dla MongoDB
- ejs - silnik szablonów
- bcryptjs - hashowanie haseł
- express-session - zarządzanie sesjami
- connect-flash - komunikaty flash
- multer - obsługa przesyłania plików
- dotenv - zarządzanie zmiennymi środowiskowymi
- method-override - obsługa metod HTTP
- express-ejs-layouts - układ szablonów EJS

## ⚙️ Instrukcja uruchomienia

### ✅ Wymagania:

- Node.js v14 lub nowszy
- npm v6 lub nowszy
- MongoDB lokalnie lub w chmurze (np. MongoDB Atlas)
- Express.js v4.21.2
### 🛠️ Instalacja:

## Sklonuj repozytorium:

```bash
git clone https://github.com/hwanlix/Kolekcja-ulubionych-przepis-w-do-koktajli.git
cd Kolekcja-ulubionych-przepis-w-do-koktajli
```

```bash
npm install
```

- Uzupełnić 'PORT' i 'SECRET_KEY' w pliku .env

## Instalacja MongoDB lokalnie

Dla systemu Windows:

- Pobrac instalator ze strony: https://www.mongodb.com/try/download/community
- Zainstaluj MongoDB z domyślnymi ustawieniami.

- Upewnic się, że zaznaczone jest "Install MongoDB as a Service".

- Uruchomić MongoDB.
- Dodać nowe połączenie i skopiwać URI, np. 'mongodb://localhost:27017'
- Odpowiednio uzupełnić 'MONGODB_URI' w pliku .env
### Zainstalować framework Express.js
```npm install express```


### Uruchomić serwer

- Tryb deweloperski (automatycznie restartuje się przy wniesieniu zmian)
  ```npm run dev```
- Tryb produkcyjny
  ```npm start```

Aplikacja będzie dostępna pod adresem http://localhost:PORT odpowiednio z ustawionym w pliku .env portem

---
## Przykładowe dane wejściowe

#### Przy rejestracji pola:
- Nazwa użytkownika - 'test'
- Email - 'test@test.test'
- Hasło - 'testtest' (minimalnie 6 symbołów)
- Potwierdź hasło
#### Przy logowaniu pola:
- Email - 'test@test.test'
- Hasło - 'testtest' (minimalnie 6 symbołów)

#### Przy dodawaniu przypisu pola:
- Nazwa przepisu 
- Czas przygotowania - forma z opcją wyboru od 5 do 60 minut z krokiem w 5 min
- Składniki - Nazwa składnika, ilośc oraz Jednostka  opcją wyboru. Możliwość dodawania wielu składników
- Instrukcje przygotowania 
- Dodanie pliku obrazu 
- Dodanie dowolnych tagów dla wyszukiwania

#### Przy dodawaniu komentarzy pola:
- Twój komentarz (opcjonalnie):
- Ocena w postaci 5 gwiazd do uzupełnienia
- 
#### Przy edytowaniu danych użytkownika pola:
- Nazwa użytkownika
- Email
- Obecne hasło
- Nowe hasło (zgodnie z wymaganiami przy rejestracji minimalnie 6 symbołów)
- Potwierdź nowe hasło

#### Przy dodawaniu do ulubionych:
- Użyć przycisku 'Dodaj do ulubionych'

---
