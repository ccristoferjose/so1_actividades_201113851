## CONCEPTOS DE SISTEMAS OPERATIVOS
- - - -
Un sistema operativo (SO) es un software que actua como una interfaz entre el hardwware del computador y el usuario. Administra y coordina las actividades del hardware y proporciona servicios a los programas de software.

### TIPOS DE KERNEL Y SUS DIFERENCIAS
- - - -

El Kernel es el núcleo de un sistema operativo. Es el programa principal que se carga en memoria durante el arranque del sistema y tiene control directo sobre todo el hardware del sistema.

Existen varios tipos de Kernel, pero los más comunes son:

#### Monolítico: 

Este es un tipo de kernel que tiene todos sus servicios en un único bloque. Todos los servicios básicos del sistema, como la administración de archivos, administración de procesos, y los drivers de dispositivos, se encuentran en el kernel.

##### Ventajas: 

Alta eficiencia ya que todo se ejecuta en un único espacio de memoria.
Desventajas: Cualquier error puede hacer que todo el sistema falle. Además, realizar cambios o actualizaciones puede ser complicado.

#### Microkernel: 

En este tipo, solo los servicios esenciales están presentes en el kernel, como la comunicación entre procesos y la administración básica de la CPU. Otros servicios se ejecutan en el espacio de usuario como procesos separados.

##### Ventajas: 

Mayor estabilidad, ya que si un servicio falla, no afecta a todo el sistema. Es más fácil de modificar y actualizar.

##### Desventajas: 

Puede ser menos eficiente que el kernel monolítico debido a las comunicaciones entre el microkernel y los servicios del espacio de usuario.

#### Kernel Híbrido: 

Es una combinación de ambos enfoques. Parte del sistema se ejecuta en el espacio del kernel y parte en el espacio del usuario, intentando combinar las ventajas de ambos enfoques.

##### Ventajas: 

Combina las ventajas de los kernels monolítico y microkernel.

##### Desventajas: 
Puede heredar también algunas desventajas de ambos tipos.

### User vs Kernel Mode
- - - -

Los modernos sistemas operativos utilizan dos modos de operación diferentes para proteger los recursos del sistema y garantizar la estabilidad: el modo usuario y el modo kernel.

#### Modo Usuario (User Mode):
Es menos privilegiado. Las aplicaciones en modo usuario no pueden acceder directamente al hardware o a la memoria del sistema. Si una aplicación necesita acceder a un recurso del sistema, tiene que hacer una solicitud al sistema operativo. Ofrece un entorno seguro ya que las aplicaciones no pueden interferir entre sí ni con el núcleo del sistema.

#### Modo Kernel (Kernel Mode):

Es un modo de operación con todos los privilegios. El código que se ejecuta en modo kernel tiene acceso directo a los recursos del sistema. El sistema operativo y algunos drivers de dispositivos operan en modo kernel. Es esencial para tareas críticas del sistema, pero también es arriesgado porque un error en este modo puede llevar a un fallo del sistema completo.