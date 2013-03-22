# Primavera Sound 2013 Horarios
![Primavera Sound 2013](http://primaverasound.com/ps/images/320x310_psbcn.jpg)
## Introduction

Retrieve Primavera Sound 2013 schedule from [Programación](http://www.primaverasound.es/programacion)

## Environment

Python 2.7.2

## License

This project has ``Apache License, Version 2.0`` see complete definition in [LICENSE](https://raw.github.com/ricardogarfe/primaverasound/master/LICENSE) file.

## Install

Read install instructions in [INSTALL](https://github.com/ricardogarfe/primaverasound/blob/master/INSTALL.md) file to use as a command in your system.

* Install from PYPI.
* Install from Source.

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
from scraper.primaverasound.schedule import Schedule
import json

primaveraSoundSchedule = Schedule()

# Print results.
schedule_result = json.dumps(primaveraSoundSchedule.horarios, sort_keys=True, indent=4)
print schedule_result
```

Retrieve schedule results in dictionary list per day (there is no hour set yet for concerts):
```json
[
    {
        "horario": [
            "Lunes 20 de mayo", 
            [
                {
                    "Artista": "Jupiter Lion", 
                    "Escenario": "Sala Apolo", 
                    "Hora": "", 
                    "dia": "2013-5-20", 
                    "id": "143"
                }, 
                {
                    "Artista": "Spectrum", 
                    "Escenario": "Sala Apolo", 
                    "Hora": "", 
                    "dia": "2013-5-20", 
                    "id": "142"
                }
            ]
        ]
    }, 
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

