## Introduction

* Momentan keine Möglichkeit Routen visuell ansprechend automatisch zu berechnen und ästhetisch darzustellen
* Die derzeitigen Kartenanbieter haben keine Daten für eine Routenführung auf dem Wasser
* Routen verlaufen momentan über Land oder sind nur als Pins zu sehen
* Algorithmus soll dieses Problem lösen und für Ship Cruising Portal (Zielgruppe beschreiben) routen in einer Interaktiven Karte darstellen

## Problems

Testing if a pixel is black (water) or white (land). First problem is that the accuracy of this hit testing is only as good as the resolution image of the image I test against. For ports close to each other, this is fine for ports further away, the accuracy suffers.

## Possible improvements:

#### Adding quad-tree preprocessing to the map befor starting a*search

Sources: 
http://www.mikechambers.com/blog/2011/03/21/javascript-quadtree-implementation/
http://www.redblobgames.com/pathfinding/grids/algorithms.html
https://www.youtube.com/watch?v=95aHGzzNCY8

#### Using better A* heuristics

https://www.microsoft.com/en-us/research/wp-content/uploads/2004/07/tr-2004-24.pdf
symmetry breaking: http://aigamedev.com/open/tutorial/symmetry-in-pathfinding/#4
Jump Point Search: http://users.cecs.anu.edu.au/~dharabor/data/papers/harabor-grastien-aaai11.pdf

#### Different Search algorithm?

https://github.com/mikolalysenko/l1-path-finder (Doesn't support weighted edges)

#### Better coastline data

https://www.ngdc.noaa.gov/mgg/shorelines/gshhs.html
http://openstreetmapdata.com/data/coast