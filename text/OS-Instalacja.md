#Instalacja#
*************

## 1. Skąd pobrać obrazy płyt?
[http://www.linuxmint.com/download.php](http://www.linuxmint.com/download.php)
## 2. Jaką wersje wybrać?
  
    
##Cinnamon
Przeznaczony jest na mocniejsze maszyny. Duży apetyt na RAM (minimum 1GB rekomendowany).
      
###Minimalne wymagania dla kart graficznych:

__Intel__ : i945G lub nowszy

__ATI__ : Radeon X1xxx lub nowszy

__NVIDIA__ : Geforce 6xxx lub nowszy , Geforce 7xxx lub nowszy rekomendowany


##MATE
Bazujący na GNOME2, można wykorzystać na słabszych maszynach bez sprzętowej akceleracji 3D.

##XFCE
Proste, ale jednocześnie funkcjonalne środowisko. Można zainstalować na słabszych maszynach.
Nie wymaga akceleracji 3D. Lżejsze i szybsze od Mate.

## 3. Jak ustawić partycje?
###[+] Wariant 1 - czysty dysk
|           |           |
---         |----       |----   
__/__       |`10-20 GB` | główna partycja
__/home__   |`???`      | partycja dla kont użytkowników
__swap__    |`0-??`     | przestrzeń wymiany

Na głównej partycji zostanie zainstalowany system oraz większość aplikacji. Tu musimy zadbać o odpowiednio dużą przestrzeń.

W wiekszości przypadków nie ma potrzeby wydzielania osobnej partycji __/boot__. Wielu początkujących użytkowników o to pyta.
Osobna partycja /boot przydaje się np. kiedy chcemy zaszyfrowac resztę dysku. Partycja zawierać będzie kernel i musi on znajdować sie własnie na niezaszyfrowanej partycji po to abyśmy mogli uruchomić system. Dopiero na etapie bootowania systemu nastąpi załadowanie odpowiednich modułów do deszyfracji dysku (więcej o szyfrowaniu będzie dalej)
  
[Partycja SWAP](http://pl.wikipedia.org/wiki/Partycja_wymiany), czyli przestrzeń wymiany nie jest wymagana. Jeśli komputer posiada dużo RAMu, np. 4-8GB, to można zrezygnować ze SWAPu.
Jednak należy przemyśleć takie podejście. Brak SWAPu uniemożliwi skonfigurowanie hibernacji.
Jeśli zależy nam na takiej funkcjonalności, wtedy warto ustawić wielkość SWAP równą ilości RAMu w komputerze.

Jakie katalogi i do czego są używane można się dowiedzieć z [tego](http://pl.wikibooks.org/wiki/Linux/System_plik%C3%B3w/Drzewo_katalog%C3%B3w) zestawienia.
Powinno to ułatwić podjęcie decyzji o tym, dla których katalogów wydzielić partycje.

###[+] Wariant 2 - Windows + Linux

 


## 4. Czy LinuxMint obsługuje język polski?
## 5. Co zrobić aby system był po polsku?
## 6. Jak ustawić język polski w aplikacjach?

