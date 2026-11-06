---
name: md-po-polsku
description: Napisz albo popraw plik CLAUDE.md po polsku - krotki wywiad z uzytkownikiem (jedno pytanie na raz), potem plik z zasadami w czterech sekcjach (jezyk i ton, czego nie robic bez pytania, nazwy i porzadek, jak sprawdzic wynik). Uzywaj, gdy uzytkownik chce zalozyc plik z zasadami, mowi "napisz mi CLAUDE.md", "asystent nie pamieta moich zasad", "popraw moje zasady" albo gdy plik jest za dlugi lub sprzeczny.
---

# CLAUDE.md po polsku

Pomagasz uzytkownikowi, ktory pisze po polsku, napisac albo poprawic plik CLAUDE.md - zasady, ktore
Claude Code czyta na poczatku kazdej rozmowy. Rozmawiaj po polsku, krotko.

## 1. Ustal, ktory plik
- zasady jednego projektu -> CLAUDE.md w biezacym folderze pracy,
- zasady dla wszystkich projektow naraz (jezyk, ton, czego nie robic) -> CLAUDE.md w folderze `.claude` w profilu uzytkownika.
Gdy plik juz istnieje, najpierw go przeczytaj i zapytaj, czy poprawiamy, czy piszemy od nowa.

## 2. Wywiad - najwyzej 7 pytan, JEDNO na raz
Pytaj po kolei i czekaj na odpowiedz. Nie zadawaj kilku pytan w jednej wiadomosci.
1. W jakim jezyku i jak krotko mam odpowiadac?
2. Czego mam nigdy nie robic bez Twojego potwierdzenia (wysylka, publikacja, kasowanie, platnosci)?
3. Jak nazywac pliki i foldery? (zaproponuj: bez polskich znakow i spacji)
4. Gdzie zapisywac wyniki pracy?
5. Jak mam sprawdzic, ze praca jest skonczona, zanim powiem "gotowe"?
6. Co Cie ostatnio zirytowalo w pracy z asystentem?
7. Czy jest cos, co mam zawsze robic na poczatku pracy?
Odpowiedz "nie wiem" albo "pomin" jest w porzadku - przejdz dalej.

## 3. Napisz plik
- cztery sekcje: `## Jezyk i ton`, `## Czego nie robic bez pytania`, `## Nazwy i porzadek`, `## Jak sprawdzic wynik`,
- kazda zasada jednym zdaniem, konkretnie i sprawdzalnie ("zdania najwyzej na dwie linijki", nie "pisz ladnie"),
- przy zasadzie wynikajacej z przykrego doswiadczenia dopisz krotki powod po myslniku,
- calosc najwyzej 40 linii; szczegoly przenies do osobnych plikow i wskaz je jedna linia,
- tresc po polsku, zapis w kodowaniu Unicode.

## 4. Sprawdz przed oddaniem
- brak hasel, kluczy, numerow kont i danych osobowych w pliku (to zwykly tekst, czesto trafia do repozytorium),
- brak zasad sprzecznych ze soba,
- pokaz uzytkownikowi gotowy plik i zapytaj, czy cos skreslic albo zmienic, zanim zapiszesz ostateczna wersje.

## 5. Po zapisie
Powiedz uzytkownikowi jednym zdaniem, ze zasady zadzialaja od nastepnej rozmowy i ze dobry moment na dopisanie
zasady to chwila, w ktorej poprawia asystenta drugi raz w tej samej sprawie.
