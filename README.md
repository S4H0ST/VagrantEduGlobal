DESPLIEGUE DE MAQUINAS CON VAGRANT
----
En este documento se va ha explicar como desplegar las siguientes maquinas y su contenido.
> [!IMPORTANT]
> Es importante que se tenga [VirtualBox](https://www.virtualbox.org/) instalado para poder usarlo como ***provider*** para interactuar y gestionar las maquinas virtuales que se creen.

1. [Ubuntu 22.04 con GlobalProtect 6.0.7 y Eduroam](./Vagrantfile)

Montaje
---

Para poder desplegarlos tendremos que dirigirnos a la carpeta donde se aloja el ```Vagrantfile``` de aquella maquina que queremos lanzar, todas van dentro de una carpeta identificativa con el nombre de la maquina.

>[!TIP]
> Este nombre es necesario para que se pueda reconocer de manera por defecto, resulta más comodo esta forma si se guardan en carpetas diferentes.

Desde la terminal ejecutamos lo siguiente:

```
vagrant up
```
Una vez montada y creado nuestra box nos conectaremos mediante ssh de la siguiente forma:

```
vagrant ssh
```
Y ya tendriamos nuestra maquina levantada.

Para salir de la maquina basta con ejecutar ```exit```, y para apagar la maquina con ```vagrant halt```

Configuración
--
Dentro de la maquina para ejecutar eduroam deberemos ejecutar el siguiente comando:
```
python3 eduroam-linux-URJC-Universidad_Rey_Juan_Carlos.py
```
Al final de la instalación, introducimos las credenciales institucionales de la URJC.

Para el globalProtect basta con ejecutar ```globalprotect```.

>[!NOTE]
> Todos los archivos descargados se encuentran en la carpeta ```./vagrant```.
