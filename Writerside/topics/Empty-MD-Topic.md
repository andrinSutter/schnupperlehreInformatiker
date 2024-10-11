# Zusammenfassung: Zahlensysteme (Binär und HEX)

## 1. Binärsystem (Dualsystem)
- **Basis**: 2 (Zwei mögliche Zustände: 0 und 1)
- **Verwendung**: Grundlegendes System in der digitalen Elektronik und Informatik.
- **Zahlendarstellung**: Jede Stelle repräsentiert eine Potenz von 2.

| Dezimal      | 1    | 2    | 4    | 8    | 16        | 32        | 64        |
|--------------|------|------|------|------|-----------|-----------|-----------|
| Binär        | 0001 | 0010 | 0100 | 1000 | 0001 0000 | 0010 0000 | 0100 0000 |
| Potenz von 2 | 2^0  | 2^1  | 2^2  | 2^3  | 2^4       | 2^5       | 2^6       |


### Umrechnung von Binär nach Dezimal:
Beispiel: 1011

| Binär   | 2^3 | 2^2 | 2^1 | 2^0 |
|---------|-----|-----|-----|-----|
| Bespiel | 1   | 0   | 1   | 1   |

Wir haben bei den Werten 1, 2 und 8 eine 1 das bedeutet wir rechnen: $1 + 2 + 8 = 11$

### Umrechnung von Dezimal nach Binär:

Wir dividieren die Anfangszahl durch 2 und schreiben den Rest auf mit dem Resultat machen wir dasselbe bis wir bei 0 angekommen sind. 

13 ÷ 2 = 6 Rest 1   
6 ÷ 2 = 3 Rest 0  
3 ÷ 2 = 1 Rest 1   
1 ÷ 2 = 0 Rest 1 

Am Ende liest man die binäre Zahl von unten nach oben von den Resten ab. 
Also ist die dezimale Zahl 13 in binär: 1101

## 2. Hexadezimalsystem (HEX)
- **Basis**: 16 (Sechzehn mögliche Zustände: 0-9 und A-F, wobei A=10, B=11, ..., F=15)
- **Verwendung**: Kompakte Darstellung von Binärzahlen, Speicheradressen, Farben in Webdesign (RGB).
- **Zahlendarstellung**: Jede Stelle repräsentiert eine Potenz von 16.

| Dezimal       | 1    | 16   | 256   |
|---------------|------|------|-------|
| Hexadezimal   | 1    | 10   | 01 00 |
| Potenz von 16 | 16^0 | 16^1 | 16^2  |

| Dezimal | Hexadezimal |
|---------|-------------|
| 0       | 0           |
| 1       | 1           |
| 2       | 2           |
| 3       | 3           |
| 4       | 4           |
| 5       | 5           |
| 6       | 6           |
| 7       | 7           |
| 8       | 8           |
| 9       | 9           |
| 10      | A           |
| 11      | B           |
| 12      | C           |
| 13      | D           |
| 14      | E           |
| 15      | F           |

### Umrechnung von Hexadezimal nach Dezimal:
Beispiel: 2F

| HEX      | 16^1 | 16^0 |
|----------|------|------|
| Beispiel | 2    | F    |

Wir machen bei Hex fast das gleiche wie bei Binär. Anders als bei Binär müssen wir die den Wert mit seinem Stellenwert multiplizieren. 

Das heisst wir nehmen die erste Stelle da haben wir F das heisst wir rechnen 15 * 1. An der Zweiten Stelle haben wir eine 2 das heisst 2 * 16

**Rechnung**: $15 * 1 + 2 * 16 = 47$

### Umrechnung von Dezimal nach Hexadezimal:

Selbe System wie bei Binär wir nehmen die Zahl und Teilen sie durch 16 notieren den Rest und führen das solange durch bis wir bei 0 angekommen sind. Am Schluss lesen wir den Rest von unten nach oben.

47 ÷ 16 = 2 Rest 15  
2 ÷ 16 = 0 Rest 2

Jetzt müssen wir 15 noch zu F umschreiben und dan kommen wir auf **2F**

## Aufgaben: Zahlensysteme

