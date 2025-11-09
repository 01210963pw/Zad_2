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

##Git – tworzenie pustego archiwum lokalnego.  

Należy w konsoli wywołać następującą sekwencję komend (zakładając, że repozytorium będzie
nosiło nazwę repo1):  

1. $mkdir repo1
2. $cd repo1
3. $git init
4. $git status

Pierwsza komenda tworzy katalog o zadanej nazwie.  

Druga komenda powoduje, że przechodzimy do właśnie stworzonego katalogu  

Trzecia komenda inicjuje puste repozytorium  

Czwarta komenda wyświetla informacje o stanie repozytorium  


![ps3](https://github.com/user-attachments/assets/86d657f4-2ecb-4e1e-8205-150cca0a396c)  

Jak widać na powyższym rysunku po stworzeniu pustego repozytorium pracujemy w głównej gałęzi
**master** i brak jest zarejestrowanych jakichkolwiek „migawek” (commits)  

Dodawanie pliku/ów do indeksu:  

* $git add file - dodanie pliku do indeksu
* $git rm - -cached file - usunięcie pliku z indeksu

![ps4](https://github.com/user-attachments/assets/eeb22f8b-7c63-496e-bba0-48d606d269dc)  
Powyższy rysunek prezentuje sekwencję komend:  
1. $touch.exe nowy.md – utworzenie pustego pliku tekstowego
2. $git add nowy.md – dodanie nowo stworzonego pliku do indeksu
3. $git status – wyświetlenie statu lokalnego repozytorium

Widać (zielony kolor), że git śledzi wprowadzone zmiany



Git - zapis pliku do repozytorium lokalnego:

* $git commit -m "komunikat" – w komunikacie podaje się krotki opis zmian wprowadzonych
do repozytorium

![ps5](https://github.com/user-attachments/assets/05642d3d-0fd9-4368-881b-2528701c6ec2)  
Polecenie $git log wyświetla listę zapisanych „migawek”. Każda migawka identyfikowana jest
sekwencją liczb szesnastkowych (żółte cyfry) – komentarzem jaki podajemy podczas wywoływania
polecenia $git commit.  

**Git – dodanie kolejnych plików, modyfikacja i stworzenie kolejnych „migawek”**  

Używając tekstowego edytora nano (można użyć własnego ulubionego edytora) – zmodyfikowano
zawartość pliku nowy.md – co natychmiast zauważył system kontroli wersji (modified nowy.md).
Następnie stworzono kolejny pusty plik (następny.md) co również system zasygnalizował jako:
(Untracked files – następny.md). Teraz zostaną wykonane dwa niezależne commity i zostanie
wyświetlony kolejny log stanu repozytorium.  

Jak widać na kolejnym rysunku w repozytorium zostały umieszczone trzy „migawki” stanu
repozytorium wszystkie umieszczone w gałęzi głównej „master”.  

![ps6](https://github.com/user-attachments/assets/798d0386-172d-42d5-bc44-7d577d40c449)

![ps7](https://github.com/user-attachments/assets/7c54b4d8-c273-4bf2-af99-4a13df45bbb0)


**Git – praca z rozgałęzieniami**  


Bardzo często zachodzi taka sytuacja, że nie chcemy wprowadzać zmian w głównej gałęzi a tylko
wykonać jakieś prace testowe i później zdecydować czy dołączyć je do głównej gałęzi lub nie. Do
tego służą rozgałęzienia, i operacja ich łączenia.  

* $git branch name – tworzenie nowego rozgałęzienia
* $git checkout name - przełączenie się do innej gałęzi
* $git branch -D name - usunięcie rozgałęzienia (trzeba być od niego odłączonym)
* $ git merge nazwa_gałęzi – złączenie gałęzi „nazwa_gałęzi” z gałęzią do której jesteśmy
podłączeni

![ps8](https://github.com/user-attachments/assets/d0c6b6cb-b895-45e0-b465-d66d5c0958d5)

Każde lokalne repozytorium możemy umieścić na dedykowanym serwerze protokołu git (możemy
także spakować katalog z repozytorium i taką kopię przesłać zainteresowanemu np. E-mailem).
Jeżeli chcemy realizować wspólne projekty - nad którymi pracuje wiele osób - to niezbędnym jest
wykorzystanie serwera.  

Mamy do dyspozycji np.  




