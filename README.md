# Laboratorium 1

## Cel:

Zapoznanie się z działaniem aplikacji: Git, Vagrant i Virtualbox.

Jeśli w trakcie laboratorium planujesz korzystać ze swojego laptopa, zainstaluj na nim wszystkie aplikacje. Są one dostępne w wersji na systemy: Linux, MacOS i Windows.

## Ćwiczenia:

### Obsługa Gita

1. Otwórz okno konsoli (terminal) i przejdź do folderu w którym będziesz pracował, np. cd labfolders
2. Utwórz repozytorium git: git init myrepo
3. Przejdź do repozytorium: cd myrepo
4. Skonfiguruj swoje dane:
   1. git config user.name "Wojtek"
   2. git config user.email "wojtek@mail.demo"
5. Utwórz nowy plik, np. czytaj.txt
6. Sprawdź stan folderu: git status
7. Dodaj plik do obszaru przechowywania: git add czytaj.txt . Sprawdź jak zmienił się stan folderu.
8. Zapamiętaj przechowane pliki: git commit -m "Pierwszy zapis"
9.  Powtórz kilkakrotnie edycję pliku i zapamiętywanie jej w historii.
10. Obejrzyj historię repozytorum korzystając z różnych widoków:
    - git log
    - git log --oneline
    - git log --graph --oneline

