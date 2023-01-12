# Qu'est ce que j'ai fait ?
J'ai installe node et fait un jupyter lab build pour que ce soit pris en compte et pouvoir
installer l'extension panel
Installer pip install pyviz-comms pour que panel marche avec Jupyterlab 3

Pas reussi a le faire marcher avec le urlpath...

# Test d'integration dans une app Django
Il y a un blem d'integration de bokeh a django, ce n'est plus trop maintenu cote bokeh et donc on a un
probleme auqnd on utilise django 4

Il faut modifier /home/vincent/.local/lib/python3.10/site-packages/bokeh/server/django/routing.py
```python
from django.urls import re_path as url
```
Ils sont censes faire un repo a part django-bokeh mais il n'existe pas...
Ils ont pris la decision il y a pas longtemps donc il devrait sortir dans les prochains jours le repo

Also line 41 de  site-packages/bokeh/server/django/apps.py
https://github.com/bokeh/bokeh/issues/11148
```python
    name = 'bokeh.server.django'
    label = 'bokeh_server_django'
```

# Test de pyscript
