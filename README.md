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

### Badanie sieci

1. W maszynie wirtualnej włącz kolejno programy: terminal (System tools -> LXTerminal), przeglądarkę (Internet -> Firefox) i program Wireshark (Internet -> Wireshark)
2. Na ekranie startowym programu Wireshark wybierz kartę eth0. 
3. W oknie terminala wpisz polecenie `ping -c 4 www.onet.pl` (lub inną stronę).
4. W oknie przeglądarki otwórz stronę `stroustrup.com` (strona twórcy języka C++).
5. Wróć do programu Wireshark i zatrzymaj rejestrację pakietów (czerwony przycisk w lewym górnym rogu).
6. W polu filtra (pasek u góry okna Wireshark z tekstem "Apply a display filter") wpisz:
   * `icmp` aby oberjrzeć działanie polecenia ping
   * `dns` aby obejrzeć rozpoznawanie nazwy przez system DNS
   * `http` aby obejrzeć dane przesyłane przez przeglądarkę 
7. Dla wybranego pakietu protokołu HTTP obejrzyj kolejne warstwy stosu protkołów TCP/IP:
   * fizyczną - część warstwy łącza danych
   * MAC - część warstwy łącza danych
   * IP - sieciową
   * TCP - połączeniową 
   * HTTP - aplikacji
    Zwróć uwagę na adresy w poszczególnych warstwach (SRC i DST)
8. Włącz na nowo rejestrację pakietów przez program Wireshark (nie musisz zapisywać starych danych). Obejrzyj dowolną witrynę WWW i prześledź w Wiresharku przesyłane dane.
