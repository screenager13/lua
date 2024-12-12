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

# ZirkaMarketPlaceApi - Backend i Baza Danych

## Opis projektu

### Od strony biznesowej
Backend projektu **ZirkaMarketPlaceApi** został zaprojektowany jako zaawansowana platforma marketplace. Jego celem jest zapewnienie stabilnego i skalowalnego zaplecza dla aplikacji frontendowej, umożliwiając obsługę:

1. **Kategorii i Produktów**:
   - Tworzenie, edytowanie i usuwanie kategorii oraz powiązanych produktów.
   - Relacja "One-to-Many" między kategoriami a produktami pozwala na grupowanie produktów w odpowiednich kategoriach.

2. **Użytkowników**:
   - Obsługa rejestracji i logowania użytkowników za pomocą JWT Authentication.
   - Role i uprawnienia zintegrowane z **ASP.Net Identity**.


---

### Od strony technicznej

1. **Technologie Backend**:
   - **ASP.NET Core**: Sercem backendu jest framework .NET Core, oferujący wysoką wydajność i skalowalność.
   - **Entity Framework Core**: Używany jako ORM do zarządzania danymi i migracjami bazy danych.
   - **FluentValidation**: Walidacja danych DTO (Data Transfer Object).
   - **Google Cloud Storage**: Przechowywanie i zarządzanie plikami.
   - **JWT Authentication**: Obsługa uwierzytelniania i autoryzacji użytkowników.
   - **NuGetPacket**: Łatwa praca z API.
   - **Microsoft.Entity.Framework** - łatwa praca z bazą danych

2. **Struktura bazy danych**:
   Baza danych została zaprojektowana w PostgreSQL, co pozwala na efektywne zarządzanie danymi w projekcie. Struktura bazy danych jest zgodna z poniższym schematem:

   **Tabela: AspNetUsers (Identity)**:
   - Kolumny:
     - Id (Guid)
     - FirstName, LastName (string)
     - UserName, NormalizedUserName (string)
     - Email, NormalizedEmail (string)
     - PasswordHash (string)
     - SecurityStamp (string)
     - CreatedDate, UpdatedDate (DateTime)
     - CreatedBy, UpdatedBy (Guid)
     - IsDeleted (bool)

   **Tabela: AspNetRoles**:
   - Kolumny:
     - Id (Guid)
     - Name (string)
     - NormalizedName (string)
     - ConcurrencyStamp (string)

   **Tabela: AspNetUserRoles**:
   - Kolumny:
     - UserId (Guid)
     - RoleId (Guid)

   **Tabela: Categories**:
   - Kolumny:
     - Id (Guid)
     - Name (string)
     - Description (string)
     - PhotoUrl (string)
     - CreatedDate, UpdatedDate (DateTime)
     - CreatedBy, UpdatedBy (Guid)
     - IsDeleted (bool)
   - Relacja:
     - One-to-Many z tabelą **Products**.

   **Tabela: Products**:
   - Kolumny:
     - Id (Guid)
     - Name (string)
     - Description (string)
     - Price (decimal)
     - PhotoUrl (string)
     - AvailableAmount (int)
     - CategoryId (Guid, klucz obcy)
   - Relacja:
     - Many-to-One z tabelą **Categories**.

---

### Relacje w bazie danych
Relacja "One-to-Many" między kategoriami a produktami jest skonfigurowana w następujący sposób:

**Kod w CategoryConfiguration.cs**:
```csharp
builder.HasMany(c => c.Products)
    .WithOne(p => p.Category)
    .HasForeignKey(p => p.CategoryId)
    .OnDelete(DeleteBehavior.Cascade);
``` 
**Kod w ProductConfiguration.cs**:
```csharp
builder.Property(p => p.CategoryId)
    .IsRequired();
```

    
## Struktura projektu i opis folderów

1. **Application**:
   - **Dtos**: Przechowuje modele DTO (np. `ProductDto`, `CategoryDto`), które są używane do przesyłania danych między warstwami aplikacji.
   - **Services**: Zawiera logikę biznesową aplikacji, implementuje usługi do obsługi logiki biznesowej, takie jak `CategoryService` i `ProductService`.
   - **Validators**: Odpowiada za walidację danych wejściowych przy użyciu FluentValidation (np. `ProductDtoValidator`).

