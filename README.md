# Parcial 1 SPD
![Tinkercad](./img/ArduinoTinkercad.jpg)


## Integrantes
- Angel Zabala

## Proyecto: Montacargas.
![Tinkercad](./img/MontacargaArduino.png)

## Descripcion

Se nos pide armar un modelo de montacarga funcional como maqueta para un hospital. El
objetivo es que implementes un sistema que pueda recibir ordenes de subir, bajar o pausar
desde diferentes pisos y muestre el estado actual del montacargas en el display 7
segmentos.

## Funcion principal

Esta funcion se encarga de identificar que pulsador fue tocado para asi llevar a cabo el ascenso, descenso o la pausa del montacargas

estado_uno, estado_dos, y estado_tres son los tres pulsadores que al ser seleccionados dan lugar a las distintas acciones del mecanismo

~~~ C
void estados(int estado_uno, int estado_dos, int estado_tres)
{
  if(estado_uno == LOW)
  {
   prenderApagar(verde, rojo);
   piso = subirM(piso); 
  }
  
  if(estado_dos == LOW)
  { 
    prenderApagar(verde, rojo);
    piso = bajarM(piso); 
  }
  
  if(estado_tres == HIGH)
  {
    prenderApagar(rojo, verde);
    Serial.println("montacargas pausado");
    estadoPausa = 0;
  }
  
  ~~~
  
  ## 🤖 link al proyecto
  - [proyecto](https://www.tinkercad.com/things/25jh8Ax4xvM)
