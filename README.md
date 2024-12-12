# Zirka Market Place

Zirka Market Place to nowoczesna, szybka i skalowalna platforma e-commerce zbudowana z użyciem zaawansowanych technologii frontendowych i backendowych. Frontend został stworzony przy użyciu Vite, React i TypeScript, zapewniając intuicyjny interfejs użytkownika.

## Funkcjonalności

- **Responsywny design**: W pełni zoptymalizowany zarówno dla użytkowników komputerów stacjonarnych, jak i urządzeń mobilnych.
- **Zarządzanie produktami**: Dodawanie, przeglądanie i zarządzanie produktami.
- **Koszyk i finalizacja zakupu**: Łatwe dodawanie produktów do koszyka i bezpieczne płatności.
- **Uwierzytelnianie użytkowników**: Funkcjonalność logowania i rejestracji użytkowników.
- **Przeglądanie kategorii**: Eksplorowanie produktów według kategorii.
- **Panel użytkownika**: Dashboard do zarządzania kontem użytkownika.

---

## Technologie

### **Vite**

Vite to narzędzie do budowy aplikacji front-endowych, które zaprojektowano z myślą o szybkości i efektywności. W odróżnieniu od tradycyjnych bundlerów takich jak Webpack, Vite działa w dwóch głównych etapach:

1. **Szybki serwer deweloperski**: Dzięki wykorzystaniu modułów ES (ESM), Vite dostarcza pliki bezpośrednio do przeglądarki bez potrzeby pełnego bundlingu. Skutkuje to niemal natychmiastowym uruchomieniem projektu, nawet w przypadku dużych aplikacji.

2. **Optymalizacja produkcji**: Vite wykorzystuje Rollup jako bundler do budowy zoptymalizowanej wersji aplikacji na produkcję, co zapewnia małe rozmiary paczek i wysoką wydajność.

#### Zalety Vite:

- Natychmiastowy start projektu bez długich czasów kompilacji.
- Obsługa Hot Module Replacement (HMR), która umożliwia szybkie aktualizacje podczas pracy nad kodem.
- Łatwa konfiguracja i integracja z frameworkami takimi jak React, Vue czy Svelte.
- Rozszerzalność dzięki szerokiemu ekosystemowi wtyczek.

Przykład konfiguracji Vite w projekcie:

```javascript
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";

export default defineConfig({
  plugins: [react()],
  server: {
    port: 3000,
  },
});
```

### **React**

React to popularna biblioteka JavaScript służąca do budowania dynamicznych interfejsów użytkownika. Oferuje komponentową strukturę, co pozwala na łatwe zarządzanie nawet skomplikowanymi interfejsami użytkownika.

#### Kluczowe cechy React:

- **Deklaratywność**: Programiści definiują, jak interfejs powinien wyglądać w danym momencie, a React zajmuje się jego aktualizacją w sposób efektywny.
- **Komponentowość**: Interfejs można podzielić na mniejsze, wielokrotnego użytku komponenty, co zwiększa modularność kodu.
- **Virtual DOM**: React korzysta z wirtualnego drzewa DOM, co minimalizuje kosztowne operacje w rzeczywistym DOM i zwiększa wydajność aplikacji.
- **Hooki**: React dostarcza Hooki, które umożliwiają zarządzanie stanem i cyklem życia komponentów w prosty sposób.

Przykład prostego komponentu React:

```tsx
import React, { useState } from "react";

const Counter: React.FC = () => {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Aktualna wartość: {count}</p>
      <button onClick={() => setCount(count + 1)}>Zwiększ</button>
    </div>
  );
};

export default Counter;
```

### **TypeScript**

TypeScript to nadzbiór JavaScript, który wprowadza statyczne typowanie. Dzięki temu programiści mogą wcześniej wykrywać błędy, co zwiększa niezawodność i czytelność kodu.

#### Zalety TypeScript:

- **Statyczne typowanie**: Dzięki definiowaniu typów (np. `string`, `number`, `interface`) można uniknąć wielu błędów związanych z typami danych.
- **Rozszerzalność**: TypeScript umożliwia tworzenie bardziej czytelnych struktur kodu dzięki interfejsom i typom złożonym.
- **Obsługa nowoczesnych funkcji JavaScript**: TypeScript wspiera najnowsze standardy JavaScript, zapewniając jednocześnie kompatybilność wsteczną.
- **Lepsza integracja z IDE**: Dzięki statycznym typom narzędzia takie jak VSCode mogą oferować bardziej precyzyjne podpowiedzi i refaktoryzację.

