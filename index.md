---
layout: default
---

# Portofoliu de Laborator – Dezvoltarea Aplicațiilor Mobile

- **Student/ă:** [Gurduza Ion]
- **Grupa:** [IT-2401]
- **Instituția:** [UTM Centrul Universitar "B.P.Hasdeu" din Cahul]

Bine ați venit în portofoliul meu! Aici găsiți lucrările de laborator la disciplina Dezvoltarea Aplicațiilor Mobile: pentru fiecare, o scurtă descriere, arhiva cu codul sursă, un link către Snack și o demonstrație video.

---

## Laboratorul 4: Catalog de produse din API public cu detalii și căutare

- **Descriere:** În această lucrare am creat o aplicație React Native care afișează un catalog de produse încărcat de la API-ul public DummyJSON. Utilizatorul poate deschide un ecran separat cu detaliile fiecărui produs (navigare cu Stack Navigator, pe baza ID-ului), poate căuta produse pe măsură ce scrie și poate filtra lista după categorie. Am adăugat și o listă de favorite, care rămâne la fel pe toate ecranele aplicației.
- **Arhivă cu codul:** [Descarcă lab4.zip](lab4/lab4.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@vane0k/fe9156)
- **Demonstrație video:**

  ![Demo Lab 4](videos/lab4.gif)

---

## Laboratorul 5.1: Încărcare treptată a listei, refresh și mesaje de eroare

- **Descriere:** Scopul lucrării a fost să afișez o listă mare de produse fără a o încărca integral. Cu FlatList și parametrii `limit` și `skip` ai DummyJSON, aplicația aduce produsele pe porții, când utilizatorul ajunge la finalul listei. Tragerea listei în jos o reîmprospătează (RefreshControl). Am tratat separat trei tipuri de erori (la prima încărcare, la refresh și la încărcarea următoarei pagini), fiecare cu propriul mesaj.
- **Arhivă cu codul:** [Descarcă lab5_s1.zip](lab5_s1/lab5_s1.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@[login]/lab5_s1)
- **Demonstrație video:**

  ![Demo Lab 5.1](videos/lab5_s1.gif)

---

## Laboratorul 5.2: Progress bar și cronometru cu hook-uri React

- **Descriere:** Am construit două componente mici, care funcționează independent una de alta. Prima este un progress bar care se umple treptat și arată valoarea în procente. A doua este un cronometru cu butoanele Start, Stop și Reset. Ambele se bazează pe `useState`, `useEffect` și `setInterval`, iar intervalul este oprit corect atunci când nu mai este necesar.
- **Arhivă cu codul:** [Descarcă lab5_s2.zip](lab5_s2/lab5_s2.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@[login]/lab5_s2)
- **Demonstrație video:**

  ![Demo Lab 5.2](videos/lab5_s2.gif)

---

## Laboratorul 6: Login/logout și notițe salvate local

- **Descriere:** Aplicația permite autentificarea și deconectarea utilizatorului prin API-ul DummyJSON. Tokenul primit este stocat local (SecureStore/AsyncStorage), așa încât, la o nouă deschidere a aplicației, utilizatorul rămâne conectat. Fiecare utilizator are propriile notițe, salvate pe dispozitiv și legate de ID-ul său, deci notițele unui cont nu apar la altul.
- **Arhivă cu codul:** [Descarcă lab6.zip](lab6/lab6.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@[login]/lab6)
- **Demonstrație video:**

  ![Demo Lab 6](videos/lab6.gif)

---

## Laboratorul 7: Jurnal foto cu cameră, galerie și scanare de coduri QR

- **Descriere:** Aici am lucrat cu hardware-ul telefonului. Aplicația poate face poze cu camera (`expo-camera`) sau poate alege imagini din galerie (`expo-image-picker`), iar cererea permisiunilor și renunțarea utilizatorului sunt tratate corect. Pozele sunt mutate într-un folder permanent cu `expo-file-system`, pentru a nu dispărea la repornire, iar informațiile despre ele se păstrează în AsyncStorage. În plus, un scanner QR verifică conținutul codului citit înainte de a-l folosi.
- **Arhivă cu codul:** [Descarcă lab7.zip](lab7/lab7.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@[login]/lab7)
- **Demonstrație video:**

  ![Demo Lab 7](videos/lab7.gif)

---

## Laboratorul 8: Harta cafenelelor din apropiere cu geolocație

- **Descriere:** Aplicația determină poziția utilizatorului (`expo-location`) și afișează pe o hartă (`react-native-maps`) cafenelele din jur, preluate din OpenStreetMap. Dacă încărcarea eșuează, se folosesc date de test. Pentru fiecare cafenea calculez distanța cu formula Haversine și ordonez lista de la cea mai apropiată. Poziția este urmărită continuu cu `watchPositionAsync`, iar urmărirea se oprește la părăsirea ecranului. Din aplicație se poate porni și navigarea către locul ales.
- **Arhivă cu codul:** [Descarcă lab8.zip](lab8/lab8.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@[login]/lab8)
- **Demonstrație video:**

  ![Demo Lab 8](videos/lab8.gif)

---

## Laboratorul 9: Aplicație de remindere cu notificări locale

- **Descriere:** Folosind `expo-notifications`, am realizat o aplicație în care utilizatorul își programează remindere: peste un anumit interval, la o oră fixă sau în fiecare zi. Pentru Android am configurat un canal de notificări, iar permisiunea este cerută la momentul potrivit. Lista salvată în AsyncStorage este comparată cu notificările programate în sistem, ca cele două să rămână sincronizate, iar apăsarea pe o notificare deschide aplicația și o gestionează corespunzător.
- **Arhivă cu codul:** [Descarcă lab9.zip](lab9/lab9.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@[login]/lab9)
- **Demonstrație video:**

  ![Demo Lab 9](videos/lab9.gif)

---

## Laboratorul 10: Starea globală cu Context API și temă light/dark

- **Descriere:** Am reorganizat codul aplicației pentru a nu mai transmite datele prin props de la un ecran la altul. Sesiunea utilizatorului este gestionată de `AuthContext`, iar notițele de `NotesContext`, ambele folosite prin hook-uri proprii. Pentru performanță am folosit `useMemo` și `useCallback`, iar logica locală complexă este tratată cu `useReducer`. La final am adăugat un context pentru tema light/dark, a cărei alegere se păstrează după închiderea aplicației.
- **Arhivă cu codul:** [Descarcă lab10.zip](lab10/lab10.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@[login]/lab10)
- **Demonstrație video:**

  ![Demo Lab 10](videos/lab10.gif)

---

## Laboratorul 11: Crearea fișierului APK cu EAS Build

- **Descriere:** Ultima lucrare a avut ca scop obținerea unei aplicații Android care se instalează direct pe telefon, fără Expo Go. Am folosit EAS Build, cu un profil `preview` care produce APK, definit în `eas.json`. Am setat versionarea automată și variabilele `EXPO_PUBLIC_*` necesare la compilare. Înainte de build am rulat `expo-doctor`, care a semnalat problemele din proiect, astfel încât compilarea în cloud să nu eșueze.
- **Arhivă cu codul:** [Descarcă lab11.zip](lab11/lab11.zip)
- **Link util:** [Deschide în Snack](https://snack.expo.dev/@[login]/lab11)
- **Demonstrație video:**

  ![Demo Lab 11](videos/lab11.gif)

---

## Tehnologii utilizate

- **Framework-uri și limbaje:** React Native, Expo, JavaScript
- **Instrumente:** Git, GitHub Pages, VS Code, EAS Build

---

© 2026 – [Gurduza Ion] | Grupa [IT-2401]
