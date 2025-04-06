# ZuzannaKarwowska_WiktoriaKaszkarot_Grupa3_SystemZarz-dzaniaBiletamiWKinie
Zarządzanie biletami w kinie
Cel Biznesowy
Celem aplikacji jest umożliwienie użytkownikom (klientom) rezerwacji biletów na seanse kinowe. Aplikacja powinna oferować interfejs do przeglądania dostępnych filmów, rezerwowania miejsc na sali kinowej, a także umożliwiać zarządzanie tymi rezerwacjami przez pracowników kina (administratorów).

Użyte Technologie
Język programowania: C#

Środowisko: WinForms

Baza danych: SQLite

Kontrola wersji: Git

Zewnętrzne biblioteki: Entity Framework Newtonsoft.Json

Funkcjonalności
1. Przeglądanie filmów
Użytkownicy mogą przeglądać dostępne filmy w kinie.

Każdy film ma przypisaną nazwę, czas trwania, opis, oraz gatunek.

2. Rezerwacja biletów
Klienci mogą rezerwować bilety na dostępne seanse.

Użytkownicy mogą wybierać miejsca na sali kinowej (np. widok siatki z miejscami).

Po rezerwacji biletów, system generuje unikalny kod rezerwacji.

3. Zarządzanie rezerwacjami
Administratorzy (pracownicy kina) mogą przeglądać i zarządzać wszystkimi rezerwacjami.

Administratorzy mogą edytować seanse filmowe (zmiana godziny, sali kinowej) oraz usuwać rezerwacje.

4. Obsługa płatności (opcjonalnie)
System może integracji z prostą obsługą płatności online (np. symulacja płatności).

5. Logowanie
Klienci oraz administratorzy mogą się logować do aplikacji, aby móc rezerwować bilety lub zarządzać systemem.

6. Raportowanie
Administratorzy mogą generować raporty dotyczące sprzedanych biletów (ilość, przychód).

Opis Architektury
Klasy i Dziedziczenie
Film: Reprezentuje film w kinie.

Atrybuty:

ID – unikalny identyfikator filmu.

Tytuł – tytuł filmu.

Opis – opis filmu.

CzasTrwania – czas trwania filmu w minutach.

Gatunek – gatunek filmu.

Seans: Reprezentuje seans filmu w kinie.

Atrybuty:

ID – unikalny identyfikator seansu.

Film – film przypisany do danego seansu.

Data – data seansu.

Godzina – godzina rozpoczęcia seansu.

Sala – sala kinowa, w której odbędzie się seans.

Bilet: Reprezentuje bilet na seans.

Atrybuty:

ID – unikalny identyfikator biletu.

Seans – seans, na który wystawiony jest bilet.

Użytkownik – użytkownik, który zakupił bilet.

Cena – cena biletu.

Miejsce – miejsce w sali kinowej.

Użytkownik: Reprezentuje użytkownika systemu (klienta lub administratora).

Atrybuty:

ID – unikalny identyfikator użytkownika.

Imie – imię użytkownika.

Nazwisko – nazwisko użytkownika.

Email – adres e-mail użytkownika.

Hasło – hasło użytkownika.

Rezerwacja: Reprezentuje rezerwację biletu przez użytkownika.

Atrybuty:

ID – unikalny identyfikator rezerwacji.

Bilet – bilet przypisany do rezerwacji.

Status – status rezerwacji (np. "oczekująca", "potwierdzona", "anulowana").
