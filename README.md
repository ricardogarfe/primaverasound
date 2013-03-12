# Primavera Sound 2013 Horarios
![Primavera Sound 2013](http://upload.wikimedia.org/wikipedia/en/7/7b/Primavera_Sound_10.jpg)
## Introduction

Retrieve Primavera Sound 2013 schedule from [Programación](http://www.primaverasound.es/programacion)

## Environment

Python 2.7.2

## License

This project has ``Apache License, Version 2.0`` see complete 
definition in **LICENSE** file.

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
$ python schedule.py
```

Or import module *Schedule* in your project and create the instance:
```python
primaveraSoundSchedule = Schedule()

import pprint
pprint.pprint(primaveraSoundSchedule.horarios)
```

Retrieve schedule results in dictionary list per day (there is no hour set yet for concerts):
```json
[{'horario': ['Lunes 20 de mayo',
              [{'Artista': 'Jupiter Lion',
                'Escenario': 'Sala Apolo',
                'Hora': ''},
               {'Artista': 'Spectrum',
                'Escenario': 'Sala Apolo',
                'Hora': ''}]]},
```

## Feel Free

Feel Free to do anything with this script ! I know it could be better :) and I'll improve it.

## Scraping Wiki

You can run this script in Scraping Wiki:

* https://scraperwiki.com/scrapers/primavera_sound_2013/

## License

<a href="http://creativecommons.org/licenses/by/3.0/" rel="Creative Commons Attribution 3.0">![Foo](http://i.creativecommons.org/l/by/3.0/88x31.png)</a>

This work by Ricardo Gracía Fernández - ricardogarfe [at] gmail [dot] com is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/).

