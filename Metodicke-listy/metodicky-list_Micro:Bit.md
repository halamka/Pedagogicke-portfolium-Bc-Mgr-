## UNIVERZITA PALACKÉHO V OLOMOUCI 

Pedagogická fakulta 

Katedra technické a informační výchovy 

**Josef Halamka** 

**Metodický list** 

##**Programování postřehové hry pro Micro:bit** 


|**Předmět**|Informatika|
|---|---|
|**Ročník**|6. – 9. ročník základní školy|
|**Autor**|Josef Halamka|
|**Téma**|Programování postřehové hry pro Micro:bit|
|**Klíčová slova**|Micro:bit, postřehová hra, programování, skóre,<br>životy, gesto, proměnné|
|**Pomůcky**|Micro:bit, počítače s přístupem k internetu, editor<br>MakeCode, USB kabely|
|**Cíle**|<br>Žák porozumí základnímu principu<br>programování na platformě Micro:bit.<br><br>Žák pochopí funkce pro zpracování gest a<br>tlačítek na Micro:bitu.<br><br>Žák správně používá editor MakeCode nebo<br>Python k vytváření a úpravám kódu.<br><br>Žák vysvětlí logiku hry a naprogramuje základní<br>strukturu postřehové hry.|



### **Struktura a organizace vyučovací jednotky** 

1. **Úvod (15 minut)** 

   - Představení tématu hodiny: tvorba postřehové hry na Micro:bitu. 

   - Diskuze: Co jsou postřehové hry? Jak mohou být programovány? 

   - Vysvětlení základních prvků hry: skóre, životy, náhodné úkoly. 

#### 2. **Teoretická část (20 minut)** 

   - **Základní principy programování hry** : 

      - Vstupy Micro:bitu (gesta, tlačítka). 

      - Proměnné ( _vstup, ukol, skore, zivoty_ ) – jejich použití a aktualizace v průběhu hry. 

      - Podmínky: Jak se rozhoduje, zda byl hráč úspěšný či neúspěšný. 

      - Náhodné generování úkolů. 

      - Zobrazení výsledků (úspěšný pokus, neúspěch, zobrazení skóre). 

   - Promítnutí kódu a vysvětlení jednotlivých částí na příkladu. 

3. **Praktická část (45 minut)** 

   - Žáci samostatně vytvoří postřehovou hru podle základního kódu. 

   - **První úkol** : Programování základní hry. 

      - Žáci nastaví proměnné _skore, zivoty_ , funkci pro náhodný úkol a porovnání, zda hráč úspěšně splnil úkol. 

      - Žáci si vyzkouší hru. 

   - **Druhý úkol (pokročilejší)** : Vylepšení hry – přidání dalších tlačítek a vstupů, úprava rychlosti hry (zkrácení pauzy). 

#### 4. **Závěr a prezentace (10 minut)** 

- Žáci předvedou své hry a diskutují o tom, jaké úpravy a vylepšení přidali. 

- Zhodnocení úspěšnosti každého žáka, poskytnutí zpětné vazby a navrhnutí dalšího rozšíření hry (např. přidání zvukových efektů, počítání času reakce apod.). 

### **Teorie programování postřehové hry na Micro:bitu** 

#### **Micro:bit a jeho vstupy** 

Micro:bit je výuková platforma, která umožňuje snadné programování různých vstupů a výstupů. V této hře využíváme následující vstupy: 

- **Gesta** : Micro:bit dokáže rozpoznat různé pohyby (gesta), jako je náklon vlevo, vpravo, nahoru a dolů. Tato gesta jsou zpracovávána pomocí zabudovaného akcelerometru. 

- **Tlačítka** : Micro:bit má dvě tlačítka (A a B), která mohou být využita jako vstupy pro interakci s hrou. 

V kódu jsou tyto vstupy zpracovávány pomocí funkcí, které reagují na konkrétní události (jako je náklon nebo stisknutí tlačítka). Každé gesto nebo stisknutí tlačítka nastaví hodnotu proměnné _vstup_ , která je následně porovnána s náhodně vygenerovaným úkolem. 

#### **Proměnné** 

Proměnné umožňují uchovávat hodnoty, které se mohou v průběhu programu měnit. V této hře jsou použity následující proměnné: 

- **_vstup_** _:_ Uchovává hodnotu, která odpovídá aktuálnímu gestu nebo stisknutí tlačítka (například 2 pro náklon doprava, 6 pro náklon doleva atd.). 

- **_ukol_** _:_ Uchovává náhodně vygenerovanou hodnotu (úkol), který hráč musí splnit. 

- **_skore_** _:_ Uchovává počet bodů, které hráč získal za správné splnění úkolů. 

- **_zivoty_** _:_ Uchovává počet životů, které hráči zbývají. Pokud počet životů klesne na nulu, hra končí. 

#### **Funkce** 

Funkce jsou bloky kódu, které provádějí určité operace. V tomto programu jsou funkce spojeny s událostmi, což znamená, že se funkce spustí automaticky, když dojde k určitému vstupu (například, když hráč nakloní Micro:bit doprava, zavolá se _funkce_ **_při pohybu je detekován náklon vpravo_** , která nastaví proměnnou _vstup_ na hodnotu 2). Každá funkce má konkrétní úkol. 

