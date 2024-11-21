# Szablon dyplomu PWr zgodny z Overleaf

[For english readme click
here](https://github.com/rkubosz/dyplompwr/blob/master/doc/manual.pdf)

Ten projekt dostarcza nieoficjalny szablon pracy dyplomowej dla studentów
Politechniki Wrocławskiej. Ten szablon jest przeznaczony do zastosowania z
systemem składu tekstu [**LaTeX**](https://pl.wikipedia.org/wiki/LaTeX).
Jest także zgodny z Overleaf, przy użyciu kompilatora LuaLaTeX/XeLaTeX.

Szablon jest kompatybilny z [wymaganiami Wydziału
Chemicznego](http://wch.pwr.edu.pl/fcp/6GBUKOQtTKlQhbx08SlkTUAJQX2o8DAoHNiwFE1xVSXtVFVZpCFghUHcKVigEQUw/36/public/druki/duplomanci/ii_stopnia/21.doc) odnośnie
formatowania i strony tytułowej.

Szablon tworzy stronę tytułową pracy magisterskiej lub inżynierskiej w wersji
polskiej lub angielskiej w formatowaniu wymaganym przez dziekanat lub w wersji
dla promotora.

## Cechy pakietu

__Dyplompwr__ zapewnia:
* tworzenie strony tytułowej;
* dopasowuje stronę tytułową do typu pracy: `master` dla pracy magisterskiej  i
  `engineer` dla pracy inżynierskiej;
* zmienia odpowiednio logo PWr i typ pracy do wybranego języka: `pl` dla języka
  polskiego i `en` dla angielskiego;
* z pomocą opcji `archive` i `oneside` dobiera odpowiednie marginesy, interlinię
  i skład dokumentu dla dziekanatu i promotora odpowiednio.


## Przykład użycia

Szablon należy załadować w pierwszej linijce pliku `.tex`:
```latex
\documentclass[master,archive,pl]{dyplompwr}
```
Użyte powyżej parametry spowodują utworzenie strony tytułowej po polsku dla
pracy magisterskiej oraz złożenie dokumentu przeznaczonego do druku
dwustronnego z interlinią i marginesami dla dziekanatu.

Strona tytułowa wymaga podania takich metadanych, jak nazwisko autora, tytuł
pracy, tytuł i nazwisko promotora etc. W tym celu należy je podać w dalszych
liniach pliku:
```latex
\documentclass[master,oneside,pl]{dyplompwr}
\author{imię i nazwisko autora pracy}
\title{tytuł polski}
\titlen{tytuł angielski}
\supervisor{tytuł, imię i nazwisko promotora}
\faculty{nazwa wydziału}
\city{Wrocław lub inna miejscowość}
\keywords{słowa kluczowe}
\abstract{Tutaj możesz napisać swoje krótkie streszczenie
pracy dyplomowej.}
```

Proste przykłady użycia klasy dyplompwr [jest zaprezentowany w tym
folderze.](https://github.com/alkus88/dyplompwr/tree/master/examples)

## Instalacja

[**Dyplompwr zgodny z Overleaf** można pobrać bezpośrednio
tutaj.](https://github.com/alkus88/dyplompwr/releases/latest)

Pobrane archiwum zip należy rozpakować i zawartość otrzymanego katalogu `dyplompwr` zainstalować
w sposób wybrany z poniższej listy:
* umieszczenie w katalogu zawierajacym główny plik `*.tex` pracy dyplomowej - dedykowane dla Overleaf
* umieszczenie w katalogu:
    * Windows 7 i wyżej:  `C:\Users\twoja nazwa użytkownika\texmf\tex\latex\local\`
    * Linux:    `~/texmf/tex/latex/local/`
    * OSX:      `/Users/twoja nazwa użytkownika/Library/texmf/tex/latex/local/`
      

Użytkownicy Arch Linux mogą zaintalować pakiet `dyplompwr` z repozytorium
[AUR](https://aur.archlinux.org/packages/dyplompwr/).

## Wymagania

Pakiet `dyplompwr` potrzebuje do poprawnego działania klasy `mwrep`, którą można
zainstalować wraz z pakietem [`mwcls`](https://www.ctan.org/tex-archive/macros/latex/contrib/mwcls).

W celu stworzenia ładnej i zgodnej z zaleceniami strony tytułowej należy
zainstalować dodatkowe fonty (URW Garamond i URW Classico), które domyślnie nie
są dostępne w dystrybucjach LaTeXa.

Fonty znajdują się w katalogu fonts. Instaluje się je umieszczając następujący kod w preambule:
% URW Garamond
\setmainfont{GaramondNo8-Reg}[
    Path=fonts/, % Ścieżka do plików
    Extension=.ttf, % Rozszerzenie pliku
    BoldFont=GaramondNo8-Med.ttf, % Font pogrubiony
    ItalicFont=GaramondNo8-Ita.ttf, % Font kursywa
    BoldItalicFont=GaramondNo8-MedIta.ttf % Font pogrubiona kursywa
]

% URW Classico
\setsansfont{URWClassico-Regular}[
    Path=fonts/, % Ścieżka do katalogu z fontami
    Extension=.ttf, % Rozszerzenie pliku
    BoldFont=URWClassico-Bold.ttf, % Font pogrubiony
    ItalicFont=URWClassico-Italic.ttf, % Font kursywa
]
\usepackage{polyglossia}
\setdefaultlanguage{polish}

## Autorzy

Pakiet stworzyłem na podstawie wcześniej stworzonych pakietów autorstwa [rkubosz](https://github.com/rkubosz), a on z kolei [dra
Andrzeja Giniewicza](https://github.com/aginiewicz/pwrmgr) oraz [dra Wojciecha
Myszki](https://kmim.wm.pwr.edu.pl/myszka/projekty/klasa-do-skladu-pracy-dyplomowej-magisterskiej-i-inzynierskiej-na-wydziale-mechanicznym-politechniki-wroclawskiej/).

## Licencja

Pakiet jest na licencji MIT.

