# Package-File-Service

Salt Quickstart - Salt stack Master and Slave on Ubuntu Linux

Nopeat ja yksinkertaiset ohjeet kuinka asentaa herra ja orja linuxille.

master$ sudo apt-get update
master$ sudo apt-get -y install salt-master
master$ hostname -I

slave$ sudo apt-get update
slave$ sudo apt-get -y install salt-minion

Jotta voit ottaa uudet asetukset käyttöön ja yhdistää orjan herraan pitää restarttaa komennolla.
slave$ sudo systemctl restart salt-minion.service
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Salt official documentation: Salt Getting Started Guide-kirjasta luvut Understanding SaltStack ja SaltStack Fundamentals ja SaltStack Configuration Management: Functions

- Erittäin kattava step by step guide saltin ympäristöstä, jonka avulla asennat ja säädät saltstackkeja.

- Annat komentoja etänä kaikkien järjestelmien kesken

- Pystyt automatisoimaan infrastruktuurisi saltreactorin avulla


a)
