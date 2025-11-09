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
