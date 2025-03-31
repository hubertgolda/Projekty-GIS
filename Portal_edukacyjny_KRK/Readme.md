# Portal Edukacyjny Kraków
Dostęp: [Portal Edukacyjny](https://experience.arcgis.com/experience/5d2f3cb485064624a8c4629ce2a85d51/)

## Opis
Portal Edukacyjny "Twoja Szkoła" to interaktywna aplikacja stworzona w ArcGIS Experience
Builder. Umożliwia ona wyszukiwanie oraz przeglądanie informacji o szkołach i placówkach
oświatowych, takich jak bursy czy młodzieżowe domy kultury, znajdujących się na terenie miasta
Krakowa. Platforma ma na celu wsparcie rodziców i nastoletnich uczniów w znalezieniu odpowiedniej 
szkoły lub placówki edukacyjnej, która najlepiej odpowiada ich potrzebom i oczekiwaniom.

## Funkcje:
- Interaktywna mapa: Pozwala na szybkie wyszukiwanie placówek oświatowych w oparciu
o lokalizację i typ instytucji.
- Filtry: Umożliwiają wybranie placówki według rodzaju, poziomu edukacji czy
dodatkowych usług (zakwaterowanie w bursie, zajęcia pozalekcyjne w domu kultury).
- Szczegóły placówek: Każda instytucja posiada dedykowaną kartę informacyjną
z podstawowymi danymi.
- Funkcja wyszukiwania: Rodzice i uczniowie mogą łatwo znaleźć interesujące ich
placówki po nazwie, adresie lub typie instytucji.
- Dodatkowe informacje: Platforma zawiera również dane dotyczące komunikacji
miejskiej, które można wykorzystać przy wyborze placówki, biorąc pod uwagę aspekt
transportowy.

Dzięki prostemu w obsłudze interfejsowi oraz nowoczesnej prezentacji danych portal "Twoja
Szkoła" to narzędzie, które czyni proces wyboru szkoły szybkim, wygodnym i przyjaznym dla
użytkownika.

## Źródła danych
- Przystanki tramwajowe:
Mapa K04_KOMUNIKACJA pobrana jako format .pitemx, a następnie otwarta w ArcGIS
Pro. Dla warstw z przystankami autobusowymi i tramwajowymi z tabeli atrybutów zostały
skopiowane dane, a na ich podstawie stworzone zostały pliki .xlsx i warstwy shapefile
(punkty). Ostatnim krokiem było dostosowanie symbolizacji.
[MSIP UM Kraków](https://msip.um.krakow.pl/arcgis/rest/services/Obserwatorium/K04_KOMUNIKACJA/MapServer)
- Sieć tramwajowa: opracowanie własne
- Dane do wektorowej mapy bazowej:
W początkowej fazie pracy nad projektem wykorzystane miały zostać dane ze strony
Bbbike Extract. Jednak ze względu na błędy w geometrii źródło danych zostało zmienione
na prawidłowo działające ze strony Geofabrik Downloads. Wybrany został zbiór
danych w formacie .shp.zip dla województwa małopolskiego. Następnie wyselekcjonowane 
zostały warstwy shapefile z przydatnymi dla projektu danymi (wody, zagospodarowanie 
terenu, budynki oraz drogi). W programie ArcGIS Pro dane zostały przycięte
do granic administracyjnych Krakowa oraz zmieniona została ich symbolizacja.
[Geofabrik.de](https://download.geofabrik.de/europe/poland.html)
- Granice administracyjne z podziałem na dzielnice: [GIS-Support.pl](https://gis-support.pl/baza-wiedzy-2/dane-do-pobrania/granice-administracyjne/)
- Dane o placówkach edukacyjnych:
Wykorzystano gotową warstwę shapefile (punkty) zawierającą informacje o różnych
rodzajach placówek edukacyjnych znajdujących się na terenie miasta Krakowa.
[MSIP UM Kraków](https://msip.um.krakow.pl/arcgis/rest/services/Obserwatorium/EDUKACJA_PLACOWKI/MapServer)
- Dodatkowe dane geograficzne: OpenStreetMap

## Wykorzystane widgety
- Search (wyszukiwarka) – służy do znalezienia potrzebnych danych, np. przystanku po
nazwie bądź numerze linii która go obsługuje, placówek edukacyjnych po nazwie,
numerze lub adresie, a także dzielnic Krakowa po nazwie i numerze. Istnieje możliwość
zaznaczenia, które warstwy mają być brane pod uwagę podczas wyszukiwania. Po
zatwierdzeniu wyszukiwania (kliknięcie na dany wynik) mapa wykonuje zoom w okolice
zaznaczonego obiektu.
- Filter (filtr) – za jego pomocą można wybrać interesujące użytkownika rodzaje placówek
edukacyjnych. Ułatwia to spersonalizowane przeglądanie mapy. Jednocześnie można
zaznaczyć jedną, kilka lub wszystkie warstwy.
- Widget controller (kontroler widgetów) – organizator wielu widgetów w mniejsze pole.
Pozwala na zwiększenie zawartości portalu, jedocześnie zwiększając estetykę. Widgety
w nim zgromadzone otwierają się jako pływające okienka, których rozmiar i położenie
można dostosowywać.
- Near me (w pobliżu) – pozwala na znalezienie danych z wybranego przez użytkownika
obszaru. Miejsce można zaznaczyć za pomocą pinezki (punkt), wielolinii lub kształtu
(poligon). Widget zwróci wyniki znajdujące się w odległości i jednostce zadanej przez
użytkownika w postaci rozwijanej listy, w której znajdują się szczegółowe dane.
- Feature info (informacje o obiekcie) – dodatkowe okno z etykietami, które można
wybierać spośród dostępnych kategorii, bądź po zaznaczeniu konkretnego obiektu.
- Directions (nawigacja) – umożliwia wytyczenie trasy między wybranymi punktami
z uwzględnieniem środka transportu i czasu rozpoczęcia podróży. Wynikiem jego działania
jest wyświetlenie trasy na mapie, lista wskazówek nawigacyjnych oraz czas i odległość
podróży.

## Wykorzystane technologie
- **ArcGIS Pro** – przygotowanie, analiza i wizualizacja danych
- **ArcGIS Online** - przesyłanie i przechowywanie danych
- **ArcGIS Experience Builder** - stworzenie interaktywanego portalu


