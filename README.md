# Transaccionar a IOTA Tangle desde Raspberry pi usando sensores:
- DHT11: Temperatura y humedad.
- MQ135: Sensor ambiental de gases.
- BMP180: Sensor barométrico.


## Wiring DHT11:
 ![](https://www.raspberrypi-spy.co.uk/wp-content/uploads/2017/09/DHT11_pi.png)
## Wiring MQ135:
 ![](https://tutorials-raspberrypi.de/wp-content/uploads/2016/10/Raspberry-Pi-Gas-Sensor-MQ2-Steckplatine.png)
## Wiring BMP180:
 ![](.\http\Wiring\Wiring_BMP180.png)


## Instrucciones:
- Utilizaremos un **Gateway [HTTP](https://github.com/iot2tangle/Streams-http-gateway)** para transaccionar datos a la Tangle de IOTA.
- Dentro del directorio **http** existe un archivo **config.py**, en él indicar el ID del dispositivo y seleccionar con un **1** el sensor determinado a utilizar, y con **0** los restantes.
- Ejemplo:
````
# Device name
device_id = 'DHT11'

# Select sensors to use 1 = use | 0 = skip
dht11 = 1
bmp180 = 0
mq135 = 0
enviromental = 0
gyroscope = 0
accelerometer = 0
magnetometer = 0
````


# Instrucciones:
- En el archivo config.py  si es necesario, modificar la puerta de enlace de la salida de datos y el tiempo de sensado.
  