2. **Domain**:
   - **Models**: Definicje głównych modeli danych, które reprezentują encje w bazie danych (np. `Product`, `Category`).

3. **Infrastructure**:
   - **Data**: Konfiguracja **Entity Framework Core**, pliki migracji oraz klasy odpowiedzialne za konfigurację bazy danych (np. `ApplicationDbContext`, `CategoryConfiguration`).
   - **Interfaces**: Definiuje interfejsy repozytoriów i usług wykorzystywane w innych częściach aplikacji.
   - **Migrations**: Zawiera migracje bazy danych utworzone przez **Entity Framework Core**.
   - **Options**: Konfiguracja opcji używanych w aplikacji, takich jak walidacja danych lub ustawienia JWT.
   - **Repositories**: Zawiera klasy repozytoriów obsługujące dostęp do danych.

4. **Presentation**:
   - **Controllers**: Odpowiadają za obsługę żądań HTTP (np. `CategoryController`, `ProductController`).
   - **Extensions**: Zawiera rozszerzenia dla aplikacji, np. `AuthenticationExtension` do konfiguracji JWT Authentication.
   - **Middlewares**: Zawiera middleware, np. `GlobalExceptionHandler` do obsługi wyjątków.
   - **Helpers**: Przykładowe funkcje pomocnicze, np. do konwersji plików lub zarządzania danymi wejściowymi.
   - **Services**: Klasy dostarczające różne funkcje wspomagające warstwę kontrolerów.
   - **Program.cs**: Główny punkt wejścia aplikacji, zawierający konfigurację serwera i zależności aplikacji.

## Przykłady kodu

### Walidator dla `ProductDto`:

```csharp
using FluentValidation;
using Application.Dtos;
using Microsoft.Extensions.Options;
using Infrastructure.Options;

namespace Application.Validators
{
    public class ProductDtoValidator : AbstractValidator<ProductDto>
    {
        public ProductDtoValidator(IOptions<ProductValidationOptions> productValidationOptions)
        {
            var productValidation = productValidationOptions.Value;

            RuleFor(p => p.Name)
                .NotEmpty().WithMessage("The 'Name' field is required.")
                .MaximumLength(productValidation.NameMaxLength)
                .WithMessage($"The 'Name' field must not exceed {productValidation.NameMaxLength} characters.");

            RuleFor(p => p.Description)
                .NotEmpty().WithMessage("The 'Description' field is required.")
                .MaximumLength(productValidation.DescriptionMaxLength)
                .WithMessage($"The 'Description' field must not exceed {productValidation.DescriptionMaxLength} characters.");
        }
    }
}
```
### Walidator dla `CategoryDto`:

```csharp
using FluentValidation;
using Application.Dtos;
using Microsoft.Extensions.Options;
using Infrastructure.Options;

namespace Application.Validators
{
    public class CategoryDtoValidator : AbstractValidator<CategoryDto>
    {
        public CategoryDtoValidator(IOptions<CategoryValidationOptions> categoryValidationOptions)
        {
            var categoryValidation = categoryValidationOptions.Value;

            RuleFor(c => c.Name)
                .NotEmpty().WithMessage("The 'Name' field is required.")
                .MaximumLength(categoryValidation.NameMaxLength)
                .WithMessage($"The 'Name' field must not exceed {categoryValidation.NameMaxLength} characters.");

            RuleFor(c => c.Description)
                .NotEmpty().WithMessage("The 'Description' field is required.")
                .MaximumLength(categoryValidation.DescriptionMaxLength)
                .WithMessage($"The 'Description' field must not exceed {categoryValidation.DescriptionMaxLength} characters.");

            RuleFor(c => c.PhotoUrl)
                .NotEmpty().WithMessage("The 'PhotoUrl' field is required.");
        }
    }
}
```
### Serwis do przechowywania plików:

