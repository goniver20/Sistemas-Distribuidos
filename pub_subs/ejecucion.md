# Guía de Uso
## 1. Ejecutar el *broker*
Abre una terminal (*cmd*)
~~~bash
python broker.py
~~~
Se mostrará como resultado:
~~~bash
[BROKER] escuchando en 0.0.0.0:14000...
~~~
## 2. Ejecutar uno o más suscriptores
Abre una terminal y ejecuta un suscriptor o más
~~~bash
python subscriber.py
~~~
Cuando se te pida escribe el tema (*topic*), por ejemplo:
~~~bash
Tema a suscribirse: deportes
~~~
El sistema mantendrá la conexión abierta esperando mensajes del *broker*
## 3. Ejecutar uno o más publicadores
En otra terminal:
~~~bash
python publisher.py
~~~
Envía el mensaje en este formato:
~~~bash 
deportes: ¡El Cruz Azul ganó 2-0!
~~~
Todos los *suscriptores* suscritos a *deportes* recibirán:
~~~bash
[deportes] ¡El Real Merced ganó 20-0!
~~~