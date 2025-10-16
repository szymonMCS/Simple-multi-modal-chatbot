# 🤖 Multi-modalny Chatbot AI Tutor

Prosty, ale potężny chatbot zbudowany w Pythonie, który pełni rolę tutora technicznego. Wykorzystuje najnowsze modele OpenAI do interakcji tekstowej, głosowej oraz do generowania obrazów. Interfejs został stworzony przy użyciu biblioteki Gradio.


## ✨ Główne Funkcje

* **Interfejs Tekstowy i Głosowy**: Możesz pisać lub mówić do chatbota.
* **Odpowiedzi Głosowe**: Asystent odpowiada na Twoje pytania głosem (Text-to-Speech).
* **Generowanie Obrazów**: Po zapytaniu o cenę subskrypcji AI (np. "ile kosztuje gemini?"), chatbot generuje unikalny obraz w stylu pop-art za pomocą DALL-E 3.
* **Tool Calling (Wywoływanie Narzędzi)**: Chatbot potrafi korzystać z zewnętrznych funkcji (w tym przypadku do sprawdzania cen), aby udzielać precyzyjnych odpowiedzi.
* **Streaming Odpowiedzi**: Odpowiedzi tekstowe pojawiają się słowo po słowie, co poprawia wrażenia z użytkowania.
* **Wybór Modelu**: Możliwość przełączania się między `gpt-4o-mini` a `gpt-3.5-turbo`.

## 🛠️ Użyte Technologie

* **Backend**: Python
* **API**: OpenAI (GPT-4o-mini, DALL-E 3, TTS-1, Whisper-1)
* **Interfejs Użytkownika**: Gradio
* **Obsługa Audio**: Pydub

## 🚀 Instalacja i Uruchomienie

Aby uruchomić projekt lokalnie, postępuj zgodnie z poniższymi krokami.

### 1. Sklonuj Repozytorium

```bash
git clone [https://github.com/TWOJA_NAZWA_UŻYTKOWNIKA/NAZWA_REPOZYTORIUM.git](https://github.com/TWOJA_NAZWA_UŻYTKOWNIKA/NAZWA_REPOZYTORIUM.git)
cd NAZWA_REPOZYTORIUM
```

### 2. Zainstaluj Zależności

Zalecane jest utworzenie wirtualnego środowiska.

```bash
python -m venv venv
source venv/bin/activate  # Na Windows: venv\Scripts\activate
```

Następnie zainstaluj wymagane pakiety. Możesz utworzyć plik `requirements.txt` o poniższej zawartości:

**requirements.txt:**
```
openai
gradio
python-dotenv
pydub
pillow
```

I zainstalować go komendą:
```bash
pip install -r requirements.txt
```

### 3. Skonfiguruj Klucz API

Projekt wymaga klucza API od OpenAI.

1.  Utwórz plik o nazwie `.env` w głównym folderze projektu.
2.  Wklej do niego swój klucz API w następującym formacie:

```
OPENAI_API_KEY="sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

### 4. Uruchom Aplikację

Twój kod jest w formacie notatnika Jupyter. Możesz go uruchomić bezpośrednio lub przekonwertować na skrypt `.py`.

**Opcja A: Uruchomienie jako notatnik**
```bash
jupyter notebook simple_chatbot.ipynb
```

**Opcja B: Uruchomienie jako skrypt Python**

Przekonwertuj notatnik na skrypt (`.py`) i uruchom go:
```bash
jupyter nbconvert --to script simple_chatbot.ipynb
python simple_chatbot.py
```

Po uruchomieniu aplikacja będzie dostępna w przeglądarce pod adresem lokalnym (np. `http://127.0.0.1:7860`).

## 💡 Jak Używać?

* Wpisz swoje pytanie w pole tekstowe i naciśnij Enter.
* Kliknij ikonę mikrofonu, aby zadać pytanie głosowo.
* **Aby zobaczyć generowanie obrazu**, zadaj pytanie o cenę jednego z modeli: `gemini`, `openai` lub `claude`. Na przykład:
    * `"How much is for gemini?"`
    * `"Jaka jest cena claude?"`
* Użyj przycisku "Clear", aby wyczyścić historię rozmowy.