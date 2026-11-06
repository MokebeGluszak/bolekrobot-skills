# Skille Bolka do Claude Code

Skille z [poradnika bolekrobot.pl](https://bolekrobot.pl/poradniki): Claude Code po polsku, na Windows. Każdy skill to jeden plik z instrukcjami (SKILL.md), bez programów do uruchomienia.

## Instalacja

Wklej jedną linię w terminalu (Windows PowerShell, Git Bash albo terminal macOS/Linux):

### md-po-polsku

Napisz albo popraw plik CLAUDE.md po polsku - krotki wywiad z uzytkownikiem (jedno pytanie na raz), potem plik z zasadami w czterech sekcjach (jezyk i ton, czego nie robic bez pytania, nazwy i porzadek, jak sprawdzic wynik). Uzywaj, gdy uzytkownik chce zalozyc plik z zasadami, mowi "napisz mi CLAUDE.md", "asystent nie pamieta moich zasad", "popraw moje zasady" albo gdy plik jest za dlugi lub sprzeczny.

```
claude plugin marketplace add MokebeGluszak/bolekrobot-skills; claude plugin install md-po-polsku@bolekrobot
```

Poradnik: https://bolekrobot.pl/poradniki/jak-napisac-claude-md-po-polsku

### windows-po-polsku

Zasady pracy po polsku na Windows - nazwy plikow bez polskich znakow, zapis plikow w Unicode, cudzyslowy wokol sciezek ze spacjami, sprawdzenie powloki przed poleceniem. Uzywaj przy kazdym tworzeniu plikow i folderow, zapisie tekstu z polskimi znakami i uruchamianiu polecen w PowerShellu albo w powloce z Gita.

```
claude plugin marketplace add MokebeGluszak/bolekrobot-skills; claude plugin install windows-po-polsku@bolekrobot
```

Poradnik: https://bolekrobot.pl/poradniki/claude-code-po-polsku-na-windows

W samej rozmowie z Claude Code to samo robią polecenia `/plugin marketplace add` i `/plugin install`.

## Skąd to jest

Repo jest generowane automatycznie z treści poradnika https://bolekrobot.pl. Poprawki i pomysły: zgłoszenie w Issues.