```csharp
using System.Text;
using Application.Interfaces;
using Google.Apis.Auth.OAuth2;
using Google.Cloud.Storage.V1;
using Infrastructure.Options;
using Microsoft.AspNetCore.Http;
using Microsoft.Extensions.Options;

namespace Application.Services
{
    public class FileStorageService : IFileStorageService
    {
        private readonly string _bucketName;
        private readonly StorageClient _storageClient;

        public FileStorageService(IOptions<GoogleStorageOptions> options)
        {
            _bucketName = options.Value.BucketName;
            var credential = GoogleCredential.FromFile(options.Value.CredentialsPath);
            _storageClient = StorageClient.Create(credential);
        }

        public async Task<string> UploadPhotoAsync(IFormFile file, string folder)
        {
            if (file == null || file.Length == 0)
                throw new ArgumentException("File is null or empty", nameof(file));

            var objectName = $"{folder}/{Guid.NewGuid()}_{file.FileName}";

            await using var stream = file.OpenReadStream();
            await _storageClient.UploadObjectAsync(_bucketName, objectName, file.ContentType, stream);
            return $"https://storage.googleapis.com/{_bucketName}/{objectName}";
        }
    }
}
```
### Controller serwisa do przechowywania plików:

```csharp
using Application.Interfaces;
using Microsoft.AspNetCore.Mvc;

namespace Presentation.Controllers
{
    [ApiController]
    [Route("api/file/")]
    public class FileStorageController : ControllerBase
    {
        private readonly IFileStorageService _fileStorageService;

        public FileStorageController(IFileStorageService fileStorageService)
        {
            _fileStorageService = fileStorageService;
        }

        [HttpPost("avatar")]
        public async Task<IActionResult> UploadFile(IFormFile file, [FromQuery] string folder = "avatars")
        {
            try
            {
                var url = await _fileStorageService.UploadPhotoAsync(file, folder);
                return Ok(new { Url = url });
            }
            catch (Exception ex)
            {
                return StatusCode(500, $"Error uploading file: {ex.Message}");
            }
        }
    }
}
```
## Problemy i ich rozwiązania

### Problem: Brak funkcjonalności wylogowania użytkownika
- **Opis problemu**: Aplikacja brakowała funkcji wylogowania użytkownika. Użytkownicy pozostawali zalogowani, nawet jeśli token dostępu oraz odświeżania były przechowywane w plikach cookie. Brakowało mechanizmu, aby usuwać te pliki cookie w momencie, gdy użytkownik wybierał opcję wylogowania.
- **Rozwiązanie**: Dodano metodę `Logout()` do `UserService`, która usuwa pliki cookie o nazwach "AccessToken" i "RefreshToken" z kontekstu HTTP. Dzięki temu po wylogowaniu użytkownika, jego sesja staje się nieważna. Następnie dodano odpowiedni endpoint `POST /logout` w kontrolerze `UserController`, aby umożliwić korzystanie z tej funkcji.
![alt text](image.png)
![alt text](image-1.png)

### Problem: Brak odczytu tokenów z plików cookie w autoryzacji
- **Opis problemu**: W procesie autoryzacji aplikacja nie była w stanie odczytać tokenów JWT przechowywanych w plikach cookie, ponieważ były one oczekiwane jedynie w nagłówkach HTTP (standardowe zachowanie JWT). To ograniczało elastyczność aplikacji, szczególnie w scenariuszach, gdzie tokeny były przechowywane w cookie, np. w aplikacjach SPA.
- **Rozwiązanie**: Dodano zdarzenie `OnMessageReceived` w konfiguracji JWT w `AuthenticationExtensions`. Dzięki temu aplikacja odczytuje token z pliku cookie "AccessToken" i przypisuje go do `context.Token`, co pozwala na jego wykorzystanie w procesie autoryzacji.
![alt text](image-2.png)

