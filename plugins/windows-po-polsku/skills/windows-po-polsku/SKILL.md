---
name: windows-po-polsku
description: Zasady pracy po polsku na Windows - nazwy plikow bez polskich znakow, zapis plikow w Unicode, cudzyslowy wokol sciezek ze spacjami, sprawdzenie powloki przed poleceniem. Uzywaj przy kazdym tworzeniu plikow i folderow, zapisie tekstu z polskimi znakami i uruchamianiu polecen w PowerShellu albo w powloce z Gita.
---

# Windows po polsku

Pracujesz na komputerze z Windows z uzytkownikiem, ktory pisze po polsku. Odpowiadaj po polsku, krotko.
Ponizsze zasady chronia przed piecioma bledami, ktore na Windows zdarzaja sie najczesciej.

## 1. Nazwy plikow i folderow bez polskich znakow
Tresc plikow moze byc po polsku. Nazwy plikow, folderow i zmiennych - tylko litery ASCII.
- zamiast `raport_wrzesień.txt` pisz `raport_wrzesien.txt`,
- zamiast `Notatki ze spotkań` pisz `notatki_ze_spotkan`.

## 2. Zapis tekstu w Unicode
Starszy PowerShell (wersja 5.1) bez parametru zapisuje pliki w kodowaniu, ktore gubi polskie znaki.
- przy `Set-Content`, `Add-Content` i `Out-File` zawsze dodawaj `-Encoding utf8`,
- po zapisie przeczytaj fragment pliku i sprawdz, czy litery takie jak ą, ę, ł wygladaja poprawnie.

## 3. Sciezki ze spacjami w cudzyslowie
Folder `Moje dokumenty` bez cudzyslowu to dla polecenia dwa osobne slowa.
- kazda sciezke w poleceniu bierz w cudzyslow: `"Moje dokumenty\plan.txt"`,
- nowe foldery robocze zakladaj bez spacji.

## 4. Najpierw sprawdz powloke
Na Windows polecenie moze trafic do PowerShella albo do powloki z Gita. Skladnia sie rozni.
- zanim napiszesz polecenie, ustal, w ktorej powloce zostanie uruchomione,
- w PowerShellu: `$env:NAZWA`, `Get-ChildItem`, `;` miedzy poleceniami (w wersji 5.1 nie ma `&&`),
- w powloce z Gita: `$NAZWA`, `ls`, ukosniki `/` w sciezkach,
- gdy polecenie pada bez jasnego powodu, najpierw sprawdz, czy nie poszlo do zlej powloki.

## 5. Jedno zadanie - jedna rozmowa
Gdy uzytkownik zaczyna nowy, niezwiazany temat, zaproponuj nowa rozmowe. To, co ma przetrwac
(ustalenia, zasady), zapisz w pliku z zasadami projektu, a nie tylko w rozmowie.
