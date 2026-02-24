# Agencja Artystyczna Pro Arte - Strona Internetowa

Profesjonalna strona internetowa dla agencji organizującej koncerty edukacyjne w szkołach.

## Funkcje

- **Responsywny design** - działa na desktop, tablet i mobile
- **Sekcja Hero** - przyciągająca uwagę z statystykami
- **Oferta** - trzy rodzaje koncertów z opisami
- **Artyści** - prezentacja zespołu
- **Galeria** - zdjęcia z koncertów
- **Cennik** - trzy pakiety cenowe
- **Kontakt** - formularz kontaktowy (Formspree) i dane firmy

## Instalacja i uruchomienie

### Wymagania
- Node.js 18 lub nowszy

### Kroki

1. Zainstaluj zależności:
```bash
npm install
```

2. Uruchom serwer deweloperski:
```bash
npm run dev
```

3. Otwórz przeglądarkę na `http://localhost:4321`

### Build produkcyjny

```bash
npm run build
```

Pliki gotowe do wdrożenia znajdziesz w folderze `dist/`.

## Personalizacja

### Zmiana kolorów
Edytuj zmienne CSS w `src/styles/global.css`:
```css
:root {
  --color-primary: #75b89f;    /* Zielony pastelowy */
  --color-secondary: #e8a484;  /* Morelowy */
}
```

### Zmiana tekstów
Wszystkie teksty znajdują się w `src/pages/index.astro`.

### Dodawanie zdjęć
1. Umieść zdjęcia w folderze `public/images/`
2. W pliku `index.astro` użyj komponentu Astro:
```astro
import { Image } from 'astro:assets';
<Image src="/images/twoje-zdjecie.jpg" alt="Opis" width={800} height={600} />
```

### Zmiana czcionek
Edytuj import w `src/layouts/Layout.astro` i zmienne w `global.css`.

## Struktura projektu

```
pro-arte/
├── src/
│   ├── components/      # Komponenty (Header, Footer)
│   ├── layouts/         # Layout główny
│   ├── pages/           # Strony (index.astro)
│   └── styles/          # Style globalne
├── public/              # Pliki statyczne (zdjęcia, ikony)
└── package.json
```

## Sekcje strony

1. **Hero** - Nagłówek z wezwaniem do działania
2. **Oferta** - Trzy rodzaje koncertów
3. **Artyści** - Prezentacja muzyków
4. **Galeria** - Zdjęcia z wydarzeń
5. **Cennik** - Trzy pakiety cenowe
6. **Kontakt** - Formularz i dane kontaktowe

## Wdrożenie

Strona jest wdrożona na GitHub Pages pod adresem `https://szprx.github.io/pro-arte`.

Deployment odbywa się automatycznie po każdym pushu do gałęzi `master` za pomocą GitHub Actions (`.github/workflows/deploy.yml`).

---

Stworzone używając [Astro](https://astro.build)
