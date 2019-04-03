# Guglina TTS "IT"

Guglina TTS, edizione speciale: in italiano (guglinatts-it), è un sintetizzatore vocale originariamente progettato per il portoghese brasiliano. Utilizza l'API di sintesi vocale di Google Traduttore. Leggi gli screenshot per gli ipovedenti. Trasforma il testo in audio, consentendo a persone non vedenti o ipovedenti di accedere al contenuto visualizzato sullo schermo. Sebbene il pubblico di riferimento principale per i sistemi di conversione da testo a voce - come Guglina TTS EN - sia costituito da persone con disabilità visive, questo tipo di programma può essere utilizzato da persone con dislessia e altre disabilità di lettura, -collegare i bambini. Oltre ad essere uno strumento di tecnologia assistiva, i sintetizzatori vocali possono ancora avere applicazioni educative e di intrattenimento.
#

**Osservazione:** Il sintetizzatore GuglinaTTS utilizza Google Api, ma può essere utilizzato in modalità offline. Non preoccuparti per la tua connessione Internet.
#

È sotto l'egida della licenza:
### GPLv3
> Manutentore: Felipe Facundes
###### Site: https://brasiltts.wordpress.com/
###### Blog: https://brasiltts.blogspot.com/
###### E-Mail: felipe.facundes@gmail.com
###### Telegram: https://t.me/comandos_linux
#
### Installazione:

    git clone https://github.com/felipefacundes/guglinatts-it
    cd guglinatts-it
    
- **Esegui comando:**

```
chmod +x INSTALL.sh
yes s | sh INSTALL.sh
```

##### O manualmente:

``` 
sudo cp guglina*generic.conf /etc/speech-dispatcher/modules/
sudo cp speechd.conf /etc/speech-dispatcher/
sudo cp googletts* /bin/
sudo chmod +x /bin/googletts*
```

#
### Installazione di dipendenze:

- **Le dipendenze sono:**
  - espeak-ng
  - speech-dispatcher
  - orca
  - onboard
  - xsel 
  - libnotify 
  - python2-notify 
  - perl-libwww 
  - perl-www-mechanize 
  - perl-html-tree
  - ffmpeg
  - sox 
  - fmt 
  - lame 
  - perl-www-curl

#
- **Installazione di ArchLinux**

```
sudo pacman -S espeak-ng speech-dispatcher orca onboard ffmpeg xsel libnotify python2-notify perl-libwww perl-www-mechanize perl-html-tree sox fmt lame perl-www-curl
```

```
sudo pacman -U svox-pico-bin-1.0+git20130326-8-x86_64.pkg.tar.xz
```

#
- **Di Debian e derivati (Ubuntu...):**
  - Se non si dispone di pico2wave nel repository.
  - Dovresti prima convertire i pacchetti ".tar.xz" a ".deb"
  - Usa il comando alieno per convertire
  - Quindi basta installare con il comando dpkg
  - **Rinominare** i file ".pkg.tar.xz"
  - Per ".pkg.tar.gz"

```
fakeroot alien -d "nome".pkg.tar.gz
sudo dpkg -i *.deb
```

#### Fedora e derivati: l'alieno genera anche pacchetti ".rpm"
    fakeroot alien -r "nome".pkg.tar.gz

#
### Installazione di finitura

- Chiudi tutto e uccidi la sessione:

```
pkill -9 -u $USER
```

- Avvia X e digita il terminale

```
orca -s
```

- Sulla scheda: **"Voce"**.
- Configura in questo modo:
  - Sistema vocale: **Speech Dispatcher**
  - Sintetizzatore vocale: **guglina_it_tts**
  - Personaggio: **guglina_it_tts (it)**

#
### Se l'onboard e l'orca non si avviano insieme al sistema. Includi in ~/.xinitrc

``` 
onboard --not-show-in=GNOME,GNOME-Classic:GNOME --startup-delay=3.0 &
orca &
```     

- Or

``` 
cp /etc/xdg/autostart/onboard-autostart.desktop ~/.config/autostart/
cp /etc/xdg/autostart/orca-autostart.desktop ~/.config/autostart/
```

### È necessario abilitare Onboard e Orca, in modo che i programmi che dispongono della funzionalità di accessibilità, come OKULAR, possano funzionare correttamente. Assicurati di andare a bordo! ;) ###

<br></br>

###### Guglina è l'acronimo di: Google + Regina. Un omaggio al brasiliano: Regina Bittar, responsabile della voce di Google in Brasile.
#### Licenza: GPLv3 ####

<br></br>

```
┏┓
┃┃╱╲ In questa 
┃╱╱╲╲ casa
╱╱╭╮╲╲ tutti
▔▏┗┛▕▔ usano
╱▔▔▔▔▔▔▔▔▔▔╲
LINUX
╱╱┏┳┓╭╮┏┳┓ ╲╲
▔▏┗┻┛┃┃┗┻┛▕▔
--------------------------
```