1. **Konvertiere die binäre Zahl 10 1110 in das Dezimalsystem.**
2. **Konvertiere die hexadezimale Zahl 03 A3 in das Dezimalsystem.**
3. **Addiere die binäre Zahl 1010 und 1101 und gib das Ergebnis in allen drei Systemen an.**


### Spielerischer Aspekt 2
- **Memory-Spiel**: Karten mit Zahlen in Binär-, Dezimal- und Hex-System z.B., 1010, 10, A

---

## IPv4-Adressierung

Eine IPv4-Adresse besteht aus 32 Bit, die in vier Oktetten dargestellt werden, wobei jedes Oktett durch einen Punkt getrennt ist. Jedes Oktett kann einen Wert von 0 bis 255 annehmen. Zum Beispiel:

192.168.0.1

### Struktur der IPv4-Adresse

Eine IPv4-Adresse wird in zwei Hauptteile aufgeteilt:
1. **Netzwerkanteil**
2. **Hostanteil**

Die Netzmaske bestimmt, welcher Teil der IP-Adresse dem Netzwerkanteil und welcher dem Hostanteil zugeordnet wird.

### Klassenbasierte Adressierung

Ursprünglich wurden IPv4-Adressen in Klassen unterteilt:

| Klasse | Netzanteil | Hostanteil                       | Bereich der ersten Oktette | Beispiel    |
|--------|------------|----------------------------------|----------------------------|-------------|
| A      | 8 Bit      | 24 Bit                           | 0 - 127                    | 10.0.0.1    |
| B      | 16 Bit     | 16 Bit                           | 128 - 191                  | 172.16.0.1  |
| C      | 24 Bit     | 8 Bit                            | 192 - 223                  | 192.168.0.1 |
| D      | Multicast  | Nicht für Hostadressen verwendet | 224 - 239                  | -           |
| E      | Reserviert | Für zukünftige Verwendung        | 240 - 255                  | -           |

### Private Adressbereiche

Bestimmte Adressbereiche sind für private Netzwerke reserviert und nicht routbar im Internet:

- **Klasse A:** 10.0.0.0 - 10.255.255.255
- **Klasse B:** 172.16.0.0 - 172.31.255.255
- **Klasse C:** 192.168.0.0 - 192.168.255.255

### Subnetting

Subnetting ist der Prozess der Aufteilung eines großen Netzwerks in kleinere Subnetze. Dies wird unter Verwendung von Subnetzmasken erreicht. Eine Subnetzmaske hat ebenfalls eine Länge von 32 Bit und wird häufig in der Dezimalnotation dargestellt, ähnlich einer IP-Adresse.

#### Beispiel einer Subnetzmaske

Wenn wir eine IP-Adresse `192.168.1.0` mit der Subnetzmaske `255.255.255.0` haben, bedeutet das:

- Netzwerkanteil: Die ersten 24 Bit (`192.168.1`)
- Hostanteil: Die letzten 8 Bit (`0-255` für Geräte im Netzwerk)

### CIDR (Classless Inter-Domain Routing)

CIDR erlaubt die flexible Zuweisung von IP-Adressen:
- CIDR-Notation verwendet einen Schrägstrich `/` gefolgt von der Anzahl der Bits, die zum Netzwerkanteil gehören.
- Zum Beispiel: `192.168.1.0/24` gibt an, dass die ersten 24 Bit für das Netzwerk sind und die restlichen 8 Bit für Hosts.

### Berechnung der verfügbaren Hosts

Die Anzahl der verfügbaren Hosts in einem Netzwerk wird berechnet, indem die Anzahl der Bits im Hostanteil betrachtet wird:
- Für ein Netzwerk mit `/24`, gibt es 8 Bits für Hosts.
- Anzahl der Hosts = $2^8 - 2 = 254$ (wir subtrahieren 2 für die Netzwerkaadresse und die Broadcast-Adresse).

### Zusammenfassung

IPv4-Adressierung spielt eine wichtige Rolle im Netzwerkdesign und -management. Sie ermöglicht die eindeutige Identifizierung von Geräten in einem Netzwerk und die effiziente Nutzung von Adressen durch Unterteilung in Subnetze.
