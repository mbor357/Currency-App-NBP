# Currency-App-NBP
Aplikacja internetowa umożliwiająca pobieranie i wyświetlanie kursów walut z podziałem na lata, kwartały, miesiące i dni. Projekt bazuje na następujących technologiach:

Frontend: Angular
Backend: FastAPI
Baza danych: PostgreSQL
Konteneryzacja: Docker
Źródło danych: NBP API
Testowanie: Pytest

Opis projektu
Aplikacja umożliwia pobieranie kursów walut z Narodowego Banku Polskiego (NBP) i wyświetlanie ich w interaktywnym interfejsie. Aplikacja wyświetla dane w formie tabeli na podstawie wybranego zakresu dat oraz filtruje według : roku, kwartału, miesiąca oraz dnia. Backend zapewnia API, które komunikuje się z bazą danych PostgreSQL, przechowującą dane o kursach. 
Instalacja

Utwórz wirtualne środowisko: python -m venv .venv

Aktywuj środowisko:
Windows: .\.venv\Scripts\activate
Linux/Mac: source .venv/bin/activate
Zainstaluj zależności: pip install -r requirements.txt

Skonfiguruj bazę danych (PostgreSQL): Utwórz bazę danych currency_db w PostgreSQL.
psql -U postgres -c "CREATE DATABASE currency_db;"
Skonfiguruj połączenie w pliku konfiguracyjnym FastAPI.

Uruchom backend: uvicorn main:app --reload
Frontend
Zainstaluj Angular CLI (jeśli nie masz jeszcze zainstalowanego):
npm install -g @angular/cli
Zainstaluj zależności: Przejdź do folderu z frontendem i zainstaluj zależności:
cd C:\Users\Admin\WebstormProjects\currency-app
npm install

Uruchom frontend: ng serve
Aplikacja będzie dostępna pod adresem http://localhost:4200.

Uruchomienie aplikacji
Aby uruchomić całą aplikację (frontend, backend i bazę danych), użyj Dockera.

Uruchom wszystkie usługi w Dockerze:
docker-compose up --build
Aplikacja będzie dostępna pod adresem:

Frontend: http://localhost:4200
Backend API: http://localhost:8000


Testowanie
Testy jednostkowe dotyczące połączenia z bazą danych i sprawdzające endpointy.
Uruchamiamy testy za pomocą komendy: pytest
