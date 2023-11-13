# Klasyfikacja-Spaceship-Titanic
# Opis Projektu
Projekt Data Science dotyczący analizy danych "Spaceship Titanic" pochodzących z platformy Kaggle. Głównym celem projektu jest doskonalenie technik data science i analizy danych. 
Projekt składa się z dwóch głównych plików Jupyter Notebook, gdzie każdy z nich obejmuje różne aspekty analizy danych, przygotowania danych i modelowania.

pliki z danymi:

- train.csv - dane osobowe dla około dwóch trzecich (~8700) pasażerów, do wykorzystania jako dane treningowe.
- test.csv - rekordy osobowe dla pozostałej jednej trzeciej (~4300) pasażerów, do wykorzystania jako dane testowe.
- sample_submission.csv - plik zgłoszenia w prawidłowym formacie.

# Plik Analizy Danych:
- Analiza struktury danych, identyfikacja brakujących wartości.
- Wykresy kolumnowe dla danych binarnych i kategorycznych, zarówno ogólnie, jak i z podziałem na zmienną wynikową (Transported).
- Histogramy dla całych danych oraz z podziałem na klasę wynikową.
- Tworzenie nowych kolumn na podstawie istniejących, takich jak "Group", "Number", "CabinDeck", "CabinNum", "CabinSide", "Surname", "Name", "FamilySize", "TravelAlone".
- Uzupełnianie brakujących danych najczęściej występującymi kategoriami i modalnymi wartościami.
- Stworzenie kolumn z wartościami logarytmów dla wybranych kategorii.

# Plik Przygotowanie Danych i Modelowanie:
- Wczytanie danych treningowych i testowych.
- Przygotowanie danych poprzez tworzenie nowych kolumn i uzupełnianie brakujących danych.
- Utworzenie nowych kolumn kategorycznych na podstawie przedziałów wartości w kolumnach Group i CabinNum.
- Wybór kolumn do modelowania: ['PassengerId', 'HomePlanet', 'CryoSleep', 'Destination', 'Age', 'VIP', 'Transported', 'GroupSize', 'CabinDeck', 'CabinSide', 'FamilySize', 'LogRoomService', 'LogFoodCourt', 'LogShoppingMall', 'LogSpa', 'LogVRDeck', 'GroupGroups', 'CabinNumGroups'].
- Rozbicie kolumn kategorycznych na kolumny binarne (dummy variables) i standaryzacja danych.
- Zastosowanie techniki gridsearch w celu znalezienia najlepszych parametrów dla modeli: regresji logistycznej, k-najbliższych sąsiadów (knn), lasu losowego.

Najlepszy modelu: lasu losowego z parametrami: {'criterion': 'entropy', 'max_depth': 20, 'min_samples_leaf': 1, 'min_samples_split': 10, 'n_estimators': 100}. Osiągnął 80% dokładności.
