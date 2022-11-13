# 08
1. Vytvořit metodu showVideo (naslouchá na /video/{file}), která bude přehrávat zvolené
video na šabloně video.html (získat z PathVariable). Src bude využívat URL z bodu 2.
2. Vytvořit metodu getVideo (naslouchá na /getvideo/{file}). Funkčně i obsahově shodné
s byterange. Pouze změnit soubor (aby využil správnou cestu = MP4_DIRECTORY a
proměnou z PathVariable)
3. Před metodou gallery vytvořte privátní proměnou MovieLibrary (výchozí hodnota null).
Uvnitř metody pak naplňte (vytvořte nový objekt MovieLibrary) tuto proměnou pouze
tehdy, když je proměnná == null. Metoda gallery předává do šablony tento objekt.
• library = new MovieLibrary(IMAGES_DIRECTORY, MP4_DIRECTORY, SUFFIX, 150);
4. Upravit metodu a šablonu gallery, aby se na stránce zobrazily obrázky videí a po
kliknutí na obrázek dojde k přesměrování na stránku z 1. bodu (včetně názvu, aby se
přehrál správný soubor).
• Pokuste se obrázky s odkazem vložit jako řádky tabulky. (Dodatečně můžete doplnit názvem videa)
• Vytvořit přes foreach v šabloně s využitím objektu movie.
• Adresa videa z objektu: @{'video/'+${movie.getFile_name()}}
• Podobně i obrázek: @{'images/'+${movie.getImage_name()}}
