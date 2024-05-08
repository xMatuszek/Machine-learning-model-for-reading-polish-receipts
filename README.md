# Model uczenia maszynowego do rozpoznawania paragonów

## 1. Przykładowy cel zastosowania modelu: 
Możliwość zeskanowania paragonu za pomocą smartfonu w celu wyodrębnienia kluczowych informacji jak np. nazwa sklepu, nazwy produktów, suma.

![image](https://github.com/xMatuszek/polish_receipts/assets/45698169/00efab99-73a1-4e88-ba7d-012a63050c0d)

## 2. Nasze podejście: ML + OCR
### 2.1
Wytrenowanie gotowego modelu uczenia maszynowego (YOLO) na własnym zestawie danych do dokładnego lokalizowania, segmentowania i przechwytywania kluczowych obszarów informacyjnych na paragonach.
Użyliśmy programu VoTT do tagowania zdjęć paragonów z podziałem na: `logo` (nazwa sklepu), `top` (część paragonu po nazwie sklepu), `products` (nazwy produktów wraz z ich ilościa i cenami), `bottom` (częśc paragonu po produktach), `total` (suma - łączna cena). 

### 2.2
Wykorzystanie rozwiązania OCR (Azure AI Vision AP) do wyodrębnienia tekstu z odpowiednich obszarów paragonu. 
Obszary paragonu takie jak `top` oraz `bottom` traktujemy jako zbędne. Natomiast obszary takie jak logo, produts oraz total dzielimy na osobne pliki aby następnie przekazać je do OCR w celu wydrębnienia tekstu.

![polish_receipts_process](https://github.com/xMatuszek/polish_receipts/assets/45698169/60a1b1e8-5b8a-4032-89b6-1337e519d8c9)


## 3. Aplikacja desktopowa wykorzystująca model:

https://github.com/pangandalf/receipts-data-extraction-app/

https://github.com/xMatuszek/polish_receipts/assets/45698169/576bb064-b9c9-4e23-87d6-a44eeba52d2a



