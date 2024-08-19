 Ich hatte dieses Problem auch, als ich versuchte, Pulse / Ivanti VPN zu installieren. Ich habe hier eine Lösung gefunden: https://github.com/bambulab/BambuStudio/issues/3973#issuecomment-2085476683

    Die Lösung ist wie folgt:   

    1.- Aktualisieren Sie die Quelldatei (sudo vim /etc/apt/sources.list.d/ubuntu.sources) und fügen Sie die folgenden Zeilen hinzu:

Types: deb
URIs: http://br.archive.ubuntu.com/ubuntu/
Suites: jammy noble-updates noble-backports
Components: main restricted universe multiverse
Signed-By: /usr/share/keyrings/ubuntu-archive-keyring.gpg

Types: deb
URIs: http://security.ubuntu.com/ubuntu/
Suites: jammy-security
Components: main restricted universe multiverse
Signed-By: /usr/share/keyrings/ubuntu-archive-keyring.gpg

    2.- Führen Sie sudo apt update aus

    3.- Installieren Sie Synaptic (sudo apt install synaptic) und öffnen Sie es.

    4.- Suchen Sie nach "libwebkit2gtk", aktivieren Sie das libwebkit2gtk-4.0-37 und wenden Sie es an.

    5. Profitieren Sie.   

    Danach sollte Ihre Installation reibungslos verlaufen.   


    2. Andere Lösung: 

https://github.com/tauri-apps/tauri/issues/966

3. libwebkit2gtk-4.0-37:
 Hängt ab von: libjavascriptcoregtk-4.0-18, aber es wird nicht installiert
 Hängt ab von: libicu70 (>=70.1-1~) but it is not installable

https://packetstormsecurity.com/files/178810/Ubuntu-Security-Notice-USN-6788-1.html

