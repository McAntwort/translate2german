# translate2german
**Übersetzung der pi-hole Weboberfläche auf deutsch**
<br>
<br>
Mit diesem Script wird die Weboberfläche Version 5.11 des Pi-hole auf deutsch übersetzt.
<br>
<br>
**Achtung! Dieses Script funktioniert (zur Zeit) nur unter Raspberry Pi OS Buster vom 07.05.2021**
<br>
Download unter: [https://downloads.raspberrypi.org/raspios_lite_armhf/images/raspios_lite_armhf-2021-05-28/2021-05-07-raspios-buster-armhf-lite.zip](https://downloads.raspberrypi.org/raspios_lite_armhf/images/raspios_lite_armhf-2021-05-28/2021-05-07-raspios-buster-armhf-lite.zip) 
<br>
<br>
Bevor die Übersetzung beginnt, wird

das Verzeichnis<br>
```bash
/var/www/html/
```

und die Dateien<br>

```bash
/usr/local/bin/pihole
/opt/pihole/gravity.sh
```

gesichert.
<br>
<br>

**Bevor Sie mit der Übersetzung beginnen:**

* haben Sie ein Backup von Ihrem System gemacht,
* haben Sie sich vom Quellcode überzeugt,
* wissen Sie, dass Sie alles auf eigene Gefahr tun,
* ...
<br>
<br>

**Installationsanleitung:**

Wer schnell und bequem loslegen möchte, kann die Übersetzung mit folgendem Befehl starten:

```bash
sudo curl -sSL https://raw.githubusercontent.com/pimanDE/translate2german/master/translate2german.sh | bash
```
<br>
Alternativ kann die Übersetzung auch folgendermaßen durchgeführt werden:

```bash
wget https://raw.githubusercontent.com/pimanDE/translate2german/master/translate2german.sh
chmod 775 translate2german.sh
sudo ./translate2german.sh
```
<br>
<br>

**Hinweise:**

* getestet unter Pi-hole Version v5.9 FTL Version 5.14 und Web Interface Version v5.11
* **vor einer Aktualisierung der Web Interface Version (pihole -up) muss erst das Backup zurückgespielt werden (siehe weiter unten)**
* ...
<br>
<br>

**Screenshot:**
<br>
![img](https://raw.githubusercontent.com/pimanDE/translate2german/master/pihole-weboberfl%C3%A4che-auf-deutsch.png)
<br>
<br>
<br>

**Rückgängig machen:**

Wenn Sie die Übersetzung wieder rückgängig machen wollen:

```bash
bash -c "$(curl -sSL https://raw.githubusercontent.com/pimanDE/translate2german/master/restore2translate.sh)"
```
<br>
Alternativ kann die Übersetzung auch folgendermaßen rückgängig gemacht werden:
<br>

```bash
sudo rm -r /var/www/html/
sudo rm -r /usr/local/bin/pihole
sudo rm -r /opt/pihole/gravity.sh
```

XXX = Datum der Sicherung im Format 'YYYYMMDD - HHMMSS'

```bash
sudo mv /var/www/html.sicherung.vom.XXX /var/www/html/
sudo mv /usr/local/bin/pihole.sicherung.vom.XXX /usr/local/bin/pihole
sudo mv /opt/pihole/gravity.sh.sicherung.vom.XXX /opt/pihole/gravity.sh
```
