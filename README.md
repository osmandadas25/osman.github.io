- Name: Osman Celik
- Datum: 11.02.2026
- Fach: ITS
- Thema: Shell Pipes

```sh
https://www.franzmatejka.at/htl/doc/ITSI_2_linux/testdata/klassenkassa.csv
```

```sh
Befehl: curl, ladet die Datei herunter (curl &Dateilink)

Befehl: grep, gibt das eingegebene String in der Datei (grep &String &Dateiname) auf der Konsole aus

Befehl: pipes: "|", der output vom letzten Befehl (in der Zeile) wird der Input vom nächsten

tr.. translate, einzelne Zeiche durch andere ersetzen bzw. löschen
echo babababa | tr a x (Output: bxbxbxbx)

shuf... shuffle, input in zufällige Reihenfolge bringen
```
## Übung 4.1 (Klassenkassa)

```sh
head -n 9 klassenkassa.csv | grep Werkstatt 
```



## Übung 4.2 (Klassenkassa)

```sh
grep Sophia klassenkassa.csv | grep Bus
```



## Übung 4.3 (tr)

 ### https://man7.org/linux/man-pages/man1/tr.1.html
 
```sh
cat klassenkassa.csv | tr [:lower:] [:upper:]
```



## Übung 4.4 (shuffle)

```sh
shuf -n 10 klassenkassa.csv | tr "," "\t"
```



## Übung 4.5 (Zufällig)

```sh
grep Jonas klassenkassa.csv | shuf -n 1
```




## Übung 4.56 (ROT13)

```sh
curl -O https://www.franzmatejka.at/htl/doc/ITSI_2_linux/testdata/p4ssw0rds.txt
cat p4ssw0rds.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```



## Übung 4.7 (LeNA)

```sh
cat klassenkassa.csv | tr [:upper:] [:lower:] | grep lena
```



## Übung 4.8 (Zufällig)

```sh
seq 1000 2000 | ./c/summiere (Output: 1501500)
```



## Übung 4.9 (tail)

### https://man7.org/linux/man-pages/man1/tail.1.html



## Übung 4.10 (head/tail)

```sh
ls -l /etc | head -n 15 | tail -n 5
```



## Übung 4.11 (grep)

```sh
Option: -i, ignoriert ob die Buchstaben klein oder groß sind (Diese Option wäre bei der LeNA Aufgabe sinnvoll)
grep -i Lena klassenkassa.csv

Option: -c, die Anzahl der übereintstimmenden Zeilen wird ausgegeben 
grep -c Lena klassenkassa.csv

Option: -n, gibt zusätzlich auch die Nummer der Zeilen aus
grep -n Lena klassenkassa.csv
```



## Übung 4.12 (date input format)

```sh
Heute in 4 Wochen:
Heute vor 4 Wochen: echo "today 4 weeks ago" | date +"%d.%m.%Y (%A, KW%V)" -f -
90 Tage nach 15.10.2023: 
Letzter Freitag vor einem Jahr: 
Kommender Freitag in 6 Monaten: 
1639927239 Sekunden seit 01.01.1970: 

```
