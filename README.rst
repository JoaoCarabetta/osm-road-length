===============
OSM Road Length
===============

|Maintenance yes|
|PyPI version fury.io|
|PyPI download total|
|PyPI download month|

.. |PyPI version fury.io| image:: https://badge.fury.io/py/osm-road-length.svg
   :target: https://badge.fury.io/py/osm-road-length
.. |PyPI download month| image:: https://pepy.tech/badge/osm-road-length/month
   :target: https://pepy.tech/project/osm-road-length/month
.. |PyPI download total| image:: https://pepy.tech/badge/osm-road-length
   :target: https://pepy.tech/project/osm-road-length
.. |Maintenance yes| image:: https://img.shields.io/badge/Maintained%3F-yes-green.svg
   :target: https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity

DISCONTINUED
USE OSMPY
https://github.com/JoaoCarabetta/osmpy

A tool to get the highway length from Open Street Maps of a region using Python using Overpass Turbo API.

It supports any region size and shape. From cities to continents.

Installing
-----------
.. code:: bash

   pip install osm-road-length

Using
-----

.. code:: python        
        
        import osm_road_length
        from shapely import wkt

        geometry = wkt.loads('POLYGON((-43.2958811591311 -22.853167273541693,-43.30961406928735 -23.035275736044728,-43.115980036084224 -23.02010939749927,-43.157178766552974 -22.832917893834313,-43.2958811591311 -22.853167273541693))')

        length = osm_road_length.get(geometry)

Why not OSMnx?
--------------

OSMnx_ is a great package if you want to analyse the road infrastructure in depth. But, sometimes we just want simple numbers to do comparissons. This package does not load all road data to memory (imagine loading a whole country to your RAM). The package fetches the Overpass API directly. If the region is too large, it splits the region in a smart way to handle the Overpass API constrains. 

.. _OSMnx: https://github.com/gboeing/osmnx

Credits
-------

* Free software: MIT license

Function `katana` from snorfalorpagus_.

.. _snorfalorpagus: https://snorfalorpagus.net/blog/2016/03/13/splitting-large-polygons-for-faster-intersections/

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
    
