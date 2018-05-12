---
layout: post
title:  "Installasjon av anaconda for MacOS"
date:   2018-05-11 10:25:43 +0200
categories: anaconda python
---

## Last ned anaconda distribusjonen fra 
Last ned anaconda fra [Anaconda][anaconda] sitt nettsted. (![Download]({{ "/assets/img/download_button.png" | absolute_url }})-knapp øverst i høyre hjørne)
Vanligvis vil nettstedet se hvilket operativsystem du har. Dersom den ikke gjør det velger du manuelt mellom MacOS, Windows eller Linux. 

{% include figure.html file="/assets/img/download_site_small.jpg" caption="Nedlastingssiden til Anaconda" %}

Velg Python 3.6-versjonen. Før nedlasting kan det hende du blir bedt om å registrere deg, da er det bare å klikke på 
{% include button.html button_name="No Thanks" button_class="btn-outline-secondary btn-sm" %}. 

## Installer anaconda
Knapper å trykke riktig på underveis. Dette er en vanlig installer, men den trenger noe tilgang til datamaskinen. Dersom installeren ber om administratorrettigheter: ta kontakt med lokal IT-support, som vanlig ved installasjon av programmer. Dersom du har nødvendige tilganger, skal du se følgende bilder underveis i prosessen: 

{% include carousel.html 
id="myCarousel" 
images="
/assets/img/installer1_annotated.png, 
/assets/img/installer2_annotated.png,
/assets/img/installer3_annotated.png,
/assets/img/installer4_annotated.png" 
%}

## Åpne anaconda
Når Anaconda en installert skal den finnes i Applications-mappen som `Anaconda-Navigator`. Åpne `Anaconda-Navigator` og velg `spyder` fra menyen. Det er flere av alternativene som kan være interessante å vurdere å bruke i undervisningen, men i kurset vil vi bruke `spyder`. 

{% include figure.html file="/assets/img/anaconda-navigator_annotated.png" caption="Her velger man hvilken måte man vil bruke Anaconda. Vi kommer til å bruke <i>Spyder</i>" %}

Når man åpner spyder for første gang kan det hende det dukker opp en beskjed om at spyder ikke er oppdatert. Denne kan ignoreres foreløpig. 

{% include figure.html width="w-75" file="/assets/img/incoming_connections.png" caption="Python vil ha lov til å bli kontaktet fra internett. For våre formål kan man fint velge å blokkere denne forespørselen." %}

{% include figure.html width="w-50" file="/assets/img/update_spyder.png" caption="Spyder kan være utdatert. Foreløpig samma det." %}

## Sjekk at anaconda-installasjonen fungerer som den skal 
I det følgende vil `>>` brukes som *python-prompt*, altså at man gir en instruksjon til python-interpreteren på maskinen. Dette svarer til det stedet i anaconda der man kan skrive inn kommandoer direkte (se bilde). 

Den første sjekken er `>> print("Hello, World!")` (trykk enter for å kjøre kommandoen)

{% include figure.html file="/assets/img/spyder-window.png" caption="Spyder. Til venstre er en kode-editor, nede til høre er det en IPython-konsoll" %}

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

{% include figure.html width="w-50" file="/assets/img/first_run.png" caption="Anbefalte innstillinger er slik som på dette bildet." %}


Dersom alt har gått bra skal du nå få opp en figure som viser $math$x^2$/math$-funksjonen. Dersom dette ikke fungerer bør du ha fått opp en feilmelding.  

Dersom man skulle få behov for å installere moduler som mangler, gjør man det i "Environments" (Men det er lite trolig at det blir nødvendig). 

{% include figure.html width="w-75" file="/assets/img/install_packages.png" caption="Pakke-installasjon. Bruk søkefeltet oppe til høyre for å søke opp pakker." %}

### Innstillinger i Anaconda
Det er mange innstillinger i Anaconda, og mange ting er smak og behag. For at alle skal ha samme oppsett når vi er på kurs, slik at vi unngår unødig feilsøking, har vi følgende forslag til innstillinger: 

Sett "Remove all variables before execution", fordi det sørger for at samme script git samme resultat hver gang. Om man velger å beholde variable kan man i enkelte tilfeller få svært uventet oppførsel. For at dette skal bli standard oppfølsel må man også ordne dett under "Preferences".

{% include figure.html width="w-75" file="/assets/img/run_settings.png" caption="Kjøreinnstillinger" %}

Man kan velge om man vil at figurer skal dukke opp *inline*, altså sammen med programoutput, eller om man vil at de skal dukke opp i egne vindier. I det siste tilfellet har man anledning til å interagere med figurene (zoom, pan etc.). Dette er en instilling man kan variere etter behov. Noen ganger lager man mange figurer som er ferdig laget -- da er *inline* mest effektivt. Andre ganger skal man studere figurer mer nøye, og trenger å interagere. Alternativet man bruker da er (selv om navnet ikke avslører oppførselen) *Automatic*.

{% include figure.html width="w-75" file="/assets/img/graphics_setting.png" caption="Innstillinger for IPython-konsollen" %}

La anaconda slette variable mellom kjøringer. Dette hindrer masse uventet oppførsel.



[anaconda]: https://www.anaconda.com/
