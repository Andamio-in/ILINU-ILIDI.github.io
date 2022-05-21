# Cinecer0 Reference

CineCer0 es un lenguaje para reproducir/transformar video, imagen y texto. A language to play/transform video, image, and text.

## Reproducir/Play

+ video "videoURL"   
+ image "imageURL"   
+ text "Este es un texto"   
+ "" --estado vacío, empty state  

## Posición/Position

+ setPosX [x] $   
+ setPosY [y] $   
+ setCoord [x] [y] $   

--Parametros, Parameters:    
--(-1) : izquierda/arriba left/top  
--  1  : derecha/abajo right/bottom  
--  0  : centro centre  

## Vol

vol 0.5 $ "myVideo.extension"  

--Parametros, Parameters: 0-1  

## Transformación/Transformation (Video/Image)

+ setSize [wh] $ --one parameter will affect both width and heigh proportionally, un parámetro que afecta alto y ancho proporcionalmente  
+ setRotate [d] $ --one parameter in degrees, un parámetro en grados  
+ setOpacity [o] $ -- 0 - 1 (no-opac)  
+ setBlur [bl] $ -- 0 = no blur (1++ = more/más)  
+ setBrightness [br] $ --  0-0.9 = less/menos, 1++ = more/más  
+ setContrast [c] $ -- 0-0.9 = less/menos, 1++ = more/más  
+ setGrayscale [g] $ -- 0 = no grayscale, 1 = full grayscale/escala de grises  
+ setSaturate [s] $ -- 1 = natural saturation (1++ = more/más, 1-- =less/menos)  

## Transformación/Transformation (Text)

+ size [n] $ -- 0++  
+ rgb [r] [g] [b] $ -- 0-1  
+ rgb' [r] [g] [b] [a] $ -- 0-1, alpha
+ strike $   
+ bold $  
+ italic $  

## Dinamic parameters, parámetros dinámicos

+ (ramp [dur] [iVal] [fVal])  

Example, Ejemplo:  
setOpacity (ramp 10 0 1) $ video "url"  

+ (range [iVal] [fVal] $ sin [vel])

Example, Ejemplo:  
setOpacity (range 0 1 $ sin 0.5) $ video "url"  
