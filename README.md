# Ordinanze COVID Regione Siciliana
[![Frictionless](https://github.com/opendatasicilia/ordinanze-covid/actions/workflows/frictionless.yaml/badge.svg)](https://repository.frictionlessdata.io/report?user=opendatasicilia&repo=ordinanze-covid&flow=frictionless) [![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/) <a href="https://www.datibenecomune.it/"><img src="https://img.shields.io/badge/%F0%9F%99%8F-%23datiBeneComune-%23cc3232"/></a> 

A partire dal 21 dicembre 2020, la Presidenza della Regione Siciliana emette **ordinanze** in **PDF** (_Ulteriori misure per l'emergenza epidemiologica da Covid-19_) con le quali vengono imposte restrizioni ai **comuni siciliani** e istituite le `zone` `rosse`, `arancioni`, `gialle` al fine di fronteggiare la pandemia.

Tali file, spesso frutto di scansione, sono raccolti nel [sito ufficiale](https://www.regione.sicilia.it/) nella sezione "[Servizi informativi](https://www.regione.sicilia.it/istituzioni/servizi-informativi/decreti-e-direttive?f%5B0%5D=category%3A26)” e non si prestano né ad **analisi** né ad una facile lettura (soprattutto se sono immagini); abbiamo pensato di raccogliere tutte le ordinanze in un [foglio elettronico](https://docs.google.com/spreadsheets/d/1qHGoC3qEkH6jyANNwsIkqnuLZk_gcaV5bSX4COphyYs/edit?usp=sharing) (che alimenta i dati di questo repository) e rilasciare queste informazioni in **formato open**.

Dati estratti da [Totò Fiandaca](https://twitter.com/totofiandaca)

⚠️ Se vuoi rimanere aggiornato, iscriviti al [feed RSS del ChangeLog](https://github.com/opendatasicilia/ordinanze-covid/commits/main/CHANGELOG.md.atom)

## Schema dati

Comuni siciliani in Zona Rossa, Arancione, Gialla

- Directory: `root`
- File: [`data.csv`](https://github.com/opendatasicilia/ordinanze-covid/blob/main/data.csv)
- Encoding: `UTF-8`
- Separatore di campo: `,`
- metadati: [`datapackage.yaml`](https://github.com/opendatasicilia/ordinanze-covid/blob/main/datapackage.yaml)

Campo | Descrizione | Formato | Esempio
-- | -- | -- | --
pro_com | Codice numerico del Comune ISTAT (2021) | Numero | 87015
comune | Denominazione del Comune | Testo | Catania
zona | Tipologia di restrizioni applicate | Testo | rossa
data_inizio | Data di inizio delle restrizioni | YYYY-MM-DD | 2021-05-12
data_fine | Data di fine delle restrizioni | YYYY-MM-DD | 2021-05-12
id_ordinanza | Codice identificativo dell'ordinanza. Indica il numero e la data dell'ordinanza nel formato DDMMYYYY| Testo | 01-03012021
nro_ordinanza | Numero dell'ordinanza della Presidenza della Regione Siciliana | Numero | 1
data_ordinanza | Data dell'ordinanza della Presidenza della Regione Siciliana | YYYY-MM-DD | 2021-05-12
PDF | Accessibilità dei file PDF | Testo | Immagine
nro_pgg | Numero di pagine dell'ordinanza | Numero | 6
link_ordinanza | URL ordinanza della Presidenza della Regione Siciliana | Testo | https://www.google.it
note | Eventuali annotazioni | Testo | Lorem ipsum

Note <br>
- L'aggiornamento dei dati è gestito da [questa action](https://github.com/opendatasicilia/ordinanze-covid/blob/main/.github/workflows/update.yml) che viene eseguita automaticamente una volta al giorno; tuttavia è possibile "forzare" l'aggiornamento molto semplicemente ogni volta che si aggiorna lo sheet. Basta fare click su `Actions` > `Update data` > `Run workflow` > `Run workflow`

## Link utili
- [Blogpost (IT)](https://opendatasicilia.it/2021/04/10/covid-19-e-i-comuni-siciliani-in-zona-rossa-anno-2021/) di [Totò Fiandaca](https://twitter.com/totofiandaca)
- [Blogpost (EN)](https://opendatasicilia.it/2021/04/22/red-zones-in-sicily-a-story-of-civic-hacking/) translated by [Paola Masuzzo](https://twitter.com/pcmasuzzo)
- [Google Sheet](https://docs.google.com/spreadsheets/d/1qHGoC3qEkH6jyANNwsIkqnuLZk_gcaV5bSX4COphyYs/edit?usp=sharing) di [Totò Fiandaca](https://twitter.com/totofiandaca)

## Elaborazioni
Dati aperti di questo tipo consentono la realizzazione di svariate elaborazioni:
- [Mappa](https://opendatasicilia.github.io/OpenDataSicilia-per-il-Coronavirus/elaborazioni/ods/) di [Giovan Battista Vitrano](https://twitter.com/gbvitrano)
- [Dashboard](https://opendatasicilia.github.io/OpenDataSicilia-per-il-Coronavirus/vaccini/sit_vaccini_zone/) di [Giovan Battista Vitrano](https://twitter.com/gbvitrano)
- [Timeline](https://gabacode.github.io/zone-rosse-timeline/) di [Gabriele Scalici](https://twitter.com/GabArcangelo)

![image](https://user-images.githubusercontent.com/77018886/148086816-0eadbf00-0aa6-4618-bc58-4534ca5b11e0.png)
_Screenshot al 2022-01-04_

👉 Se vuoi includere questa mappa dinamica e interattiva sul tuo sito, copia il codice sottostante

```
<iframe title="2022 | Comuni siciliani attualmente in zona rossa/arancione/gialla" aria-label="Mappa" id="datawrapper-chart-KcM9c" src="https://datawrapper.dwcdn.net/KcM9c/30/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1767"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}(); </script>
```
## Dicono di noi

Data | Testata e Articolo
-- | -- 
2021-04-13 | [PalermoToday](https://www.palermotoday.it/cronaca/coronavirus-bollettino-contagi-palermo-sicilia-13-aprile-2021.html)
2021-04-14 | [FocuSicilia ](https://focusicilia.it/caos-covid-mancano-gli-open-data-chiesti-da-un-anno-nessuna-risposta/)
2021-04-15 | [24live di Barcellona P.G.](https://24live.it/2021/04/15/la-mappa-dei-comuni-siciliani-in-zona-rossa-aggiornata-con-opendatasicilia/)

## Licenza
<a href="https://creativecommons.org/licenses/by/4.0/"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/CC-BY_icon.svg/640px-CC-BY_icon.svg.png" width="150"/></a>
