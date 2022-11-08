# Package-File-Service

Salt Quickstart - Salt stack Master and Slave on Ubuntu Linux

Nopeat ja yksinkertaiset ohjeet kuinka asentaa herra ja orja linuxille.

master$ sudo apt-get update
master$ sudo apt-get -y install salt-master
master$ hostname -I

slave$ sudo apt-get update
slave$ sudo apt-get -y install salt-minion

Jotta voit ottaa uudet asetukset käyttöön ja yhdistää orjan herraan pitää restarttaa komennolla.
slave$ sudo systemctl restart salt-minion.service HUOM! toiminto tulee suorittaa aina uudelleen, jotta uudet asetukset tulevat voimaan.



Salt official documentation: Salt Getting Started Guide-kirjasta luvut Understanding SaltStack ja SaltStack Fundamentals ja SaltStack Configuration Management: Functions

- Kattava step by step guide saltin ympäristöstä, jonka avulla asennat ja säädät saltstackkeja.

- Annat komentoja etänä kaikkien järjestelmien kesken

- Pystyt automatisoimaan infrastruktuurisi saltreactorin avulla

- Pystyt komentamaan 10 tai 1000 orjaa reaaliaikaisesti


a) Asennetaan apache

sudo apt-get update

sudo apt-get install apache2
asennus alkaa
lopuksi vastaa "yes"

Tämän jälkeen testataan että apache toimii eli käynnistetään ohjelma komennolla
sudo systemctl start apache2.service

tämän jälkeen voidaan testata että toimiiko juuri asentamamme apache komennolla
sudo service apache2 status
process is running joten asennus on sujunut onnistuneesti.


b) Asennetaan master.

sudo apt-get update
sudo apt-get install salt-master
ja hyväksytään valitsemalla "yes"

asennetaan minion eli orja

sudo apt-get update
sudo apt-get install salt-minion -y

Tämän jälkeen orjan pitää saada tietää missä master on.

sudoedit /etc/salt/minion

hostname "ip osoite"
id: Jarkko

tämän jälkeen bootataan, jotta asetukset tulevat voimaan. 

sudo systemctl restart salt-minion.service

c)


