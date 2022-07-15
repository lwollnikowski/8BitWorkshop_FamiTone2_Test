8BitWorkshop_FamiTone2_Test
=====

[Open this project in 8bitworkshop](http://8bitworkshop.com/redir.html?platform=nes&githubURL=https%3A%2F%2Fgithub.com%2Fverteks16%2F8BitWorkshop_FamiTone2_Test&file=fami.c).

 Co takiego zrobiłem żeby działało, na bazie przykładu "Famitone Demo" z przykładowych projektów z 8BitWorkshop:
- Famitracker 0.4.6 -> File -> Export Text.
- Pobrałem text2data.exe z tego repo: https://github.com/nesdoug/famitone2d
- Wyeksportowany plik oraz text2data.exe wrzuciłem do jednego katalogu.
- Otworzyłem CMD / terminal, wpisałem: `text2data.exe <nazwa_pliku.txt> -ca65`.
- Dostałem errorem że instrument zero nie ma obwiedni głośności, to na szybko ją ustawiłem w Famitrackerze; powtarzać konwersję aż skończą się błędy i narzędzie wypluje plik *.s.
- Skopiowałem zawartośc pliku *.s do pliku w 8BitWorkshop, dodałem export labelki, dodałem deklarację tablicy typu char w pliku fami.c, podobnie jak to jest dla przykładowego utworu "Danger Streets".
- Działa, muzyka się odtwarza w IDE.

FamiTone2 ma tam jakieś ograniczenia na efektach, także trzeba się nauczyć co przepada w trakcie konwersji. Na pewno jest jakiś problem z prędkością odtwarzania (efekt Fxx), bo muzyka odtwarza się inaczej w 8BitWorkshop i inaczej w Famitrackerze.

Plik ftm_test.zip zawiera użyty w przykładzie plik FTM oraz wszystkie kroki pośrednie stworzone w trakcie procesu dodawania swoich utworów do projektów w 8BitWorkshop.
