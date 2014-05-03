#Karty graficzne, drivery, obraz#
*************

## 1. Jak sprawdzić jaką mam karte graficzną?

Polecenie:  
    **lspci -nn**

Zwróci przykładowo m.in. taką informację:

`04:00.0 VGA compatible controller [0300]: NVIDIA Corporation GT218 [ION 2] [10de:0a76] (rev ff)`

Kluczowe dla nas informacje to:  
1. Widzimy, ze mamy kartę **NVIDIA GT218**  
2. Identyfikator urządzenia to: 10de:**0a76** (___DEVICE PCI ID___)  
3. W tym przypadku widzimy,że to jest karta hybrydowa drugiej generacji: ION 2  

Fragment identyfikatora wykorzystamy do odnalezienia naszego sprzętu na liście obsługiwanych urządzeń w instrukcji sterownika.  


## 2. Jak dobrać sterownik do karty NVIDIA?

Kiedy znamy już model i identyfikator karty - czas odnależć sterownik.
W tym celu udajemy się na stronę [http://www.nvidia.com/object/unix.html](http://www.nvidia.com/object/unix.html) i wybieramy sterownik dla odpowiedniej architektury.
Najczęściej to będzie: **x86** (dla 32 bitowej architektury) lub **x86_64** (dla 64 bitowej architektury)

Sprawdźmy zatem czy wersja 331.67 obsługuje naszą kartę. Wybieramy arch x86_64 i w zakładce **Additional Information** znajdujemy link do pliku [README](http://us.download.nvidia.com/XFree86/Linux-x86_64/331.67/README/index.html).  
W spisie treści odnajdujemy sekcje [Supported NVIDIA GPU Products](http://us.download.nvidia.com/XFree86/Linux-x86_64/331.67/README/supportedchips.html)  

Po kliknięciu pojawi nam się lista obsługiwanego sprzętu. Interesuje nas kolumna ___Device PCI ID___.
Jak widzimy nasze ID znajduję się na liście (0x**0a76**) pod nazwą **Second Generation ION**
Zatem ta wersja sterownika obsługuje nasz sprzęt i taki należy pobrać i zapisać w swoim katalogu domowym.

__Z terminala:__  
`wget http://us.download.nvidia.com/XFree86/Linux-x86_64/331.67/NVIDIA-Linux-x86_64-331.67.run`

Pobrać możemy też poprzez kliknięcię na przycisk [Download](http://us.download.nvidia.com/XFree86/Linux-x86_64/331.67/NVIDIA-Linux-x86_64-331.67.run)

Jeśli nie widzimy tam naszego identyfikatora, to próbujemy odszukać go w innych [liniach sterowników](http://www.nvidia.com/object/unix.html). Jeśli dysponujemy dość starym sprzętem to najprawdopodobniej będzie to któraś z linii ___legacy___.  

## 3. Jak zainstalować sterownik do karty NVIDIA?

 a) w trybie konsoli (wyjscie z X'ow: CTRL+ALT+F2)  
 b) zabijamy proces Xorg (np. kill `pidof X`)  
 c) sudo apt-get update  
 d) sudo apt-get upgrade  
 e) sh NVIDIA-Linux-x86_64-331.67.run  
 f) restart  


