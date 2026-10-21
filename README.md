# Procedura WebGazer — prototyp

Statyczna, lokalna wersja testowa procedury badawczej. Nie ma backendu, `localStorage`, ciasteczek ani eksportu danych. Odpowiedzi i próbki spojrzenia istnieją tylko w pamięci bieżącej karty.

## Uruchomienie

Kamera działa na `localhost` lub przez HTTPS. W tym katalogu uruchom:

```powershell
python -m http.server 4173 --bind 127.0.0.1
```

Następnie otwórz `http://localhost:4173/` w aktualnej wersji Chrome lub Edge. WebGazer może odrzucić równoważny adres `127.0.0.1`, ponieważ rozpoznaje dosłownie nazwę `localhost`.

WebGazer.js jest pobierany z oficjalnego hosta projektu, dlatego pierwsze uruchomienie wymaga połączenia z internetem.

## Zakres prototypu

- ankieta demograficzna;
- dwie próby kalibracji, próg 80%;
- losowa kolejność siedmiu postów;
- jednakowa wysokość obszaru tekstowego i jednakowa wysokość obszaru ilustracji;
- sześciocyfrowe zadanie pamięciowe;
- ekspozycja posta przez 10 sekund;
- ocena prawdziwości na skali 0–100%;
- wybór liczby spośród pięciu wariantów;
- ostrzeżenie po trzech sekundach bez spojrzenia na ekran;
- debriefing i usunięcie danych po odświeżeniu/zamknięciu karty.

## Ważna uwaga metodologiczna

Aktualna wersja implementuje wyłącznie warunek obciążenia poznawczego zgodnie z opisem (sześć cyfr przed każdą ekspozycją). Do testu przyczynowego wpływu obciążenia potrzebny jest także warunek kontrolny lub warunek o niższym obciążeniu oraz losowy przydział uczestników albo prób.
