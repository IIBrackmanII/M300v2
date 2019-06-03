# M300 Seitz
27.05.2019
Überarbeitung vagrant file, hinzufügen von SHELL Befehlen
  # documentation for more information about their specific syntax and use.
   config.vm.provision "shell", inline: <<-SHELL
		sudo su 
		apt-get update
		apt-get upgrade -y 
		apt-get install -y apache2
		apt-get install ufw
		sudo systemctl enable ufw
		sudo ufw allow 80/tcp
   SHELL

   Im Moment ist es möglich eine Virtuellle Maschine auszusetzen auf der ein apache Webserver läuft. 
   Es finded der Versuch statt mit einer Windows Maschine ob der Webserver läuft.

   Update: 03.06.2019
   Das mit der Windows Maschine hat nicht funktioniert bei vagrant up, ich verwende deshalb jetzt ein Ubuntu 18.04. dort bin ich in das problem mit den gleichen IP-Adressen reingelaufen. Dies konnte ich leider aufgrund meines heutigen zustandes nicht mehr automatisiert lösen.

   Wissensstand
  	 Linux: Linux ist ein Betriebssystem wie Windows. Allerdings sind die meisten Linux-Betriebssysteme kostenlos und können viel freier konfiguriert werden.
	Linux basiert auf dem Betriebssystem Unix, das häufig in Rechenzentren oder Universitäten eingesetzt wird.
	Maßgeblich für die Entwicklung von Linux war und ist der finnische Programmierer Linus Torvalds.
	Im Jahr 1991 wurde Linux das erste Mal öffentlich zur Verfügung gestellt.
	Bis heute ist Linux kostenlos und ein sogenanntes freies Betriebssystem. Das heißt, der Quellcode ist frei zugänglich und jeder kann an der Weiterentwicklung mitarbeiten.
	Es gibt inzwischen zahlreiche Linux-Varianten wie beispielsweise das kostenlose Ubuntu oder Mint. Die können Sie jeweils sowohl als 32 Bit wie auch als 64 Bit Version bekommen. Zudem haben beide eine schicke Oberfläche und erinnern sehr an Windows. Für den Einstieg für Windows-Umsteiger sind sie also sehr gut geeignet.
	Virtualisierung: Virtualisierung bezeichnet in der Informatik die Nachbildung eines Hard- oder Software-Objekts durch ein ähnliches Objekt vom selben Typ mit Hilfe eines Abstraktions-Layers. Dadurch lassen sich virtuelle Geräte oder Dienste wie emulierte Hardware, Betriebssysteme, Datenspeicher oder Netzwerkressourcen erzeugen
	Vagrant: Vagrant ist eine freie Ruby-Anwendung zum Erstellen und Verwalten von virtuellen Maschinen
	Git: GitHub ist ein Onlinedienst, der Software-Entwicklungsprojekte auf seinen Servern bereitstellt.
	Virtualbox: Ein von Oracle entwikeltes Virtualisierungsprogramm. Wird in diesem Modul von vagrant verwendet um virtuelle Maschinen zu erstellen.