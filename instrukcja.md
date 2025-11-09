# Zad_2
Zad_2
# Lekcja 2 – Git – system kontroli wersji
Jest to oprogramowanie służące do śledzenia zmian (głównie w dokumentach tekstowych)
podczas pracy zespołów wieloosobowych dokonujących zmian w różnym czasie i
miejscach przebywania.
## Git - podstawowe cechy  
* efektywna praca z dużymi projektami - jest jednym z najszybszych systemów
kontroli wersji
* wsparcie dla protokołów sieciowych - dane można wymieniać przez HTTP(S), FTP,
rsync, SSH, e-mail
* każda kopia repozytorium to obraz całego projektu - Git nie zapamiętuje zmian
między kolejnymi rewizjami lecz kompletne obrazy (snapshots)
* możliwość tworzenia oprogramowania z rozgałęzieniami
* tryb pracy off-line - każdy pracuje na własnej kopii repozytorium, a następnie
zmiany mogą być wymieniane między lokalnymi repozytoriami jak również
serwerem.
## Idea pracy:
Na powyższym rysunku symbolicznie przedstawiono zasadę pracy z gitem. Większy okrąg
symbolizuje repozytorium lokalne (po lewej) w którym pracuje użytkownik. Mniejszy okrąg (po
prawej) to kopia repozytorium na wybranym serwerze (np. github.com lub gitlab.com). Czerwone
strzałki to komendy git’a, które powodują przenoszenie plików i/lub katalogów pomiędzy
poszczególnymi elementami repozytorium lub pomiędzy maszyną lokalną a serwerem.  

Git rozróżnia trzy typy plików w repozytorium lokalnym: nadzorowane, pomijane i
nienadzorowane. Z punku widzenia systemu plików repozytorium to zwykły katalog w którym
zaicjalizowany został specjalny podkatalog o nazwie .git, w którym przetrzymywane są wszystkie
informacje o repozytorium.  

Użytkownik pracuje w katalogu roboczym, gdzie modyfikuje swoje pliki. Gdy uzna, że postęp prac
wymaga zapisania zmian przenosi je do staging area (komenda add). Gdy suma zmian stanowi
jakąś spójną całość (np. dodanie nowego rozdziału pracy, dodanie nowej funkcjonalności itd.)
tworzy się nową „migawkę” zapisywaną w lokalnym repozytorium (komenda commit). Co jakiś
czas można przenieść lokalne zmiany w repozytorium na serwer (komenda push).  

Uwaga: Do pracy z systemem git należy zainstalować oprogramowanie ze strony:  

[https://git-scm.com/downloads](https://git-scm.com/downloads)  

Po zainstalowaniu będzie dostępna powłoka z wyglądu podobna do tej z poniższego rysunku  

Jest to aplikacja **Git Bash** w której wydajemy polecenia z linii komend.

![ps1](https://github.com/user-attachments/assets/0ad0ea1e-d724-4adf-aa5a-7c71bdbd1367)  

Pierwszym krokiem po instalacji git’a i uruchomieniu aplikacji Git Bash jest wydanie dwóch
poleceń:  

**$git config --global user.name "Student Wspaniały"**  

**$git config --global user.email "wspanialy@pw.edu.pl"** 

W ten sposób informujemy system git kto będzie autorem zmian wprowadzanych do repozytorium
Uwaga: należy wprowadzić własne dane osobowe i własny adres e-mail  
W przypadku piszącego tą instrukcję wynik wprowadzonych komend ma postać:  
![ps2](https://github.com/user-attachments/assets/9188f49e-1f4c-4f73-9576-788d8bbbaae6)



