# MiniTidal Reference

Minitidal, refiriéndose al lenguaje Tidal Cycles es una lenguaje que te permite hacer patrones/secuencias musicales.

## Reproducir / Play

+ s "sonido"

## Samples

+ s "sonido:2"  -- accesa al sample no.2 del mismo banco, access to sample no.2 of the same bank

## Patterns / Partrones

+ s "sonido" -- toca 1 sonido en un ciclo, plays 1 sound in one cycle  
+ s "sonido sonido" -- toca 2 sonidos en un ciclo, plays 2 sounds in one cycle  
+ s "sonido sonido:2 sonido:3" -- toca 3 sonidos en un ciclo, plays 3 sounds in one cycle  
+ and so on... y así...

+ s "sonido:1 <sonido:2 sonido:3>"
-- primer ciclo: 1 y 2  
-- segundo ciclo: 1 y 3  
-- loop

+ s "sonido*5" -- 5 sonidos en in ciclo, 5 sounds in a cycle  

+ s "sonido:5 sonido:10*2 sonido:13"   
-- ciclo dividido en tres
-- doble sonido a la mitad del ciclo


## Transformar

+ s "sonido" # gain 0.2 -- modifica/modifies volumen 0++
+ s "sonido" # up (-0.5) -- modifica/modifies pitch, 0-- low/bajo, 0++ high/alto

+ s "sonido sonido:2 sonido:3" # gain (1 0.5 1.5)
-- patrones en transformaciones, cada sonido va a tener un volumen diferente
-- patters in transformation, each sound will have a different gain

## Video/Image functions

+ slow 2 $ s "sonido" # gain 0.2
-- slows the time, alentiza el tiempo    
-- normally/normálmente, 1c=1s  