### Problem: Nieprawidłowe ustawienia dla odświeżania tokenów w plikach cookie
- **Opis problemu**: W konfiguracji plików cookie brakowało odpowiednich ustawień dla ich wygasania i ochrony. Pliki cookie były mniej bezpieczne i potencjalnie mogły być narażone na kradzież.
- **Rozwiązanie**: Dodano konfigurację plików cookie w `AuthenticationExtensions`, w tym nazwę pliku cookie, ustawienia dla automatycznego wygasania (SlidingExpiration) oraz czas życia (ExpireTimeSpan). Dzięki temu tokeny są automatycznie odświeżane, jeśli użytkownik pozostaje aktywny w aplikacji.
`
![alt text](image-3.png)

### Problem: Nieprawidłowe typy danych w walidatorach i usługach

1. **Opis problemu**:
   - **ProductService** korzystał z walidatora dla `ProductDto`, zamiast dla `CreateProductDto`. Prowadziło to do błędów walidacji, ponieważ struktura `ProductDto` i `CreateProductDto` różniła się.
   - W `ProductDtoValidator` typem walidowanym był `ProductDto`, co było niezgodne z faktycznym użyciem w procesie tworzenia produktu.

2. **Rozwiązanie**:
   - Zmieniono typ walidatora w `ProductService` na `CreateProductDto` oraz dostosowano implementację walidatora `ProductDtoValidator`, aby obsługiwał `CreateProductDto`.

**Kod przed zmianą:**
![alt text](image-4.png)

**Kod po zmianie:** 
![alt text](image-5.png)

**Kod walidatora po zmianie:**
![alt text](code8.png)

### Problem: Nadmiarowe pola w DTO i niepotrzebna logika w kontrolerze

1. **Opis problemu**:
   - `LoginDto` zawierał pola `IsGoogleLogin` i `GoogleToken`, które były wykorzystywane do rozróżniania logowania tradycyjnego i logowania za pomocą Google. Wprowadzało to nadmiarową logikę i zwiększało złożoność DTO oraz kodu kontrolera.
   - W `UserController` znajdowała się rozbudowana logika warunkowa sprawdzająca wartość pola `IsGoogleLogin`, co zwiększało złożoność kodu i utrudniało jego utrzymanie.

2. **Rozwiązanie**:
   - Z `LoginDto` usunięto pola `IsGoogleLogin` i `GoogleToken`.
   - Logikę rozróżniania logowania tradycyjnego i Google przeniesiono na poziom serwisu użytkownika (`UserService`) lub w całości zastąpiono uproszczonym podejściem.
   - W `UserController` uproszczono metodę `LoginUser`, usuwając warunki związane z logowaniem Google.

**Kod przed zmianą**:
![alt text](code9.png)

**Kod po zmianie:**
![alt text](code10.png)

**Kod kontrolera przed zmianie:**
![alt text](code1`.png)

**Kod kontrolera po zmianie:**
![alt text](code12.png)

### Problem: Niespójność w typach danych zwracanych przez metody serwisu i kontrolera

1. **Opis problemu**:
   - Metoda `GetAllCategoriesAsync` w serwisie `CategoryService` zwracała dane typu `IEnumerable<CategoryDto>`, podczas gdy inne metody w serwisie, takie jak `GetCategoryByIdAsync` czy `CreateCategoryAsync`, zwracały dane typu `CategoryResponseDto`.
   - To prowadziło do niespójności w strukturze danych zwracanych przez API oraz mogło powodować trudności w integracji z frontendem.
   - W kontrolerze `CategoryController` występowała niespójność w trasie API — użyto `api/category`, co nie było zgodne z konwencją liczby mnogiej (`api/categories`).

2. **Rozwiązanie**:
   - **Zmiana zwracanego typu**:
     - W metodzie `GetAllCategoriesAsync` zmieniono typ zwracanych danych na `IEnumerable<CategoryResponseDto>`, aby zachować spójność z innymi metodami w serwisie.
     - Zmiana ta wymagała aktualizacji w interfejsie `ICategoryService` oraz odpowiedniej adaptacji danych w implementacji serwisu.
   - **Poprawa trasy API**:
     - W kontrolerze `CategoryController` zmieniono trasę z `api/category` na `api/categories`, co poprawiło czytelność i zgodność z konwencją RESTful.

**Kod serwisu:**
![alt text](code14.png)

**Kod kontrolera przed zmianą:**
![alt text](code16.png)

**Kod kontrolera po zmianie:**
![alt text](code17.png)



### ***Photo z Jiry Dashboard***: 
# *Podsumowanie:*
### Frontend i Backend Zirka Market Place został zaprojektowany z myślą o wydajności i łatwości użytkowania. Dzięki zastosowaniu Vite, React i TypeScript, aplikacja oferuje nowoczesny interfejs użytkownika, który jest zarówno szybki, jak i responsywny. Implementacja została zoptymalizowana pod kątem przyszłego rozwoju, co ułatwia dodawanie nowych funkcji oraz dostosowywanie aplikacji do zmieniających się wymagań użytkowników.
