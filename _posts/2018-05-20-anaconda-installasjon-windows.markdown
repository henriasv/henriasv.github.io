---
layout: post
title:  "Installasjon av Anaconda for Windows"
date:   2018-05-11 10:25:43 +0200
categories: anaconda python
---

## Last ned Anaconda 
Last ned Anaconda fra [Anaconda][anaconda] sitt nettsted. ![Download]({{ "/assets/img/download_button.png" | absolute_url }})-knapp finnes øverst i høyre hjørne. Etter å ha klikket på denne lander man på en side med flere nedlastingsvalg. 
Vanligvis vil nettstedet se hvilket operativsystem du har. Dersom den ikke gjør det velger du manuelt mellom MacOS, Windows eller Linux. 

{% include carousel.html 
id="downloadCarousel"
images="
/assets/img/windows/anaconda_page.png,
/assets/img/windows/anaconda_download.png,
/assets/img/windows/anaconda_download_2.png
" %}

Velg Python 3.6-versjonen. Før nedlasting kan det hende du blir bedt om å registrere deg, da er det bare å klikke på 
{% include button.html button_name="No Thanks" button_class="btn-outline-secondary btn-sm" %}. 

## Installer anaconda
Knapper å trykke riktig på underveis. Velg å kun insallere for din egen bruker om det er på egen maskin og du ikke har administratorrettigheter. Dersom installeren allikevel ber om administratorrettigheter: ta kontakt med lokal IT-support, som vanlig ved installasjon av programmer. Dersom du har nødvendige tilganger, skal du se følgende bilder underveis i prosessen: 

{% include carousel.html 
id="myCarousel" 
images="
/assets/img/windows/installation_1.png, 
/assets/img/windows/installation_2.png,
/assets/img/windows/installation_3.png,
/assets/img/windows/installation_4.png,
/assets/img/windows/installation_5.png,
/assets/img/windows/installation_6.png,
/assets/img/windows/installation_7.png,
/assets/img/windows/installation_8.png,
/assets/img/windows/installation_9.png" 
%}

Selve installasjonssteget der man ser en progressbar tar noen minutter, for eksempel 10. 

## Åpne Spyder
Anaconda er en stor pakke som inneholder mye forskjellig. Det viktigste den inneholder er et svært godt utvalg av Python-pakker. Anaconda tilbyr flere forskjellige innganger til å bruke disse pakkene. Vi skal bruke *Spyder*.

Vi skal åpne `Spyder` gjennom `Anaconda-Navigator`. Når vi åpner Anaconda-Navigator (på samme måte som ethert annet program på datamaskinen) kan vi velge mellom flere alternativer under `Home`: jupyterlab, notebook, qtconsole, spyder, glueviz etc. Vi skal bruke `Spyder`, og klikker derfor på {% include button.html button_name="Launch" button_class="btn-outline-primary btn-small" %}-knappen i boksen til nettop `Spyder`. 

{% include carousel.html 
id="anacondaCarousel"
images="
/assets/img/windows/open_anaconda_nav.png,
/assets/img/windows/open_spyder.png"
%}
Over vises hvordan du åpner Anaconda og deretter åpner *Spyder*. 

Når man åpner spyder for første gang kan det hende det dukker opp en beskjed om at spyder ikke er oppdatert. Denne kan ignoreres foreløpig, men det er også trygt å la spyder oppdatere seg. 

## Sjekk at anaconda-installasjonen fungerer som den skal 
I det følgende vil `>>` brukes som *python-prompt*, altså at man gir en instruksjon til python-interpreteren på maskinen. Dette svarer til det stedet i anaconda der man kan skrive inn kommandoer direkte (se bilde). 

Den første sjekken er `>> print("Hello, World!")` (trykk enter for å kjøre kommandoen)

{% include figure.html file="/assets/img/windows/spyder_1.png" caption="Spyder. Til venstre er en kode-editor, nede til høre er det en IPython-konsoll" %}

Dersom dette har gått bra printes `Hello, World!` i terminalen. 


### Er anaconda installert med nødvendige pakker?
Kopier innholdet i kodesnutten under, og legg det inn i et nytt script i anaconda. Kjør deretter scriptet ved å trykke på den grønne play-knappen, eller med tastekombinasjonen ..

{% highlight python %}
from pylab import *
t = linspace(0, 3, 100)
A = t**2
plot(t, A)
xlabel("tid")
ylabel("amplitude")
{% endhighlight %}

Første gang en fil kjøres kommer følgende vindu opp: 

{% include figure.html width="w-100" file="/assets/img/windows/spyder_3.png" caption="Anbefalte innstillinger er slik som på dette bildet." %}


Dersom alt har gått bra skal du nå få opp en figur som viser $$A = t^2$$. Dersom dette ikke fungerer bør du ha fått opp en feilmelding.  

Dersom man skulle få behov for å installere moduler som mangler, gjør man det i "Environments" (Men det er lite trolig at det blir nødvendig). 

### Innstillinger i Anaconda
Det er mange innstillinger i Anaconda, og mange ting er smak og behag. For at alle skal ha samme oppsett når vi er på kurs, slik at vi unngår unødig feilsøking, har vi følgende forslag til innstillinger: 

Sett "Remove all variables before execution", fordi det sørger for at samme script git samme resultat hver gang. Om man velger å beholde variable kan man i enkelte tilfeller få svært uventet oppførsel. For at dette skal bli standard oppfølsel må man også ordne dett under "Preferences".

{% include figure.html width="w-100" file="/assets/img/windows/spyder_settings_1.png" caption="Kjøreinnstillinger" %}

Man kan velge om man vil at figurer skal dukke opp *inline*, altså sammen med programoutput, eller om man vil at de skal dukke opp i egne vindier. I det siste tilfellet har man anledning til å interagere med figurene (zoom, pan etc.). Dette er en instilling man kan variere etter behov. Noen ganger lager man mange figurer som er ferdig laget -- da er *inline* mest effektivt. Andre ganger skal man studere figurer mer nøye, og trenger å interagere. Alternativet man bruker da er (selv om navnet ikke avslører oppførselen) *Automatic*.

{% include figure.html width="w-100" file="/assets/img/windows/spyder_settings_2.png" caption="Innstillinger for IPython-konsollen" %}

Etter å ha valgt *Automatic* kan du sjekke at alt er i orden. Figuren skal nå komme opp i et eget vindu. Det kan hende du må restarte Spyder for at endringen skal tre i kraft. 

{% include figure.html width="w-100" file="/assets/img/windows/plot_separate_window.png" caption="Når du plotter med automatioc skal det se omtrent slik ut, altså at plottet dukker opp foran Spyder-vinduet." %}

### Det var det hele
Vi sees på kurs. 

[anaconda]: https://www.anaconda.com/
