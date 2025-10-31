# 🛡️ Proiect: ESP32 Marauder

Bun venit! Acest proiect documentează construcția a faimosului **ESP32 Marauder**, un instrument portabil de testare (penetration testing) pentru WiFi și Bluetooth.

Proiectul original și tot meritul aparțin lui **[justcallmekoko](https://github.com/justcallmekoko/ESP32Marauder)**. Acest repo servește doar ca un jurnal al componentelor folosite și al pașilor de asamblare.


---

## 🛒 Listă de Materiale (Bill of Materials)

Pentru a replica această construcție, am folosit următoarele componente:

* [ ] 1x Placă de Dezvoltare **ESP32** (cu WiFi și Bluetooth 4.2)
* [ ] 1x Afișaj tactil **TFT LCD 2.8"** (240x320px) cu cititor SD SPI
* [ ] 2x **Mini Breadboard**
* [ ] 1x Set de **fire Rigide** pentru Breadboard (Jumper Wires)
* [ ] 1x Header de Pini Mamă 5p (2.54 mm)
* [ ] 1x Header de Pini Mamă 8p (2.54 mm)
* [ ] 1x Header de Pini Mamă 6p (2.54 mm)

---

## 🚀 Pași de Instalare

Procesul de instalare are două etape majore: flash-uirea firmware-ului și asamblarea hardware.

### 1. 💾 Flash-uirea Firmware-ului

Înainte de a conecta firele, este esențial să încărcați software-ul pe placa ESP32.

1.  **Descărcați Fișierele:**
    * Navigați la secțiunea **[Releases](https://github.com/justcallmekoko/ESP32Marauder/releases)** a repository-ului oficial.
    * Descărcați cele patru fișiere `.bin` necesare din cel mai recent release:
        * `esp32_marauder.ino.bootloader.bin`
        * `esp32_marauder.ino.partitions.bin`
        * `boot_app0.bin`
        * `esp32_marauder_v1_8_9_20251030_old_hardware.bin`

2.  **Utilizați Web Flasher:**
    * Accesați utilitarul web **[https://esptool.spacehuhn.com/](https://esptool.spacehuhn.com/)**.
    * Conectați placa ESP32 la computer prin USB.
    * Apăsați **"Connect"** și selectați portul COM corespunzător.

3.  **Încărcați Fișierele:**
    * Adăugați cele 4 fișiere `.bin` pe care le-ați descărcat, asigurându-vă că fiecare este la adresa de memorie corectă (de obicei, instrumentul le recunoaște automat).
    * Apăsați **"Program"** și așteptați finalizarea procesului.

### 2. 🔌 Asamblarea Hardware (Wiring)

Aceasta este cea mai migăloasă parte. Urmați cu atenție schema de conectare.

1.  **Consultați Documentația:**
    * Mergeți la pagina oficială Wiki: **[IC Connections](https://github.com/justcallmekoko/ESP32Marauder/wiki/ic-connections)**.

2.  **Găsiți Schema:**
    * Derulați în jos până la secțiunea specifică pentru **"TFT Touch Screen"** (modelul de 2.8 inch).

3.  **Conectați Componentele:**
    * Poziționați placa ESP32 pe breadboard așa cum este indicat în diagrama de pe wiki.
    * Folosind firele de tip jumper, conectați cu atenție fiecare pin de la ESP32 la pinul corespunzător de pe afișajul TFT.
    * **Verificați de două ori toate conexiunile!** O conexiune greșită este cea mai frecventă cauză a problemelor.



---

## 🙏 Mulțumiri

Felicitări și mulțumiri lui **[justcallmekoko](https://github.com/justcallmekoko)** pentru crearea și menținerea acestui proiect extraordinar.

## ⚠️ Disclaimer

Acest instrument este destinat **exclusiv** scopurilor educaționale și de testare autorizată. Nu utilizați acest dispozitiv pe rețele sau echipamente pe care nu le dețineți sau pentru care nu aveți permisiunea explicită de a le testa. Fiți responsabil!