Przykład użycia TypeScript w aplikacji:

```typescript
interface User {
  id: number;
  name: string;
  email: string;
}

const getUser = (id: number): User => {
  return {
    id,
    name: "Jan Kowalski",
    email: "jan.kowalski@example.com",
  };
};

const user = getUser(1);
console.log(user.name);
```

### **Material-UI**

Material-UI to popularna biblioteka komponentów React, która implementuje wytyczne Material Design opracowane przez Google. Dzięki niej można szybko tworzyć estetyczne i responsywne interfejsy użytkownika.

#### Kluczowe cechy Material-UI:

- **Gotowe komponenty**: Duży wybór komponentów takich jak przyciski, pola tekstowe, tabele, ikony itp.
- **Responsywność**: Komponenty są zaprojektowane tak, aby dobrze wyglądały na różnych urządzeniach.
- **Motywy**: Możliwość dostosowywania wyglądu aplikacji za pomocą własnych motywów.

Przykład wykorzystania Material-UI w projekcie:

```tsx
import React from "react";
import { Button, TextField } from "@mui/material";

const LoginForm: React.FC = () => {
  return (
    <form>
      <TextField label="Email" variant="outlined" fullWidth margin="normal" />
      <TextField
        label="Hasło"
        type="password"
        variant="outlined"
        fullWidth
        margin="normal"
      />
      <Button variant="contained" color="primary" type="submit">
        Zaloguj
      </Button>
    </form>
  );
};

export default LoginForm;
```

---

## Instalacja

Postępuj zgodnie z poniższymi krokami, aby uruchomić projekt lokalnie:

1. **Sklonuj repozytorium**

   ```bash
   git clone https://github.com/josteen1luv/ZirkaMarketplaceUI.git
   cd ZirkaMarketplaceUI
   ```

2. **Zainstaluj zależności**

   ```bash
   npm install
   ```

3. **Uruchom serwer deweloperski**

   ```bash
   npm run dev
   ```

