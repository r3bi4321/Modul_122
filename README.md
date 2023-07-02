Modul_122

# Vergleichsoperatoren

In diesem Portfolio werde ich die Vergleichsoperatoren von PowerShell beschreiben. Dazu brauche ich ein Beispiel aus dem Projekt vom Modul 122.

Bei dem Projekt habe musste ich dafür sorgen, dass ein Benutzer unterschiedliche Optionen wählen kann und die unterschiedlichen Optionen andere Outputs haben.

Die Operatoren werden, anders als bei C# wie Parameter geschrieben. Hierbei gibt es folgende Operatoren.

| Operator| Beschreibung|
|--------- |-------------|
|-eq | gleich|
|-ne | ungleich|
|-lt| kleiner|
|-le| kleiner oder gleich|
|-gt| grösser|
|-ge| grösser oder gleich|

Code:

```$DataLog = "C:\Users\rebec\OneDrive\Dokumente\DataLog_M122.txt"
$Date= Get-Date
$catch = $true

while($catch -eq $true){
$desicion = Read-Host "bbb,kanti oder privat"
#BBB
if ($desicion -eq "bbb"){
start https://moodle.bbbaden.ch
start C:\Users\rebec\OneDrive\Dokumente\BBB
$catch = $false
}
#Kanti
elseif ($desicion -eq "kanti") {
start https://www.schul-netz.com/baden/index.php
start C:\Users\rebec\OneDrive\Dokumente\Kanti
$catch = $false
}

#privat
elseif ($desicion -eq "privat")
{
start spotify
$catch = $false
}

else{
Write-Output "Falsche Eingabe, versuchen sie es noch einmal. "
$catch = $true
}
}
Add-Content $DataLog -Value " $date $desicion "
```
Wie man sehen kann, sind die Vergleichsoperatoren immer mit einem - vorher. Die anderen Operatoren, wie zum Beispiel =, sind hier Zuweisungsoperatoren für Variablen.

**Reflexion:**

Das Thema mit den Vergleichsoperatoren fand ich am Anfang nicht sehr einfach, da ich mir nicht gewohnt war, die Operatoren auszuschreiben. Somit habe ich immer die Zuweisungsoperatoren bei einem Vergleich verwendet. Dies brachte dann Fehler im Skript hervor, welche ich zu Beginn nicht verstanden habe. Jedoch konnte ich mich mit etwas Übung schnell daran gewöhnen und beherrsche die Operatoren mittlerweile recht gut.
