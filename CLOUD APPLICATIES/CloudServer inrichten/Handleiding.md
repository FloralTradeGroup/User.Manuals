# CloudServer inrichten

Dit document beschrijft het inrichten/instellen van de API/CloudServer t.b.v. cloud applicaties

## Inhoudsopgave

[Inrichten CloudServer](#inrichten-cloudserver)  

## Inrichten CloudServer

|Stap|Uitleg|
|:-:|:--|
|**1**|Open Internet Information Services (IIS) en klik op de **Add Application Pool** knop rechts bovenin. Vul de naam in van de cloud applicatie en klik op OK.<details><summary><b>Klik voor voorbeeld</b></summary><img src=".Handleiding/image.png" height="400px"></details>|
|**2**|De Application Pool is aangemaakt.<details><summary><b>Klik voor voorbeeld</b></summary><img src=".Handleiding/image1.png" height="400px"></details>|
|**3**|We gaan nu de **Advanced Settings** van de Application Pool wijzigen.<br>Wijzig Start Mode > AlwaysRunning.[1]<br>Wijzig Identity > FTGBV/{USER}[2]<br>Wijzig Disable Overlapped Recycle > True.[3]<br>Wijzig Specific Times > Value 02:00:00.[4]</br><details><summary><b>Klik voor voorbeeld</b></summary><img src=".Handleiding/image2.png" height="400px"></details>|
|**4**|We gaan nu de website aanmaken.<br>Geef de website een naam.[1]<br>Selecteer de Application Pool die we in STAP 2 hebben aangemaakt.[2]<br>Geef het pad aan waar de instantie staat. (Je kan een instantie kopieren, pas de FS-INTRO.dbf aan)[3]<br>Binding instellen op https.[4]<br>Host name invullen met de gewenste 'vriendelijke' URL. Een binding kan je aanvragen bij Arjan van Rijn.[5]<br>Koppel vervolgens een certificaat.[6]</br><details><summary><b>Klik hier voor voorbeeld</b></summary><img src=".Handleiding/image3.png" height="400px"></details>|
|**5**|Zorg ervoor dat de CloudServerMap bekend is in Florisoft. Deze kan je toevoegen via de systeeminstellingen.<details><summary><b>Klik hier voor voorbeeld</b></summary><img src=".Handleiding/image4.png" height="400px"></details>|
|**6**|De Instance directory moet ge-shared worden zodat de map te benaderen is vanaf de server waarop Florisoft actief is. Geef de gebruiker je gekoppeld heb bij de Application Pool de Read/Write rechten.<details><summary><b>Klik hier voor voorbeeld</b></summary><img src=".Handleiding/image5.png" height="400px"></details>|
|**7**|Als je de stappen goed heb doorlopen en je de URL opvraagt via je browser moet je dit scherm krijgen<details><summary><b>Klik hier voor voorbeeld</b></summary><img src=".Handleiding/image6.png" height="400px"></details>|
