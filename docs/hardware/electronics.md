# Elektrische Komponenten
Für die ADClock wurde ein eigene Platine entworfen, auf der ein Arduino ATmega328p sitzt.
Dieser übernimmt die Steuerung der Motoren und liest die Hall-Sensoren aus.
Außerdem ist dieser für die Datenkommunikation verantwortlich.

Die Platine stellt für alle Verbindungen Pins bereit, sodass die Kabel für die Motoren, Hall-Sensoren, Stromversorgung und Datenkommunikation nur drauf gesteckt werden müssen.

## Controller 
Der Chip Arduino ATmega328p benötigt folgende Komponenten, damit dieser lauffähig ist:
- TODO

## Platine
Alle diese Komponenten sind auf der Platine installiert. 

Die Leiterbahnen sind auf zwei Ebenen angeordnet.

## Schrittmotoren
Pro Uhr sind zwei Schrittmotoren verbaut, die jeweils einen Zeiger steuern.
Die Schrittmotoren des Modells TODO besitzen vier Spulen und können sich unendlich oft in eine Richtung drehen.

## Hallsensoren
Da sich die Schrittmotoren frei bewegen können, ist eine Kalibrierung erforderlich. Dies geschieht über zwei Hallsensoren, welche jeweils für einen Motor zuständig sind.

An den Zahnrädern sind kleine Magneten befestigt, welche durch die Rotation des Zahnrads durch den Messbereich der Hallsensoren wandern. Die Sensoren sind so platziert, dass diese die “12 Uhr” Stellung erkennen können.

Weitere Informationen zum Ablauf der Kalibrierung sind in TODO beschrieben.


## Stromversorgung 
Alle elektronischen Komponenten benötigen eine Spannung von 5V. 

In dem ursprünglichen Entwurf sollten die Schrittmotoren ebenfalls über die Platine mit Strom versorgt werden. Dies ist jedoch nicht möglich, da die Motoren beliebig viel Strom ziehen & die Controller dadurch resetten.
In einer zukünftigen Version sollte dieses Problem gelöst werden.
Aktuell ist dieses Problem durch zwei getrennte Stromkreise gelöst. 

Um die Installation mit ausreichend Strom zu versorgen, werden zwei Netzteile verwendet:
- TODO