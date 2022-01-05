# Ordinanze COVID Regione Siciliana
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/) <a href="https://www.datibenecomune.it/"><img src="https://img.shields.io/badge/%F0%9F%99%8F-%23datiBeneComune-%23cc3232"/></a> 

A partire dal 21 dicembre 2020, la Presidenza della Regione Siciliana emette ordinanze in PDF (_Ulteriori misure per l'emergenza epidemiologica da Covid-19_) con le quali vengono imposte restrizioni ai comuni siciliani (zone rosse, arancioni, gialle). Tali file, spesso frutto di scansione, sono raccolti nel [sito ufficiale](https://www.regione.sicilia.it/) nella sezione “SERVIZI INFORMATIVI | ORDINANZE COVID-19”.

I PDF non si prestano a una facile lettura, soprattutto se sono immagini (in questo caso non è nemmeno possibile effettuare ricerche), da parte di macchine e tantomeno da parte degli umani, in quanto si troverebbero davanti a centinaia di pagine; allora abbiamo pensato di raccogliere tutte le ordinanze in un foglio elettronico (che alimenta i dati di questo repository) e rilasciare queste informazioni in formato open.

Dati estratti da [Totò Fiandaca](https://twitter.com/totofiandaca)

## Schema dati

Comuni siciliani in Zona Rossa, Arancione, Gialla

- Directory: `root`
- File: `data.csv`
- Encoding: `UTF-8`
- Separatore di campo: `,`

Campo | Descrizione | Formato | Esempio
-- | -- | -- | --
pro_com | Codice ISTAT numerico del Comune | Numero | 87015
comune | Denominazione del Comune | Testo | Catania
zona | Tipologia di restrizioni applicate | Testo | rossa
data_inizio | Data di inizio delle restrizioni | YYYY-MM-DD | 2021-05-12
data_fine | Data di fine delle restrizioni | YYYY-MM-DD | 2021-05-12
id_ordinanza | Codice identifico dell'ordinanza. Indica il numero e la data dell'ordinanza nel formato DDMMYYYY| Testo | 01-03012021
nro_ordinanza | Numero dell'ordinanza della Presidenza della Regione Siciliana | Numero | 1
data_ordinanza | Data dell'ordinanza della Presidenza della Regione Siciliana | YYYY-MM-DD | 2021-05-12
PDF | Accessibilità dei file PDF | Testo | Immagine
nro_pgg | Numero di pagine dell'ordinanza | Numero | 6
link_ordinanza | URL ordinanza della Presidenza della Regione Siciliana | Testo | https://www.google.it
note | Eventuali annotazioni | Testo | Lorem ipsum
provincia | ⚠️ rimuoverei il campo (solo su GitHub) |  | 
proroga/cessa | ⚠️ rimuoverei il campo (solo su GitHub). È essenziale da pubblicare?| tbd | tbd
sovrapposizione | ⚠️ rimuoverei il campo (solo su GitHub). È essenziale da pubblicare?| tbd | tbd
cessa | ⚠️ rimuoverei il campo (solo su GitHub). È essenziale da pubblicare?| tbd | tbd
area_kmq | ⚠️ rimuoverei il campo (solo su GitHub) | tbd | tbd
pop_2020 | ⚠️ rimuoverei il campo (solo su GitHub) | tbd | tbd

Note: <br>
- tbd: to be determined
- Attualmente la frequenza di aggiornamento dei dati è settimanale ma si può "forzare" molto semplicemente ogni volta che si aggiorna lo sheet. Basta fare click su `Actions` > `Update data` > `Run workflow` > `Run workflow`

## Link utili
- [Blogpost (IT)](https://opendatasicilia.it/2021/04/10/covid-19-e-i-comuni-siciliani-in-zona-rossa-anno-2021/) di [Totò Fiandaca](https://twitter.com/totofiandaca)
- [Blogpost (EN)](https://opendatasicilia.it/2021/04/22/red-zones-in-sicily-a-story-of-civic-hacking/) translated by [Paola Masuzzo](https://twitter.com/pcmasuzzo)
- [Mappa](https://bl.ocks.org/gbvitrano/raw/664ac98fd51590d48290b70709a4ea48/) di [Giovan Battista Vitrano](https://twitter.com/gbvitrano)
- [Google Sheet](https://docs.google.com/spreadsheets/d/14f2AUf3k3jP60sPkUhzqhSIFlTEuUFCfac9b-1_29jc/edit#gid=1669181736) di [Totò Fiandaca](https://twitter.com/totofiandaca)

![image](https://user-images.githubusercontent.com/77018886/148086816-0eadbf00-0aa6-4618-bc58-4534ca5b11e0.png)
_Screenshot al 2022-01-04_

👉 Se vuoi includere questa mappa dinamica e interattiva sul tuo sito, copia il codice sottostante

```
<iframe title="2022 | Comuni siciliani attualmente in zona rossa/arancione/gialla" aria-label="Mappa" id="datawrapper-chart-KcM9c" src="https://datawrapper.dwcdn.net/KcM9c/30/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1767"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}(); </script>
```

## Licenza
<a href="https://creativecommons.org/licenses/by/4.0/"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/CC-BY_icon.svg/640px-CC-BY_icon.svg.png" width="150"/></a>
