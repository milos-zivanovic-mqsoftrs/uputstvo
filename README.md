 ### _**Kako se prijaviti za rad u PAPA aplikaciji?**_
- na ruti za prijavu na PAPA aplikaciju (slika 1.0) (```/login```), unesite Ime korisnika i Lozinku

slika 1.0

![alt text](https://raw.githubusercontent.com/milos-zivanovic-mqsoftrs/uputstvo/images/PAPA.png)
![papa](https://user-images.githubusercontent.com/42855729/51324423-f9202600-1a6a-11e9-9307-7f3ad9faa3b3.png)

- kliknite na ```Uloguj se```
- nakon uspesne prijave, sistem vas redirektuje na rutu ```/pregled```

slika 1.1

![alt text](https://raw.githubusercontent.com/milos-zivanovic-mqsoftrs/uputstvo/images/master/pregled.png)

![Optional Text](../master/uputstvo/pregled.png)

ruta ```/pregled``` sadrzi graficki prikaz: 
- dnevnog pregleda naloga 
- mesecnog pregleda naloga
- dnevnog pregleda podataka

---
---
  
### _**Kako dodati novog Isplatioca?**_
- nakon uspesnog prijavljivanja i prelaska na rutu ```/pregled```, u korisnickom interfejsu sa leve strane kliknuti na opciju ```Isplatioci``` cijim odabirom nas sistem redirektuje na rutu ```/isplatioci``` (slika 1.2)


slika 1.2
![image](images\isplatioci.png)
![Alt text](relative/milos-zivanovic-mqsoftrs/uputstvo/images/master/isplatioci.png?raw=true "Title")

-  kliknuti na dugme ```Dodaj```
- sistem ce vas redirektovati na rutu za dodavanje novog isplatioca, rutu ```/isplatioci/editor``` (slika 1.3)

slika 1.3
![image](images\isplatioci-editor.png)

ekran za unos novog isplatioca se sastoji od: 
- sekcije za unos _**Osnovnih podataka o isplatiocu**_: da li je isplatioc klijent UCB ili ne, polja za unos imena isplatioca, broja zaposlenih, maticnog broja isplatioca, PIB-a isplatioca koja predstavljaju obavezna polja kao i neobavezna polja grad i ulica isplatioca
Ukoliko je u polju ```*Klijent UCB``` selektovano ```DA```, sa desne strane se otvaraju jos 2 polja, ```*Klijentski broj``` i ```*OPU```. U tom slucaju je potrebno uneti jedino klijentski broj isplatioca koji je klijent banke i kliknuti na ```Potvrdi```. Posle odredjenog vremena, sva polja osim ```*Broj zaposlenih``` ce se automatski popuniti podacima iz baze. Polje ```*Broj zaposlenih``` popuniti naknadno 
- sekcije za unos _**Vrste podataka**_: vrste podataka mogu biti Spisak, Fajl i Payroll. U slucaju kada je selektovan Fajl kao vrsta podataka, potrebno je u polju ```*Parametrizacija``` koje se pojavljuje sa desne strane zadati prethodno sacuvanu matricu parametrizacije koja ce se koristiti za parsiranje dostavljenog dokumenta od strane Isplatioca. Ukoliko je selektovan Payroll kao vrsta podataka, pored polja ```*Parametrizacija``` pojavljuju se i obavezna polja ```*Payroll racun``` (u koji treba uneti jedinstveni payroll racun), ```Kontrola na nivou racuna``` (DA ili NE), ```Racun provizije```, kao i neobavezna polja ```Model provizije``` (Fiksna RSD, Fiksna EUR...) i ```Iznos provizije```.
- sekcije _**Kontakti**_: u ovoj sekciji nalaze se neobavezna polja za ```E-mail ovlascenog lica``` (moguc je unos do 5 mailova ovlascenog lica), ```E-mail```(maksimalan unos- 5), ```Telefon```(maksimalan unos- 4), ```Kontakt osoba```(maksimaln unos- 2)
 
 Nakon popunjavanja odgovarajucih polja kliknuti na dugne ```Sacuvaj```, a nakon pojave prozorcica sa porukom upozorenja (Da li ste sigurni da zelite da sacuvate promene?) kliknite na ```Potvrdi```. U slucaju da ne zelite da sacuvate promene, klikom na ```Otkazi``` se vracate na rutu /isplatioci/editor

 Posle poruke o uspesnom dodavanju novog isplatioca, sistem vas redirektuje na rutu ```/isplatioci```(slika 1.2)

 Ruta ```/isplatioci``` (slika 1.2) sadrzi pregled svih prethodno unetih Isplatioca, kao i formu za detaljnu pretragu isplatioca po sledecim parametrima:
 
 - Naziv isplatioca
 - Broj klijenta
 - Maticni broj(MB)
 - Poreski broj(PIB)
 - Tip podataka
  
Unos zeljenih podataka u polja ovih parametara i klikom na dugme ```Pretrazi```, vrsi se detaljna pretraga po zadatim parametrima. Ponistavanje rezultata pretrage i vracanje na pregled svih prethodno unetih isplatilaca vrsi se klikom na dugme ```Reset```

Tabelarni pregled isplatilaca sa manje detalja, sadrzi sledece kolone:
- ```Isplatilac``` - ime unetog Isplatioca
- ```Klijent UCB``` - da li je klijent UCB ili ne
- ```Broj klijenta``` - jedinstveni broj klijenta u registru banke
- ```MB``` - maticni broj isplatioca
- ```PIB``` - poreski broj isplatioca
- ```Tip podataka``` - da li je u pitanju Spisak Fajl ili Payroll

Klikom na ```Vise detalja``` u desnom uglu stranice, pored prethodno opisanih polja prikazuju se i:
- ```Vreme unosa```
- ```Vreme izmene```
- ```Email ovlascenog lica```
- ```Kontakt osobe```
- ```Kontakt telefoni```
- ```Elektronska posta```

Podatke sa tabelarnog pregleda isplatilaca moguce je preuzeti kao trenutnu stranu klikom na dugme ```Preuzmi stranu```. Podaci se preuzimaju u formatu ```isplatioci_{datum preuzimanja}.xlsx```. Moguce je i preuzimanje svih isplatilaca klikom na dugme ```Preuzmi sve```. Podaci se takodje preuzimaju u formatu ```isplatioci_{datum preuzimanja}.xlsx```

### _**Kako izmeniti unetog Isplatioca?**_

Izmena unetog isplatioca vrsi se dvoklikom na isplatioca u tabeli na ruti ```/isplatioci```, ili klikom na ikonicu ```Izmeni``` u koloni ```Akcija```, posle cega nas sistem redirektuje na rutu ```/isplatioci/editor``` za izmenu podataka

slika 1.4
![image](images\izmena.png)

U svakom momentu mozemo izaci iz izmene isplatioca klikom na dugme ```Nazad``` uz propratnu poruku u prozorcicu da promene nece biti sacuvane

Nakon zeljenih izmena u sekcijama ```Osnovni podaci o isplatiocu```, ```Vrsta podataka``` i ```Kontakti```, iste potvrdjujemo klikom na dugme ```Sacuvaj```. U prozorcicu sa upozorenjem (Da li ste sigurni da zelite da sacuvate promene?) kliknite na ```Potvrdi```. Klikom na ```Otkazi``` vracamo se u editor za izmenu podataka o Isplatiocu (slika 1.4)

---
---

### _**Kako kreirati matricu parametrizacije?**_

Nakon uspesnog prijavljivanja i prelaska na rutu ```/pregled```, u korisnickom interfejsu sa leve strane kliknuti na opciju ```Podesavanja```, a u podmeniju koji se otvara njenim odabirom, a koji sadrzi sekcije ```Parametrizacija```, ```Zbirni racuni```, ```Sifre banaka```, ```Kodovi uplate```, kliknite na sekciju ```Parametrizacija``` koja vas redirektuje na rutu ```/podesavanja/parametrizacija``` (slika 1.5)

slika 1.5
![image](images\parametrizacija.png)

Na slici 1.5, prikazane su prethodno sacuvane matrice parametrizacije. 

Dodavanje nove matrice parametrizacije zapocinjemo klikom na dugme ```Dodaj```.
Otvara se prozor za kreiranje matrice parametrizacije (slika 1.6), koji sadrzi sledeca polja:
- Naziv parametrizacije
- Prvi red (red od kog pocinju podaci za knjizenje)
- Iznos
- Racun
- Naziv
- Adresa
- Mesto
- PBO model
- PBO
- PBZ model
- PBZ 
- SIF (sifra placanja)
- Svrha

slika 1.6
![image](images\dodavanje-parametrizacije.png)

Polja dozvoljavaju unos brojeva i slova kao i dvotacku (```:```), u zavisnosti o kom se formatu dokumenta radi.

Primer jedne matrice parametrizacije za dokument u txt formatu, prikazan je na slici 1.7

slika 1.7
![image](images\TXT-parametrizacija.png)


Primer jedne matrice parametrizacije za dokument u XLS formatu, prikazan je na slici 1.8

slika 1.8
![image](images\XLS-parametrizacija.png)

Klikom na dugme ```Potvrdi``` kreirana matrica parametrizacije bice sacuvana

Pretraga zeljene parametrizacije vrsi se po Nazivu parametrizacije (moze i parcijalna pretraga, po delu naziva matrice) unosom u polje ```Naziv parametrizacije``` i klikom na dugme ```Pretrazi``` (```Enter```). Vracanje na pregled svih sacuvanih matrica parametrizacije vrsi se klikom na dugme ```Reset```. Prikaz matrica parametrizacije u tabeli moze se vrsiti u manje ili vise detalja pritiskom na dugme ```vise detalja``` ili ```manje detalja```. Moguce je i preuzimanje podataka o sacuvanim parametrizacijama. Klikom na dugme ```preuzmi stranu```, preuzima se trenutna strana sa sacuvanim matricama na ruti ```podesavanja/parametrizacija``` u formatu ```parametrizacija_{datum}.xlsx```. Preuzimanje podataka sa svih strana, ostvaruje se klikom na dugme ```preuzmi sve``` takoje u formatu ```parametrizacija_{datum}.xlsx```.

Postojecu matricu parametrizacije je moguce izmeniti kao i obrisati. Izmena se vrsi dvoklikom na matricu u tabeli koju zelimo da promenimo ili klikom na ikonicu izmeni u koloni ```Akcija```, kada se otvara prozor sa podacima matrice parametrizacije koju zelimo da izmenimo. Napravljene izmene cuvamo klikom na dugme ```Potvrdi```
Brisanje matrice parametrizacije se vrsi klikom na ikonicu ```Obrisi``` u koloni akcije. U prozorcicu sa upozorenjem (Da li ste sigurni da zelite da obrisete podatke?), kliknite na da kako bi potvrdili brisanje

---
---


### _**Kako parametrizovati podatke za knjizenje?**_

U korisnickom interfejsu sa leve strane kliknuti na opciju ```Podaci```. U podmeniju izabrati ```Editor```. Sistem nas redirektuje na rutu ```podaci/editor``` (slika 1.9).

slika 1.9
![image](images\podaci-editor.png)

Klikom na obavezno polje ```*Isplatilac```, sa desne strane se otvara prozor sa prikazanom tabelom svih isplatilaca koji su trenutno u sistemu (slika 2.0)

slika 2.0
![image](images\pretraga.png)

Pretraga odredjenog isplatioca vrsi se unosom imena isplatioca ili samo delimicnog imena u inputu za pretragu. Dvoklikom na odabranog isplatioca ili selektovanjem isplatioca i klikom na dugme ```Potvrdi```, potvrdjujemo odabir isplatioca za proces parametrizacije podataka za knjizenje. 
Nakon unosa Isplatioca, obavezno polje ```*Vrsta podataka``` se automatski popunjava sa onom vrednoscu koja je bila selektovana tokom unosenja isplatioca u sistem (spisak, fajl ili payroll). Ove vrednosti je moguce promeniti rucno, pri cemu se javlja upozorenje da su ucinjene izmene u vrednosti. Ukoliko je vrsta podataka Spisak ili Fajl, u polje ```*Payroll racun``` je moguce uneti brojeve racuna koji su ponudjeni u drop-down meniju, a koji se kreiraju na ruti ```/podesavanja/zbirniracuni```. Ukoliko je vrsta podataka ```Payroll```, tada se ispisuje jedinstveni payroll racun za tog isplatioca koji se nalazi u sistemu, a koji je unet prilikom kreiranja isplatioca. 
- klikom na ```Napred``` prelazi se u korak 2, ```upload``` (slika 2.1) 
 
slika 2.1
![image](images\upload.png)

Polje ```*Parametrizacija``` se automatski popunjava vrednoscu parametrizacije koja je uneta pri kreiranju isplatioca. Ona se moze izmeniti, pri cemu od sistema dobijamo upozorenje da smo izvrsili izmenu kao i da unetu izmenu potvrdimo.

- kliknuti na dugme ```Izaberi fajl``` kako bi ucitali dokument koji sadrzi podatke o knjizenju. Selektujte fajl koji odgovara izabranoj matrici parametrizacije i kliknite na ```Ucitaj fajl```. Sacekajte da se pojavi poruka da je fajl uspesno ucitan. U slucaju poruke o gresci, proverite da li je odabrana odgovarajuca matrica parametrizacije, kao i da li ucitani fajl odgovara zadatoj matrici parametrizacije. Ukoliko je fajl uspesno ucitan, za nastavak procesa kliknite na dugme ```Napred``` pri cemu se prelazi u korak 3 (Primaoci, slika 2.2).

slika 2.2
![image](images\Primaoci.png)

U koraku 3 (Primaoci), sistem prikazuje ime isplatioca, vrstu podataka (Spisak, Fajl ili Payroll) i racun (payroll racun), a u tabeli ispod podatke za knjizenje (Racun, Ime, Adresa, Grad, PBO Model, PBO, PBZ Model, PBZ, Svrha, SIF, Iznos). U ovom koraku, moguce je brisanje odgovarajucih redova iz tabele klikom na ikonicu ```Obrisi``` u koloni ```Akcije``` uz poruku upozorenja u prozorcicu. Obrisane redove moguce je povratiti klikom na dugme ```Resetuj``` uz poruku upozorenja u prozorcicu. Za nastavak u sledeci korak, kliknuti na dugme ```Napred```

slika 2.3
![image](images\Iznos.png)

U zavrsnom koraku 4 (Iznos), sistem prikazuje ukupan iznos naloga za knjizenje u polju ```*Iznos```, kao i datum za koji se taj nalog vezuje, a koji se moze izmeniti. Klikom na ```Sacuvaj``` pojavljuje se prozorcic (Da li ste sigurni da želite da sačuvate promene?), sa opcijama ```Potvrdi``` i ```Otkazi```. Klikom na potvrdi dobijamo poruku o uspesnom slanju na server i uspesnom kreiranju naloga za knjizenje, pri cemu nas sistem redirektuje na rutu ```/podaci/pregled``` (slika 2.4), gde se nalazi tabelarni prikaz svih prethodno kreiranih naloga za knjizenje

slika 2.4
![image](images\podaci-pregled.png)

Tabelarni prikaz naloga za knizenje sadrzi sledece kolone:
- ```Isplatilac``` - Ime isplatioca za koga je kreiran odgovarajuci nalog za knjizenje
- ```Iznos``` - Ukupan iznos naloga
- ```Datum``` - Datum na koji se nalog odnosi
- ```Vrsta podataka``` - Da li je u pitanju Spisak, Fajl ili Payroll
- ```Status podataka``` - Moze biti ```Upisan``` (status podataka nakon upisa/učitavanja i pre sprovedene kontrole), ```Neispravan``` (status podataka u slučaju da neka od kontrola nije zadovoljena, tj. da postoje neispravni nalozi), ```Validiran``` (status podataka u slučaju da postoje neispravni nalozi, ali smo odlučili da takve podatke propustimo dalje), ```Ispravan``` (status podataka u slučaju da su sve kontrole zadovoljene, tj. da su svi nalozi ispravni), ```Korigovan```(u slučaju da su nad podacima urađene korekcije, i da podaci nakon toga zadovoljavaju sve kontrole), ```Ponisten``` (status podataka u slučaju da iz nekog razloga želimo da poništimo učitane/upisane podatke), kao i ```Obrada``` ukoliko je nalog jos uvek u procesu obrade (videti sliku 2.4)
- ```Status``` - Statusi 2-8 (```2-Nema uplata```, ```3-Neupareno```, ```4-Povezivanje```, ```5-Upareno```, ```7-Validacija```, ```8-Proknjizeno```), kao i Status ```?-Nepoznat```

Redovi u tabelarnom prikazu za naloge za knjizenje koji imaju status ```Neispravan``` ili ```Obrada``` imaju status ```Nepoznat status``` i prikazani su crvenom bojom

_**Kada je nalog u procesu obrade, ceo proces provere naloga vrsi se asinhrono u pozadini. Stoga je potrebno s vremena na vreme osveziti stranicu klikom na dugme koje se nalazi u koloni ```Status podataka``` desno od statusa ```Obrada``` **_

Pretraga naloga za knjizenje moze se vrsiti po sledecim parametrima:

- Naziv isplatioca
- Pocetni datum-Krajnji datum
- Vrsta podataka
- Status podataka

Pretragu potvrdjujemo klikom na dugme ```Pretrazi```. Ponistavanje pretrage po odredjenim parametrima i izlistavanje svih kreiranih naloga za knjizenje vrsimo pritiskom na dugme ```Reset```. 

Selektovanjem odredjenog isplatioca u tabeli u gornjoj (master) formi, otvara se donja (details) tabelarna forma u kojoj su izlistani svi podaci (detalji) sa naloga za knjizenje koji je vezan za tog isplatioca (slika 2.5). Ti podaci se odnose na Racun, Iznos, Status racuna, Ime, koji se prikazuju u formi sa manje detalja, a u formi sa vise detalja jos i PBO Model, PBO, PBZ Model, PBZ, SIF, Svrha i Grad. I sa master i sa details forme je moguce preuzeti podatke klikom na ```preuzmi stranu```, kada se preuzima trenutna strana ili klikom na ```preuzmi sve``` kada se preuzimaju svi podaci. U master formi podaci se preuzimaju u formatu ```pregled-podataka_{datum}.xlsx```, a u details formi u formatu ```racuni_{datum}.xlsx```

slika 2.5
![image](images\master-details.png)

U slucaju da su tokom provere parametrizovanih podataka za knjizenje pronadjene odredjene nepravilnosti, u donjem (details) tabelarnom pregledu takvi redovi ce biti prikazani crvenom bojom a sadrzaj kolone tog reda kod kog je utvrdjena nepravilnost bice boldovan (zadebljani tekst- slika 2.6). Na krajevima tabelarnih redova za koje su utvrdjene nepravilnosti pojavljuju se ikonice ```Promeni``` i ```Potvrdi``` Opcija ```Promeni``` omogucava izmenu iskljucivo ziro racuna. Klikom na ```Promeni``` otvara se prozorcic ```Promena recuna``` u kojem se moze izmeniti postojeci ziro racun i potvrditi klikom na ```U redu```, pa ukoliko je racun validan on se prikazuje obojen zelenom bojom. Da bi sve promene bile sacuvane, mora se kliknuti na dugme ```Sacuvaj promene```. Ukoliko se stranica osvezi pre pritiska na dugme ```Sacuvaj promene```, iste nece biti sacuvane. Opcija ```Potvrdi``` omogucava ignorisanje nepravilnosti u tom redu details tabele. Tada ceo red koji je prethodno bio nevalidan, i oznacen crvenom bojom postaje validan i oznacen zelenom bojom. Takodje je posle potvrde potrebno kliknuti na dugme ```Sacuvaj promene``` da bi iste bile sacuvane.

Sve nevalidne redove jednog naloga za knjizenje mozemo izlistati cekiranjem opcije ```Nevalidno``` koja se nalazi levo od dugmeta ```Sacuvaj promene```

slika 2.6
![image](images\details-greska.png)

U slucaju da je ceo red validan on ce biti obojen zelenom bojom (slike 2.5 i 2.6)

Kada je u pitanju ziro racun koji ne pripada UCB, takav racun ce biti prikazan crnom bojom i za taj racun nece biti prikazan status. Ostale kolone u tom redu koje su validne, bice prikazane zelenom bojom (slika 2.7)

slika 2.7
![image](images\nije-UCB.png)


U gornjem (master) tabelarnom prikazu sa desne strane, nalazi se kolona ```Akcije``` (slike 2.4 i 2.5) koja sadrzi opcije: ```Izmeni```, ```Validiraj```, ```Ponisti``` i ```Obrisi```. Ove opcije su aktivne samo za naloge za knjizenje koji imaju statuse ```2```-```5```. Za statuse ```7``` i ```8``` ove opcije u koloni ```Akcije``` nisu dozvoljene.

- Akcija ```Izmeni``` omogucava nam izmenu podataka u nalogu za knjizenje. U izmenu podataka ulazimo pritiskom na dugme ```Izmeni``` u koloni ```Akcije``` ili dvoklikom na red u kojem se isplatioc nalazi. Tada nas sistem redirektuje na rutu ```/podaci/editor``` za izmenu prethodno unetih parametrizovanih podataka za knjizenje za odredjenog isplatioca a sam proces je identican postupku kreiranja parametrizovanih podataka za knjizenje i takodje se sastoji od 4 koraka (```Isplatilac```, ```Upload```, ```Primaoci``` i ```Iznos```). U 4-tom koraku, klikom na dugme ```Sacuvaj``` potvrdjujemo unete izmene, i posle upozorenja sistema (Da li ste sigurni da želite da sačuvate promene?) i klika na ```Potvrdi```, sistem nas vraca na rutu ```/podaci/pregled```. Status izmenjenog naloga sada dobija vrednost ```Korigovan```

- Akcija ```Validiraj``` omogucava nam da potvrdimo sve neispravne naloge (kako ne bi morali da ih potvrđujemo jedan po jedan). Status naloga posle validacije menja se iz ```Nepoznat``` u status ```2-Nema uplata```, koji se kasnije u zavisnosti od depozita vezanih za tog isplatioca moze menjati u status ```3-Neupareno``` ili ```5-Upareno```

- Akcija ```Ponisti``` omogucava nam da poništimo podatke, ali da oni ostanu zapisani. Status naloga posle ponistavanja prelazi u ```Ponisten```

- Akcija ```Obrisi``` omogucava nam da obrisemo podatke

---
---

### _**Kako rasknjiziti parametrizovane podatke (naloge)?**_

U korisnickom interfejsu sa leve strane kliknuti na opciju ```Nalozi```. U podmeniju izabrati ```Knjizenje```. Sistem nas redirektuje na rutu ```/nalozi/knjizenje``` na kojoj zapocinjemo proces rasknjizavanja naloga za knjizenje (slika 2.8).

slika 2.8
![image](images\knjizenje.png)

U tabelarnom prikazu na toj ruti nalaze se ```status``` naloga za knjizenje (od ```1-5```), ```ime isplatioca```, kao i ```datum``` kreiranja naloga. Statusi prikazani na ovoj strani mogu biti:
- status ```1``` (Nema podataka) - ukoliko postoji samo depozit za odredjeno pravno lice, a isplatioc jos uvek nije kreiran u sistemu
- status ```2``` (Nema uplata) - ukoliko postoji samo kreiran nalog za knjizenje za odredjenog isplatioca a nema uplate od strane istog isplatioca vezane za taj nalog
- status ```3``` (Neupareno) - ukoliko postoje i kreirani nalog za odredjenog isplatioca i depozit (uplata) za tog istog isplatioca, koji se slazu po ```datumima``` kao i po ```maticnom broju``` iz aplikacije sa ```maticnim brojem``` iz depozita, ali su sume u depozitu i kreiranom nalogu ```razlicite```. I depozit i nalog se sada nalaze u zajednickoj grupi i imaju status ```3``` -Neupareno. Naziv zajednicke grupe nosi naziv Isplatioca (npr GRADSKO SAOBRACAJNO PREDUZECE BEOGRAD JKP iz grupe Neupareno sa slike 2.8). 

Ukoliko su datum depozita i datum na koji je naznacen nalog za knjizenje razliciti iako se oni slazu po maticnim brojevima (isto pravno lice) onda depoziti ostaju u statusu ```1``` - Nema podataka, a kreirani nalog u statusu ```2```- Nema uplata

- status ```4``` (Povezivanje) -
- status ```5``` (Upareno) -  ukoliko postoje i kreirani nalog za odredjenog isplatioca i depozit (uplata) za tog istog isplatioca, koji se slazu po ```datumima``` (datum depozita i datum na koji je naznacen nalog za knjizenje)  kao i po ```maticnom broju``` iz aplikacije sa ```maticnim brojem``` iz depozita, i sume u depozitu i kreiranom nalogu su identicne, tada dolazi do automatskog uparivanja i takva grupa dobija status ```5``` - Upareno.

Pored automatskog moguce je i rucno uparivanje iz grupe sa statusom ```3``` - Neupareno. Rucno uparivanje je moguce jedino ukoliko je iznos veci ili jednak iznosu naloga. Moguce je rucno upariti i vise uplata za odredjenog isplatioca sa jednim nalogom za knjizenje takodje ukoliko su ispunjeni uslovi da je iznos selektovanih uplata veci ili jednak iznosu u nalogu.
Aplikacija ne sme da dozvoli ručno povezivanje nalog za knjiženje sa dve uplate koje su imale različit PBO, različit PBZ i različite šifre. Ukoliko se šifre u nalogu i sifra u depozitu razlikuju, prioritet uvek imaju šifre iz naloga. Ukoliko nedostaje neka šifra u nalogu za knjiženje, onda se ona dopunjuje sa šifrom iz uplate. Ukoliko u nalogu nedostaju sve šifre, tada svi podaci iz naloga dobijaju šifru iz uplate.

Detaljni pregled svih podataka (uplata i naloga za kniženje) prikazuju se klikom na opciju ```+``` koja se nalazi levo od podataka u koloni ```Status``` (slika 2.8)

Ručno uparivanje (mora se prvo otvoriti detaljni pregled) vrši se tako sto se u polju za štikliranje (check box) selektuje uplata ili vise njih i odgovarajuci nalog za knjizenje (videti sliku 2.9) 

slika 2.8
![image](images\rucno-uparivanje-ne.png)

Potvrda rucnog uparivanja vrsi se klikom na dugme ```Potvrdi``` koje se nalazi sa desne strane izabrane grupe za uparivanje

_**Međutim, u slučaju sa prethodne slike, ručno uparivanje nece biti moguće iz razloga sto je suma depozita niža od sume u nalogu za knjiženje**_ 

Kada su svi uslovi ispunjeni, tada grupa podataka iz statusa ```3``` - Neupareno, prelazi u status ```5``` - Upareno sto se moze videti na slici 2.9

slika 2.9
![image](images\status-5.png)

Pretraga podataka na ovoj ruti moze se vrsiti po nazivu isplatioca, statusima i po datumu, koji se potvrdjuju pritiskom na dugme ```Pretrazi```

Osvezivanje stranice vrsi se pritiskom na dugme ```Proveri```

Detaljini pregled moze se prikazati sa vise detalja, pritiskom na dugme ```vise detalja```

Preuzimanje detalja odredjene grupe vrsi se pritiskom na dugme ```Preuzmi stranu```

Potvrdu uparenih podataka ostvaruje se klikom na dugne ```Proknjizi``` (slika 2.9). Posle poruke o uspehu, ova grupa prelazi na rutu ```/nalozi/validacija``` i dobija status ```7``` (slika 3.0)

slika 3.0
![image](images\status-7.png)

Na ovoj ruti nalaze se jedino grupe podataka koje su u statusu ```7```- Validacija

Pretraga podataka u statusu ```7``` moze se vrsiti po nazivu isplatioca i datumu a potvrda klikom na ```Pretrazi```. Klikom na dugme reset ponistavaju se rezultati pretrage i izlistavaju sve grupe podataka sa statusom ```7```

Detaljni pregled svih podataka odredjene grupe u statusu ```7``` prikazuju se klikom na opciju ```+``` koja se nalazi levo od podataka u koloni ```Status``` (slika 3.1). 

slika 3.1
![image](images\detalji-7.png)

Na slici 3.1 prikazani su detalji vezani za uplate. Detalje vezane za nalog izlistavamo klikom na ```Nalozi```

Formirana grupa sa statusom ```7``` moze se ponistiti i vratiti u status ```5``` klikom na dugme ```Ponisti```

Operater koji je kreirao grupu u statusu ```7``` ne moze ici dalje u proces i ne moze validirati taj skup podataka sto se moze videti sa slike 3.1

U slucaju da je prijavljen operater koji nije kreator tog skupa podataka u statusu ```7```, dugme ```Validiraj``` ce biti vidljivo (slika 3.2).


slika 3.2
![image](images\dugme-validiraj.png)

Tada nas klikom na dugme ```Validiraj``` sistem redirektuje na rutu ```/nalozi/rasknjizeno```. 
Na toj strani se izlistavaju svi rasknjizeni podaci koji se nalaze u statusu ```8``` - Proknjizeno.
Pretraga tih rasknjizenih podataka vrsi se prema nazivu isplatioca i datumu naloga, a potvrdjuju klikom na dugme ```Pretrazi```. Klikom na dugme reset ponistavaju se rezultati pretrage i ponovo izlistavaju sve grupe podataka sa statusom ```8```