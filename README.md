Deze handleiding dient als hulpmiddel voor mensen die met dit project verder willen gaan. Momenteel is deze applicatie een aanpassing van de demo applicatie van Posenet zelf. Wij hebben deze applicatie uitgebreid met een pagina waarin camera beelden opgeslagen en gedownload kunnen worden, en een pagina waarin onze Visual Inspection Tool te vinden is. Voordat deze tool gebruikt kan worden moeten er een aantal stappen genomen worden zodat de applicatie werkt. 
 
Setup Navigeer naar de folder van de applicatie in de Command Line Interface. cd posenet/demos installeer de dependencies. Yarn Om de applicatie dan te starten doe je: Yarn Watch 
 
Lokale ontwikkeling  Voor de ontwikkeling van posenet zelf dient je de volgende stappen te nemen. cd posenet installeer de dependencies yarn publish posenet lokaal. Yarn build && yarn yalc publish Ga naar de demo en installeer de dependencies cd demos yarn Link de lokale posenet met de demo. yarn yalc link @tensorflow-models/posenet Start de dev demo server yarn watch 
 
  
Onderzoeksopzet | Versie 0.1 2 september 2019    
 
93 
Casusgroep GMB 
PowerBI koppeling Binnen de Visual Inspection Tool zitten een aantal API-calls. De eerste om de bearer key op te halen, de andere om de slide uit Power BI op te halen. Indien dit project verder uitgewerkt wordt zullen deze API-calls aangepast moeten worden. In de map Demos/VisualTool bevindt zich het bestand index.html. Hierin moeten de login settings voor de Power Bi login aangepast worden naar werkende credentials. Wij hebben deze gegevens eruit gehaald op dat deze momenteel privé inlog gegevens zijn van een van de deelnemers van deze casus.  Daarnaast moet de URL van de PowerBI aangepast worden, aangezien deze momenteel gelinkt is naar het PowerBI dashboard dat gelinkt in aan het privé account. 
 
→ De bearer code van powerBI dient aangepast te worden op regel 202, binnen index.html in de oorspronkelijke staat. → De inloggegevens van powerBI dient aangepast te worden op regel 223 en 224. 
 
Functionaliteit uitleg Hoofdscherm 
 
Camera recorder 
 
Dit is een prototype waarin het mogelijk is om webcam te zien, op te slaan en te downloaden vanuit een javascript. De knop ‘START RECORDING’ zal de opname starten en de knop ‘STOP RECORDING’ zal de opname stoppen. Wanneer er op ‘STOP RECORDING’ wordt geduwd, zal de tweede video gelinkt worden met het opgenomen bestand. Vervolgens zal er een link onder de video’s komen te staan waarmee de opname te downloaden is. 
Onderzoeksopzet | Versie 0.1 2 september 2019    
 
94 
Casusgroep GMB 
Visual Inspection Tool 
 
Deze tool maakt gebruik van een zip-bestand waarin bepaalde bestanden zijn opgeslagen. Deze zip dient een video  te bevatten en een of meer Json bestanden. Momenteel ondersteunt deze tool alleen Json bestanden die afkomstig zijn van een Myo armband of van de Microsoft Kinect.  
 
Zodra het zip-bestand ingeladen is kunnen er in de tabel ‘Attribute list’ een of meer keypoints  geselecteerd worden die vergeleken dienen te worden. Deze keypoints worden vervolgens in de tabel ernaast geplot. Deze worden tevens gesynchroniseerd met de video.  
 
Er kan gewerkt worden met annotaties en tijdsintervallen. Daarnaast kunnen er opmerkingen gekoppeld worden aan bepaalde selecties van tijd, deze kunnen dan worden opgeslagen en op een later moment worden bekeken. 
