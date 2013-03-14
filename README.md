# Primavera Sound 2013 Horarios
![Primavera Sound 2013](http://primaverasound.com/ps/images/320x310_psbcn.jpg)
## Introduction

Retrieve Primavera Sound 2013 schedule from [Programación](http://www.primaverasound.es/programacion)

## Environment

Python 2.7.2

## License

This project has ``Apache License, Version 2.0`` see complete definition in [LICENSE](https://raw.github.com/ricardogarfe/primaverasound/master/LICENSE) file.

## Install

### Developer requirements

Libraries required:

    * requests
    * lxml
    
Install using python dependency management [easy_install](http://peak.telecommunity.com/DevCenter/EasyInstall).
```shell
$ easy_install requests
$ easy_install lxml
```
## Command

run the script using:
```shell
$ python retrieve_schedule.py
```

Or import module *Schedule* in your project and create the instance:
```python
primaveraSoundSchedule = Schedule()

import pprint
pprint.pprint(primaveraSoundSchedule.horarios)
```

Retrieve schedule results in dictionary list per day (there is no hour set yet for concerts):
```json
{
    'horario': 
        ['S\xc3\x83\xc2\xa1bado 25 de mayo',
               {
                'Artista': 'Mount Eerie',
                'Escenario': 'Parc del F\xc3\xb2rum',
                'Hora': '',
                'dia': '2013-5-25',
                'id': '114'
               },
               {
                'Artista': 'My Bloody Valentine',
                'Escenario': 'Parc del F\xc3\xb2rum',
                'Hora': '',
                'dia': '2013-5-25',
                'id': '116'
               },
               {
                'Artista': 'Nick Cave & The Bad Seeds',
                'Escenario': 'Parc del F\xc3\xb2rum',
                'Hora': '',
                'dia': '2013-5-25',
                'id': '121'
               },
               {
                'Artista': 'Nils Frahm',
                'Escenario': 'Parc del F\xc3\xb2rum',
                'Hora': '',
                'dia': '2013-5-25',
                'id': '124'
               }
        ]
}
```

## Feel Free

Feel Free to do anything with this script ! I know it could be better :) and I'll improve it.

## Scraping Wiki

You can run this script in Scraping Wiki:

* https://scraperwiki.com/scrapers/primavera_sound_2013/

And collect data using ScrapperWiki SQL API in:

* https://scraperwiki.com/docs/api?name=primavera_sound_2013#sqlite

Create sql and use them from you want ! use the data !

```url
https://api.scraperwiki.com/api/1.0/datastore/sqlite?format=jsondict&name=primavera_sound_2013&query=select%20*%20from%20%60swdata%60%20limit%205
```

Retrieve and play with results in JSON:

```json
[
    {
        "Hora": "",
        "dia": "2013-5-20",
        "Artista": "Jupiter Lion",
        "Escenario": "Sala Apolo",
        "id": "143"
    },
    {
        "Hora": "",
        "dia": "2013-5-20",
        "Artista": "Spectrum",
        "Escenario": "Sala Apolo",
        "id": "142"
    },
    {
        "Hora": "",
        "dia": "2013-5-21",
        "Artista": "Bo Ningen",
        "Escenario": "Sala Apolo",
        "id": "145"
    },
    {
        "Hora": "",
        "dia": "2013-5-21",
        "Artista": "Foscor",
        "Escenario": "Sala Apolo",
        "id": "146"
    },
    {
        "Hora": "",
        "dia": "2013-5-21",
        "Artista": "Godflesh",
        "Escenario": "Sala Apolo",
        "id": "144"
    }
]
```
## License

<a href="http://creativecommons.org/licenses/by/3.0/" rel="Creative Commons Attribution 3.0">![Foo](http://i.creativecommons.org/l/by/3.0/88x31.png)</a>

This work by Ricardo Gracía Fernández - ricardogarfe [at] gmail [dot] com is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/).

