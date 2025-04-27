# ZuzannaKarwowska_WiktoriaKaszkarot_Grupa3_SystemZarz-dzaniaBiletamiWKinie
Zarządzanie biletami w kinie
Zarządzanie biletami w kinie Cel Biznesowy: 
Celem aplikacji jest umożliwienie użytkownikom (klientom) rezerwacji biletów na seanse kinowe. 
Aplikacja powinna oferować interfejs do przeglądania dostępnych filmów, rezerwowania miejsc na sali kinowej,
a także umożliwiać zarządzanie tymi rezerwacjami przez pracowników kina (administratorów).

1. Użyte Technologie Język programowania:
- C#
- Środowisko: WinForms
- Baza danych: SQLite
- Kontrola wersji: Git
- Zewnętrzne biblioteki: Entity Framework Newtonsoft.Json
2. Funkcjonalności
- Przeglądanie filmów Użytkownicy mogą przeglądać dostępne filmy w kinie.
- Każdy film ma przypisaną nazwę, czas trwania, opis, oraz gatunek.
- Rezerwacja biletów Klienci mogą rezerwować bilety na dostępne seanse.
- Użytkownicy mogą wybierać miejsca na sali kinowej (np. widok siatki z miejscami).
- Po rezerwacji biletów, system generuje unikalny kod rezerwacji.
- Zarządzanie rezerwacjami Administratorzy (pracownicy kina) mogą przeglądać i zarządzać wszystkimi rezerwacjami.
- Administratorzy mogą edytować seanse filmowe (zmiana godziny, sali kinowej) oraz usuwać rezerwacje.
- Obsługa płatności (opcjonalnie) System może integracji z prostą obsługą płatności online (np. symulacja płatności).
- Logowanie Klienci oraz administratorzy mogą się logować do aplikacji, aby móc rezerwować bilety lub zarządzać systemem.
- Raportowanie Administratorzy mogą generować raporty dotyczące sprzedanych biletów (ilość, przychód).

3. Opis Architektury Klasy i Dziedziczenie Film:
a.Reprezentuje film w kinie. Atrybuty:
- ID – unikalny identyfikator filmu.
- Tytuł – tytuł filmu.
- Opis – opis filmu.
- CzasTrwania – czas trwania filmu w minutach.
- Gatunek – gatunek filmu.
b. Seans: Reprezentuje seans filmu w kinie. Atrybuty:
- ID – unikalny identyfikator seansu.
- Film – film przypisany do danego seansu.
- Data – data seansu.
- Godzina – godzina rozpoczęcia seansu.
- Sala – sala kinowa, w której odbędzie się seans.
c. Bilet: Reprezentuje bilet na seans. Atrybuty:
- ID – unikalny identyfikator biletu.
- Seans – seans, na który wystawiony jest bilet.
- Użytkownik – użytkownik, który zakupił bilet.
- Cena – cena biletu.
- Miejsce – miejsce w sali kinowej.
d. Użytkownik: Reprezentuje użytkownika systemu (klienta lub administratora). Atrybuty:
- ID – unikalny identyfikator użytkownika.
- Imie – imię użytkownika.
- Nazwisko – nazwisko użytkownika.
- Email – adres e-mail użytkownika.
- Hasło – hasło użytkownika.
e. Rezerwacja: Reprezentuje rezerwację biletu przez użytkownika. Atrybuty:
- ID – unikalny identyfikator rezerwacji.
- Bilet – bilet przypisany do rezerwacji.
- Status – status rezerwacji (np. "oczekująca", "potwierdzona", "anulowana").

About
Zarządzanie biletami w kinie
Resources
 Readme
 Activity
Stars
 0 stars
Watchers
 0 watching
Forks
 0 forks
Releases
No releases published
Create a new release
Packages
No packages published
Publish your first package
Footer
