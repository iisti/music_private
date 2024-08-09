# Music repository

A repository for saving music related stuff.

* Äänitys Leon ja Jorin kanssa

  ~~~text
  oma loopback "thru mute"
  
  äänitys: DI rec päälle
  ~~~

* Lataa youtube-biisejä <https://en.loader.to/>


## Kitaralle

1. Asenna pluginit:
    STL Tones Ignite Emissary Bundle
        Sisältää STL Tones Ignite NadIR
        C:\Program Files\Steinberg\VSTPlugins
        C:\Program Files (x86)\Steinberg\VSTPlugins
    Stillwell Audio, Vibe EQ
        C:\Program Files\Steinberg\VSTPlugins
        C:\Program Files (x86)\Steinberg\VSTPlugins

1. Konfiguroi imainen-kitaramallinnus
    1. Pura zip ja kopioi metal-chain.RfxChain kansioon
        ~~~
        %userprofile%\AppData\Roaming\REAPER\FXChains
        ~~~
    1. Raita -> FX -> FX Chains -> Chain: metal-chain
    1. Valitse Ignite - NadIR (STL Tones)
        1. Avaa IR File: 0-G12... 
        1. Avaa IR File: 1on-preshigh.wav

## Bassolle

~~~text
SHB-1
https://www.igniteamps.com/#shb-1
    C:\Program Files\VSTPlugins
~~~

## Laululle

~~~text
Stillwell Audio Rocket Character Compressor
    Vocal in yer face
W1 Limiter http://www.yohng.com/software/w1limit.html
    Kopioi George Yohng's W1 Limiter x64.dll kansioon C:\Program Files\VSTPlugins
~~~

## Reaper

### Tempo kohilleen
https://www.youtube.com/watch?v=PlGnzK7GiSU

### Lisää isku tahtiin

* Shift + C, ja sitten tahtilaji kohdilleen.

### Pikanäppäinyhdistelmät

<https://user.cockos.com/~glazfolk/ReaperKeyboardShortcuts.pdf>

#### Vaihda snap gridin tarkkuus

* Alt + S = snap grid päälle pois
* Snap gridin tarkkuuden voi vaihtaa klikkaamalla oikealla hiiren painikkeella magneetti-ikonia vasemmalla ylhäällä (metronomin lähellä).

#### Monta äänityskierrosta, valitse paras

* Ctrl+Shift+T, poista
* Alt+Shift+T, valitse paras äänitys

#### Voimakkuuden säätö keskellä raitaa

* v = Volume Envelope
* shift+click = insert point
* ctrl+shift kahden pisteen välillä = säädä voimakkuutta vain sillä välilä

## Ohjeita äänitykseen

### Recording 1 acoustic guitar

* Record Guitar Like A PRO (& revealing my BIG secret!) "by Paul Davids" <https://www.youtube.com/watch?v=ww-cH29IGeM>

    ~~~text 
    Recording acoustic guitar:
        2 mics in a "triangle" with the guitar
            
            1 mic  <-distance x3->  2 mic
             \                      /
              \                    / <- distance x1
               \                  /
            12th fret, guitar, bridge
            
            - 1st mic is pointing to 12th fret of the guitar.
            - 2nd mic is pointing to the bridge of the guitar.
            - To avoid phase issues:
                - Distance of the mics should be the same from the guitar.
                - Distance between the mics should be 3 times as far of each other as from the guitar.x
    ~~~
                
    ~~~text    
    DAW (Digital Audio Workstation)
        -EQ
            Q = how widely the eq affects the spectrum
        
            Cut low frequencies away
                Highpass with 50Hz
            Bring up clarity
                Boost Clarity
                    2.5k - 4kHz
                Boost High shelf (can be annoying):
                    10kHz - 12kHz < (meaning boost everything over 10kHz)
                In the video these were boosted:
                    3.3kHz, Gain +3.7 dB, Q 0.7
                    11kHz < , Gain +2.4 dB, Q 0   
            Remove boxiness (make a cup from your hands and cover your mouth and talk, that sound is boxiness)
                200Hz - 500Hz, -1dB, Q 4.1
        -Compressor (same compressor for both mics)
            threshold
                Aim for -5/-7 gain reduction, when playing live
                In example -1/-2 gain reduction when in quiet section
            ratio
                2-4
            attack
                slow (keeps initial punch)
            release
                fast (release fast, so that the it doesn't get breathy/bumpy sound of compressor)
        -Pan
            Neck hard left (all sound on left)
            Bridge hard right
        -Reverb
            Return track / bus
                In example 15dB and 2.19 seconds
                Tip reverb should be short in fast song and longer in slower song.
            
            2 tracks
                Reverb left
                Reberb right
                
                Send left/neck into right with predelay
                Send right/bridge into left with predelay
        -Compressor to bus of tracks
    ~~~

### Mixing Acoustic Guitars in REAPER

<https://www.youtube.com/watch?v=yDQQSs7tikE>

* Monta raitaa voi EQuttaa samalla tekemällä "kansion", eli raidan, jonka aliraitoja muut raidat on. Aliraidaksi saa tehtyä klikkaamalla raidan vasemmalta puolelta alhaalta (nauhoitus nappulan vieressä).

~~~text
VST: ReaEQ (Cockos)
    High Pass, 50Hz, Bandwidth 1.70 määrää, ettei korkeat taajuudet korostu.
~~~

### Mixing Bass Guitar in REAPER

<https://www.youtube.com/watch?v=ghEMSKgqjQo>

~~~
Chain: 
VST: ReaCOmp (Cockos)
VST: ReaEQ (Cockos)
VST: SHB-1
~~~       

### Leon vinkit joulubiisiin

* Soundit oikeen hyvät ja terveen kuuloiset. Kitaroiden panorointi ja stereofiilis on ihan hyvä, ei se musta tartte olla tän kummempi kun elementit on aika simppelit
* bassoon kompressoria, myös kitaroihin. Bassoon vois kokeilla jotain basso amp mallinnusta että se ei kuuloistais ihan DI:ltä
* kitaroihin “send efektinä” kaikua. Valkkaa sellanen kaiku ettei ne yläpäät “sihise”. Voit myös leikata kaiun yläpäitä eq:lla pois. Laita sitä kaikua van sen verran että tulee kiva tilan tuntu, ettei mee puuroksi. Kaiun pituus on hyvä olla sellanen että se toimii suunnilleen biisin tempon kanssa, eli että jos biisi on nopea niin ei kande olla kauheen pitkää hallikaikua vaan sit mieluummin vähän nopeampi, lyhyempi.
* Jos haluat voit tähän tehdä vielä jotain perkussioita äänittämällä vaikka jalalla “basarin” tömistämällä ja sit nostat eq:lla bassotaajuuksia ja miksaat sen sinne sopivan hiljaa. Jotain hyvin hillittyä jos tonne haluu tehdä juttuja
* Mä aina ajattelen miksauksen (jos puhutaan et haluaa tehdä valmiin lopputuotteen) niin et “perusjutut kuntoon”, sit tilan tuntua ja sit jotain mielenkiintoista mikä saa kuulijan kiinnostumaan. Joskus oon lisäilly jotain pistemäisiä efektejä, joskus jotain metron ääntä tai puheensorinaa tms. 
* Tuleeks tähän vielä vokaalit?
* Tää kuulosti kyl ihan siltä ku se olis jo kompressoitu kokonaisuutena, laitoitko lopputuotteen W1:n läpi?
