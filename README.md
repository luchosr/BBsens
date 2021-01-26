# Transaccionar a IOTA Tangle desde Raspberry pi usando sensores:
- DHT11: Temperatura y humedad.
- MQ135: Sensor ambiental de gases.
- BMP180: Sensor barométrico.




## Instrucciones:
- Realizar el cableado acorde al sensor correspondiente como se encuetra en las instrucciones de la carpeta [Wiring](https://vassgit.vass.es/root/iot2tangle_raspberry/-/tree/master/http/Wiring).
- Utilizaremos un **Gateway [HTTP](https://github.com/iot2tangle/Streams-http-gateway)** para transaccionar datos a la Tangle de IOTA.
- Dentro del directorio **http** existe un archivo **config.py**, en él indicar el ID del dispositivo y seleccionar con un **1** el sensor determinado a utilizar, y con **0** los restantes, seleccionamos el intervalo de relé y definimos el endpoint a donde queremos apuntar el sensado.
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


# Select relay interval
relay = 30

# Define endpoint
endpoint = 'http://127.0.0.1:8080/sensor_data'

````


- Posteriormente ejecutamos `python sensorStreams.py`.
- En una terminal aparte ejecutamos el gateway que nos conectará a la Tangle.