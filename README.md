# Laboratorium 1

## Cel:

Zapoznanie się z działaniem aplikacji: Git, Vagrant i Virtualbox.

Jeśli w trakcie laboratorium planujesz korzystać ze swojego laptopa, zainstaluj na nim wszystkie aplikacje. Są one dostępne w wersji na systemy: Linux, MacOS i Windows.

## Ćwiczenia:

### Obsługa Gita

1. Otwórz okno konsoli (terminal) i przejdź do folderu w którym będziesz pracował, np. `cd labfolders`
2. Utwórz repozytorium git: `git init myrepo`
3. Przejdź do repozytorium: cd myrepo
4. Skonfiguruj swoje dane:
   ```
   git config user.name "Wojtek"
   git config user.email "wojtek@mail.demo"
   ```
5. Utwórz nowy plik, np. czytaj.txt
6. Sprawdź stan folderu: `git status`
7. Dodaj plik do obszaru przechowywania: `git add czytaj.txt` . Sprawdź jak zmienił się stan folderu.
8. Zapamiętaj przechowane pliki: `git commit -m "Pierwszy zapis"`
9.  Powtórz kilkakrotnie edycję pliku i zapamiętywanie jej w historii.
10. Obejrzyj historię repozytorum korzystając z różnych widoków:
    ```
    git log
    git log --oneline
    Git log --graph --oneline
    ```

### Obsługa Vagranta

1. Pobierz repozytorium laboraryjne na swój komputer: `git clone https://github.com/pwr-sisi/lab1.git`
2. Wejdź do projektu `cd lab1.git`
3. Uruchom maszynę przy pomocy Vagranta: `vagrant up` . Jeśli wykonujesz operację po raz pierwszy, system musi pobrać obraz maszyny z Internetu co może trochę potrwać.
4. Maszyna powinna się uruchomić. Zaloguj się do maszyny korzystając z konta vagrant z takim samym hasłem.
5. Dodatkowe operacje (w razie potrzeby):
   * Aby zatrzymać maszynę: `vagrant halt`
   * Aby skasować maszynę: `vagrant destroy`