4. **Otwórz aplikację**
   W przeglądarce przejdź do [http://localhost:5173](http://localhost:5173).

---

## Struktura katalogów

```
ZirkaMarketplaceUI/
├── public/             # Zasoby statyczne, takie jak obrazy i ikony
├── src/                # Główne źródła aplikacji
│   ├── api/            # Integracja z API i pliki usługowe
│   ├── features/       # Moduły i funkcje aplikacji
│   │   ├── addProductForm/       # Formularz dodawania produktów
│   │   ├── categoriesList/       # Kategorie produktów
│   │   ├── header/               # Nagłówek aplikacji
│   │   ├── mainCarousel/         # Karuzela z wyróżnionymi produktami
│   │   ├── pages/                # Komponenty stron
│   │   ├── paymentForm/          # Formularz płatności
│   │   ├── productsList/         # Lista produktów
│   │   ├── singleProductItem/    # Szczegóły pojedynczego produktu
│   ├── pages/          # Strony aplikacji
│   │   ├── cart/                # Koszyk użytkownika
│   │   ├── dashBoard/           # Panel zarządzania użytkownika
│   │   ├── mainPage/            # Strona główna
│   │   ├── productsPage/        # Strona listy produktów
│   │   ├── signIn/              # Strona logowania
│   │   ├── signUp/              # Strona rejestracji
│   │   ├── singleProduct/       # Szczegóły produktu
│   ├── store/          # Zarządzanie stanem aplikacji (np. Redux lub Context API)
│   ├── style/          # Style globalne i specyficzne dla komponentów
│   ├── types/          # Typy i interfejsy TypeScript
│   ├── App.tsx         # Główny komponent aplikacji
│   └── main.tsx        # Punkt wejścia aplikacji
├── package.json        # Zależności projektu i skrypty
├── tsconfig.json       # Konfiguracja TypeScript
├── vite.config.ts      # Konfiguracja Vite
└── README.md           # Dokumentacja projektu
```

---

## Skrypty

- `npm run dev`: Uruchamia serwer deweloperski.
- `npm run build`: Buduje projekt do produkcji.
- `npm run preview`: Podgląd wersji produkcyjnej lokalnie.
- `npm run lint`: Uruchamia ESLint w celu sprawdzenia problemów w kodzie.

---

## Problemy podczas implementacji i ich rozwiązania

### Problem: Błąd podczas przesyłania zdjęć na serwer

**Opis:**
Podczas implementacji funkcji przesyłania zdjęć (upload photo) pojawiał się błąd 400 „Bad Request”. Przyczyną problemu było wysyłanie danych w niewłaściwym formacie, co powodowało, że backend nie był w stanie poprawnie odczytać przesyłanego pliku.

**Rozwiązanie:**
Zastosowano `FormData` do poprawnego przesyłania plików w formacie multipart/form-data:

```typescript
import apiClient from "./api";

export const uploadPhoto = async (file: File) => {
  try {
    const formData = new FormData();
    formData.append("photo", file);

    const response = await apiClient.post("/upload", formData, {
      headers: {
        "Content-Type": "multipart/form-data",
      },
    });

    return response.data;
  } catch (error) {
    console.error("Błąd podczas przesyłania zdjęcia:", error);
    throw error;
  }
};
```

**Przykład użycia w komponencie:**

```tsx
import React, { useState } from "react";
import { uploadPhoto } from "../api/photoApi";

const PhotoUpload: React.FC = () => {
  const [file, setFile] = useState<File | null>(null);
  const [message, setMessage] = useState("");

  const handleFileChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    if (e.target.files) {
      setFile(e.target.files[0]);
    }
  };

  const handleSubmit = async (e: React.FormEvent) => {
    e.preventDefault();
    if (file) {
      try {
        const response = await uploadPhoto(file);
        setMessage("Zdjęcie przesłane pomyślnie!");
        console.log(response);
      } catch (error) {
        setMessage("Błąd podczas przesyłania zdjęcia.");
      }
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <input type="file" onChange={handleFileChange} />
      <button type="submit">Prześlij zdjęcie</button>
      <p>{message}</p>
    </form>
  );
};

export default PhotoUpload;
```

---

### Problem: Problemy z logowaniem użytkownika

**Opis:**
Podczas implementacji logowania użytkowników, zdarzało się, że backend odrzucał żądania z kodem błędu 401 „Unauthorized”, mimo poprawnie wprowadzonych danych.

**Rozwiązanie:**
Przyczyną problemu było brakujące nagłówki uwierzytelniające w żądaniach. Dodano obsługę tokenów JWT w Axios:

```typescript
import apiClient from "./api";

export const login = async (credentials: {
  email: string;
  password: string;
}) => {
  try {
    const response = await apiClient.post("/login", credentials);
    const { token } = response.data;
    apiClient.defaults.headers.common["Authorization"] = `Bearer ${token}`;
    return response.data;
  } catch (error) {
    console.error("Błąd podczas logowania:", error);
    throw error;
  }
};
```

**Przykład użycia w komponencie logowania:**

```tsx
import React, { useState } from "react";
import { login } from "../api/authApi";

const LoginForm: React.FC = () => {
  const [email, setEmail] = useState("");
  const [password, setPassword] = useState("");
  const [message, setMessage] = useState("");

  const handleSubmit = async (e: React.FormEvent) => {
    e.preventDefault();
    try {
      const response = await login({ email, password });
      setMessage("Logowanie zakończone sukcesem!");
      console.log(response);
    } catch (error) {
      setMessage("Nie udało się zalogować. Sprawdź swoje dane.");
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="email"
        placeholder="Email"
        value={email}
        onChange={(e) => setEmail(e.target.value)}
      />
      <input
        type="password"
        placeholder="Hasło"
        value={password}
        onChange={(e) => setPassword(e.target.value)}
      />
      <button type="submit">Zaloguj</button>
      <p>{message}</p>
    </form>
  );
};

export default LoginForm;
```

---

### Problem: Błąd podczas edytowania danych użytkownika

**Opis:**
Podczas edytowania danych użytkownika API backendowe zwracało błąd 400 „Bad Request”. Okazało się, że przy wysyłaniu danych brakowało właściwego formatu dla niektórych pól, takich jak numer telefonu.

**Rozwiązanie:**
Dodano walidację danych po stronie frontendu przed wysłaniem ich do API. Zastosowano również odpowiednie formatowanie numeru telefonu:

```typescript
import apiClient from "./api";

export const updateUser = async (
  userId: string,
  userData: { name: string; email: string; phone: string }
) => {
  try {
    // Formatowanie numeru telefonu
    const formattedPhone = userData.phone.replace(/\D/g, "");
    const payload = { ...userData, phone: formattedPhone };

    const response = await apiClient.put(`/users/${userId}`, payload);
    return response.data;
  } catch (error) {
    console.error("Błąd podczas edytowania danych użytkownika:", error);
    throw error;
  }
};
```

**Przykład użycia w komponencie:**

```tsx
import React, { useState } from "react";
import { updateUser } from "../api/userApi";

const EditUserForm: React.FC = () => {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");
  const [phone, setPhone] = useState("");
  const [message, setMessage] = useState("");

  const handleSubmit = async (e: React.FormEvent) => {
    e.preventDefault();
    try {
      const userId = "12345"; // Pobierz z kontekstu użytkownika lub stanu aplikacji
      const response = await updateUser(userId, { name, email, phone });
      setMessage("Dane użytkownika zostały zaktualizowane!");
      console.log(response);
    } catch (error) {
      setMessage("Błąd podczas aktualizacji danych.");
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        placeholder="Imię i nazwisko"
        value={name}
        onChange={(e) => setName(e.target.value)}
      />
      <input
        type="email"
        placeholder="Email"
        value={email}
        onChange={(e) => setEmail(e.target.value)}
      />
      <input
        type="text"
        placeholder="Telefon"
        value={phone}
        onChange={(e) => setPhone(e.target.value)}
      />
      <button type="submit">Zapisz zmiany</button>
      <p>{message}</p>
    </form>
  );
};

export default EditUserForm;
```

### Problem: Błąd podczas realizacji płatności

**Opis:**
Podczas realizacji płatności API backendowe zwracało błąd 500 „Internal Server Error”. Problemem okazało się niewystarczające dane przesyłane w żądaniu płatności, szczególnie brak identyfikatora użytkownika i tokenu uwierzytelniającego.

**Rozwiązanie:**
Zaktualizowano funkcję realizacji płatności, aby upewnić się, że wszystkie wymagane dane są przesyłane w żądaniu:

```typescript
import apiClient from "./api";

export const processPayment = async (paymentData: {
  amount: number;
  paymentMethod: string;
  userId: string;
}) => {
  try {
    const response = await apiClient.post("/payments", paymentData);
    return response.data;
  } catch (error) {
    console.error("Błąd podczas realizacji płatności:", error);
    throw error;
  }
};
```

**Przykład użycia w komponencie płatności:**

```tsx
import React, { useState } from "react";
import { processPayment } from "../api/paymentApi";

const PaymentForm: React.FC = () => {
  const [amount, setAmount] = useState(0);
  const [paymentMethod, setPaymentMethod] = useState("");
  const [message, setMessage] = useState("");

  const handleSubmit = async (e: React.FormEvent) => {
    e.preventDefault();
    try {
      const userId = "12345"; // Pobierz z kontekstu użytkownika lub stanu aplikacji
      const response = await processPayment({ amount, paymentMethod, userId });
      setMessage("Płatność zakończona sukcesem!");
      console.log(response);
    } catch (error) {
      setMessage("Błąd podczas realizacji płatności.");
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="number"
        placeholder="Kwota"
        value={amount}
        onChange={(e) => setAmount(Number(e.target.value))}
      />
      <select
        value={paymentMethod}
        onChange={(e) => setPaymentMethod(e.target.value)}
      >
        <option value="">Wybierz metodę płatności</option>
        <option value="card">Karta</option>
        <option value="BLIK">BLIK</option>
      </select>
      <button type="submit">Zapłać</button>
      <p>{message}</p>
    </form>
  );
};

export default PaymentForm;
```

**Podsumowanie**
Frontend Zirka Market Place został zaprojektowany z myślą o wydajności i łatwości użytkowania. Dzięki zastosowaniu Vite, React i TypeScript, aplikacja oferuje
nowoczesny interfejs użytkownika, który jest zarówno szybki, jak i responsywny. Implementacja została zoptymalizowana pod kątem przyszłego rozwoju, co ułatwia
dodawanie nowych funkcji oraz dostosowywanie aplikacji do zmieniających się wymagań użytkowników.
