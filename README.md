# Koncerty dla Szkół - Strona Internetowa

Profesjonalna strona internetowa dla firmy organizującej koncerty edukacyjne w szkołach.

## 🎵 Funkcje

- **Responsywny design** - działa świetnie na desktop, tablet i mobile
- **Sekcja Hero** - przyciągająca uwagę z statystykami
- **Oferta** - trzy rodzaje koncertów z opisami
- **Artyści** - prezentacja zespołu
- **Galeria** - miejsce na zdjęcia z koncertów
- **Cennik** - trzy pakiety cenowe
- **Kontakt** - formularz kontaktowy i dane firmy
- **Elegancki design** - ciepła paleta kolorów, ładna typografia

## 🚀 Instalacja i uruchomienie

### Wymagania
- Node.js 18 lub nowszy
- npm lub yarn

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

## 📝 Personalizacja

### Zmiana kolorów
Edytuj zmienne CSS w `src/styles/global.css`:
```css
:root {
  --color-primary: #e85d04;    /* Główny kolor */
  --color-secondary: #f48c06;  /* Kolor pomocniczy */
  --color-accent: #faa307;     /* Akcent */
}
```

### Zmiana tekstów
Wszystkie teksty znajdują się w `src/pages/index.astro`. Możesz je łatwo edytować.

### Dodawanie zdjęć
1. Umieść zdjęcia w folderze `public/images/`
2. W pliku `index.astro` zamień placeholdery na:
```html
<img src="/images/twoje-zdjecie.jpg" alt="Opis">
```

### Zmiana czcionek
Edytuj import w `src/layouts/Layout.astro` i zmienne w `global.css`.

## 📂 Struktura projektu

```
koncerty-dla-szkol/
├── src/
│   ├── components/      # Komponenty (Header, Footer)
│   ├── layouts/         # Layout główny
│   ├── pages/          # Strony (index.astro)
│   └── styles/         # Style globalne
├── public/             # Pliki statyczne (zdjęcia, ikony)
└── package.json
```

## 🎨 Sekcje strony

1. **Hero** - Nagłówek z wezwaniem do działania
2. **Oferta** - Trzy rodzaje koncertów
3. **Artyści** - Prezentacja muzyków
4. **Galeria** - Zdjęcia z wydarzeń
5. **Cennik** - Trzy pakiety cenowe
6. **Kontakt** - Formularz i dane kontaktowe

## 🔧 Dalszy rozwój

Możesz dodać:
- Blog z aktualnościami
- System rezerwacji online
- Integrację z kalendarzem
- Referencje i opinie szkół
- Więcej sekcji z informacjami

## 📱 Responsywność

Strona jest w pełni responsywna i działa na:
- Desktop (1200px+)
- Tablet (768px - 1199px)
- Mobile (< 768px)

## 🌐 Hosting

Możesz wdrożyć stronę na:
- Netlify (darmowy)
- Vercel (darmowy)
- GitHub Pages
- Własny hosting

## 📧 Kontakt

W razie pytań dotyczących strony, skontaktuj się z developerem.

---

Stworzone z ❤️ używając Astro