- **_při pohybu je logo otočeno dolů, při pohybu je logo otočeno nahoru, při pohybu je detekován náklon vpravo, při pohybu je detekován náklon vlevo_** 

Tyto funkce nastaví hodnotu proměnné _vstup_ podle gesta, které hráč provede. 

#### **Náhodné generování úkolů** 

Micro:bit umožňuje generovat náhodná čísla, což je klíčová součást této hry. V každém kole se vygeneruje náhodné číslo, které odpovídá konkrétnímu gestu nebo tlačítku. Tento úkol se zobrazí hráči pomocí symbolů na displeji (např. šipka, písmeno). 

Tento kód vygeneruje náhodné číslo od 0 do 6 a následně zobrazí šipku, která odpovídá tomuto číslu. 

<figure>
  <img width="418" height="112" alt="Generování náhodného úkolu" src="https://github.com/user-attachments/assets/48b9b467-0cfe-4eb1-b2ca-c0a0cf87d556" />
  <figcaption>Generování náhodného úkolu</figcaption>
</figure>


#### **Podmínky a rozhodování** 

V každém kole hráč provede nějaké gesto nebo stiskne tlačítko. Program pak porovná hodnotu proměnné _vstup_ (která uchovává hráčův vstup) s hodnotou proměnné _ukol_ (náhodný úkol). Pokud jsou hodnoty shodné, hráč získá bod, jinak ztratí život. Toto rozhodování je realizováno pomocí podmínky **_když_** . 

Pokud hráč správně reaguje na zobrazený úkol (např. nakloní Micro:bit správným směrem), jeho skóre se zvýší o 1. Pokud udělá chybu, ztratí život. 



<!-- Start of picture text -->
kdyz ukol ¥ ev vstup ¥ tak<br>zméi skore ¥ o oe<br>ukaZ ikonu 4" ©<br>jinak (S)<br>zméii zivoty ¥ 0 e<br>ukazZ ikonu at oa<br><!-- End of picture text -->

_Podmínka když_ 

#### **Zobrazení výsledků** 

Po každém kole se na displeji Microbitu zobrazí buď ikona **fajfky** (úspěch) nebo **křížku** (chyba). Když hráči dojdou životy, hra končí a na displeji se zobrazí **smutný obličej** a konečné skóre. 



<!-- Start of picture text -->
ukaz ikonu mee)abe ’<br>cekej delay ~ ms<br>prerus<br>zobraz Cislo skore v<br><!-- End of picture text -->

_Zobrazení konečného skóre_ 

#### **Vylepšení hry** 

Pro rozšíření hry mohou studenti přidat další prvky, jako jsou: 

- **Různá gesta a tlačítka** : Můžeme přidat další vstupy pomocí tlačítek A, B a kombinace A+B. 

- **Zvyšování obtížnosti** : S každým kolem můžeme snížit dobu, kterou má hráč na reakci (hodnota proměnné _delay_ ). 

- **Zvuková odezva** : Hráči mohou být odměňováni zvukem za správné reakce. 

### **Základní program** 



<!-- Start of picture text -->
oi starta<br>vai obrazova<br>BE Sip, wo nastay vstup > oa @<br>sara ©<br>iat itom "ee"+<br>®<br>Soo.<br>sina ©<br>kad tho 2 =<br>®<br><!-- End of picture text -->

_Základní program postřehové hry_ 

### **Příklad vylepšeného programu** 

**1. Přidání tlačítek jako další vstupy** 

   - Tlačítko A (vstup = 8) a tlačítko B (vstup = 10) rozšiřují možnosti hry. 

   - Kromě gest (náklonů) nyní hráči musí reagovat i na zobrazení písmen A a B. 

**2. Speciální funkce pro tlačítka A+B** 

   - Hra se spustí až po stisknutí tlačítka A i B zároveň. 

**3. Zrychlení hry** 

   - Snížení času pro reakci (zkrácení pauzy na 500 ms). 

**4. Restart hry** 

- Na konci hry se zobrazí dosažené skóre, poté se hra automaticky resetuje, což umožňuje opakování pokusů bez ručního 



<!-- Start of picture text -->
pei stisknuts taditka AB<br>ae<br>douad (vet * a @® wymat obrazovin<br>oats st<br>wma? obrazovku<br>ka? Sipkay ukot +<br>Fi potybu je detekovin nsielon vpravo = > _<br>PFI polybu je loge atozeno natoru © feke}_ delay ~ )ms<br>Rete<br>ctay~ \as<br>pF potyou<br>Je detekovén ndkion vievo© ®<br>pit stishnuts t1agitka Ay ee an<br>ziti xivotys 0 @®<br>pH stistoutf taaditea B © vat thon =<br>Sinak [o}<br>ak ikonw 32, ><br>eke}<br>cetay~ Je<br>®<br>vane obrazovke<br>worn tot ED<br>zobraz Eislo store +<br>tse) Oo<br>resetuj<br><!-- End of picture text -->

_Vylepšený program postřehové hry_ 

