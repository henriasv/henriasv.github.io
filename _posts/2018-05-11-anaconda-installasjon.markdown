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
{% include button.html button_name="No Thanks" button_class="primary" %}. 

{% include carousel.html 
id="myCarousel" 
images="
/assets/img/installer1.png, 
/assets/img/installer2.png,
/assets/img/installer3.png,
/assets/img/installer4.png" 
%}

## Installer anaconda
Knapper å trykke riktig på underveis. Dette er en vanlig installer, men den trenger noe tilgang til datamaskinen. Dersom installeren ber om administratorrettigheter: ta kontakt med lokal IT-support, som vanlig ved installasjon av programmer. Dersom du har nødvendige tilganger, skal du se følgende bilder underveis i prosessen: 

## Åpne anaconda
Når Anaconda en installert skal den finnes i Applications-mappen som `Anaconda-Navigator`. Åpne `Anaconda-Navigator` og velg `spyder` fra menyen. Det er flere av alternativene som kan være interessante å vurdere å bruke i undervisningen, men i kurset vil vi bruke `spyder`. 

{% include figure.html file="/assets/img/anaconda-navigator.png" caption="Her velger man hvilken måte man vil bruke Anaconda." %}

Når man åpner spyder for første gang kan det hende det dukker opp en beskjed om at spyder ikke er oppdatert. Denne kan ignoreres foreløpig. 

{% include figure.html width="w-75" file="/assets/img/incoming_connections.png" caption="Python vil ha kontakt med internett" %}

{% include figure.html width="w-50" file="/assets/img/update_spyder.png" caption="Spyder kan være utdatert. Foreløpig samma det." %}

## Sjekk at anaconda-installasjonen fungerer som den skal 
I det følgende vil `>>` brukes som *python-prompt*, altså at man gir en instruksjon til python-interpreteren på maskinen. Dette svarer til det stedet i anaconda der man kan skrive inn kommandoer direkte (se bilde). 

Den første sjekken er `>> print("Hello, World!")` (trykk enter for å kjøre kommandoen)

{% include figure.html file="/assets/img/spyder-window.png" %}

Dersom dette har gått bra printes `Hello, World!` i terminalen. 


### Er anaconda installert med nødvendige pakker?
Kopier innholdet i kodesnutten under, og legg det inn i et nytt script i anaconda. Kjør deretter scriptet. 

{% highlight python %}
from pylab import *
print("Hello, World")
t = linspace(0, 3, 100)
A = x**2
plot(t, A)
xlabel("tid")
ylabel("amplitude")
show()
{% endhighlight %}

Dersom alt har gått bra skal du nå få opp en figure som viser $math$x^2$/math$-funksjonen. Dersom dette ikke fungerer bør du ha fått opp en feilmelding.  

### Innstillinger i Anaconda
Det er mange innstillinger i Anaconda, og mange ting er smak og behag. For at alle skal ha samme oppsett når vi er på kurs, slik at vi unngår unødig feilsøking, har vi følgende forslag til innstillinger: 

La anaconda slette variable mellom kjøringer. Dette hindrer masse uventet oppførsel.


[anaconda]: https://www.anaconda.com/
