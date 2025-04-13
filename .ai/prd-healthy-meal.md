# Dokument wymagań produktu (PRD) - HealthyMeal

## 1. Przegląd produktu
HealthyMeal to aplikacja, która umożliwia dostosowanie przepisów kulinarnych do indywidualnych potrzeb żywieniowych użytkownika. Aplikacja pozwala na wklejanie surowego tekstu przepisu, walidację jego minimalnej długości (1000 znaków), automatyczną modyfikację przez API AI zgodnie z predefiniowanymi preferencjami żywieniowymi oraz prezentację porównawczą oryginalnego przepisu i zmodyfikowanej wersji. System logowania opiera się na e-mailu i haśle, co gwarantuje bezpieczeństwo danych.

## 2. Problem użytkownika
Użytkownicy mają trudności z adaptacją dostępnych w sieci przepisów do własnych potrzeb dietetycznych. Ręczne dzielenie przepisu na składniki i instrukcje jest czasochłonne, a brak personalizacji prowadzi do nieoptymalnych rozwiązań żywieniowych.

## 3. Wymagania funkcjonalne
- Umożliwienie wklejania surowego tekstu przepisu bez konieczności ręcznego dzielenia na składniki i instrukcje.
- Walidacja przepisu, gdzie tekst musi mieć minimum 1000 znaków.
- Integracja z API AI, które automatycznie modyfikuje przepis na podstawie predefiniowanej listy preferencji żywieniowych. Lista ta obejmuje m.in.:
  - dieta bezglutenowa
  - dieta bezlaktozowa
  - dieta niskowęglowodanowa
  - dieta niskotłuszczowa
  - dieta wysokobiałkowa
  - dieta niskobiałkowa
  - preferencje łatwostrawne
  - alergie i nietolerancje
  - weganizm i wegetarianizm
  - unikanie produktów wysoko przetworzonych
  - unikanie oleju palmowego
  - sezonowość
  - unikanie wołowiny i wieprzowiny
- Prezentacja oryginalnego przepisu obok zmodyfikowanej wersji, umożliwiająca użytkownikowi ocenę porównawczą.
- System logowania oparty na e-mailu i haśle zapewniający dostęp do aplikacji.
- Po zatwierdzeniu przepisu dalsza modyfikacja nie jest możliwa.

## 4. Granice produktu
- Brak importu przepisów z adresu URL.
- Nieobsługiwanie multimediów, takich jak zdjęcia przepisów.
- Brak funkcji społecznościowych, takich jak udostępnianie przepisów.
- Weryfikacja przepisu ograniczona jest do sprawdzenia minimalnej długości; nie ma szczegółowej walidacji składników i instrukcji.
- Po zatwierdzeniu przepisu, dalsza edycja jest wyłączona.

## 5. Historyjki użytkowników
- US-001
  - Tytuł: Rejestracja i logowanie do systemu
  - Opis: Użytkownik rejestruje się oraz loguje do systemu używając e-maila i hasła, aby uzyskać dostęp do funkcji aplikacji.
  - Kryteria akceptacji: Użytkownik może utworzyć konto i zalogować się, otrzymując komunikat potwierdzający sukces lub informujący o błędzie przy niepoprawnych danych.

- US-002
  - Tytuł: Wklejanie przepisu
  - Opis: Użytkownik wkleja surowy tekst przepisu w dedykowanym formularzu.
  - Kryteria akceptacji: System wyświetla wklejony tekst oraz potwierdza, że tekst spełnia wymóg minimalnej długości (1000 znaków).

- US-003
  - Tytuł: Modyfikacja przepisu przez AI
  - Opis: Po wklejeniu przepisu, system wysyła jego treść do API AI, które automatycznie identyfikuje składniki i instrukcje oraz modyfikuje przepis zgodnie z predefiniowanymi preferencjami.
  - Kryteria akceptacji: Zmodyfikowany przepis jest wyświetlany obok oryginału, a różnice między wersjami są widoczne i zgodne z oczekiwaniami użytkownika.

- US-004
  - Tytuł: Zatwierdzenie przepisu
  - Opis: Użytkownik porównuje oryginalny przepis z jego zmodyfikowaną wersją i zatwierdza jedną z nich do zapisania.
  - Kryteria akceptacji: Po zatwierdzeniu, wybrana wersja przepisu zostaje zapisana, a możliwość dalszej edycji przepisu zostaje wyłączona.

- US-005
  - Tytuł: Bezpieczny dostęp do danych
  - Opis: Użytkownik loguje się do systemu, gdzie dane są chronione, a dostęp do funkcji aplikacji jest ograniczony tylko do uwierzytelnionych użytkowników.
  - Kryteria akceptacji: System poprawnie uwierzytelnia użytkownika, a dane są dostępne jedynie po pozytywnym zalogowaniu.

## 6. Metryki sukcesu
- 90% użytkowników posiada wypełnioną sekcję preferencji żywieniowych w swoim profilu.
- 75% użytkowników generuje co najmniej jeden przepis tygodniowo.
- Czas modyfikacji przepisu przez API AI nie przekracza 5 sekund. 