# KUBERNETES.__GB__
he istalado
```bash
choco install kubernetes-cli
kubectl version --client
```
# k0s kubernetes ubuntu
<a href="https://k0sproject.io/">k0s</a>
<a href="https://www.youtube.com/watch?v=gmFSmzAWcig">youtobe k0s 1hs</a>
  
# kubernetes curso
- Contenedor: no es una entidad. Son distintas tecnologias que trabajando en conjunto crean un contenedor.

Las 3 tecnologias son:

CGroups: Asignan a cada contenedor/proceso los recursos va a utilizar (memoria, disco, cpu). Limitan el uso de recursos del sistema operativo para cada contenedor.

Chroot: Nos permite que nuestro proceso/container tenga visibilidad sobre archivos donde tiene que trabajar y no acceder a otros recursos del sistema.

Namespaces: (son 7, aqui los mas importantes):

    Mount: Nos permite que nuestro proceso tenga una visibilidad reducida de los directorios. Esto permite que dos contenedores que trabajen sobre un sistema de archivos no se interfieran entre si.

    Networking: Permite que cada contenedor tenga su dirección IP, su tabla de rutas, su interfaz de red, y que no interfiera con otros contenedores.
    Concepto de POD: Entidad atomica scheduleable - Entidad sobre la cual kubernetes va a ejecutar los contenedores. (se verá en detalle más adelante).

    PID o de proceso: si ejecutamos un ps cuando ejecutamos nuestro contenedor, vamos a ver que nuestro contenedor es el process id 1 y no vemos todo el resto de los procesos del SO. Esto es posible gracias al namespace de procesos. (se verá en detalle más adelante).
    
 - Docker & Kubernetes

    Docker se encarga principalmente de gestionar los contenedores.
    Kubernetes es una evolución de proyectos de Google Borg & Omega.
    Kubernetes pertenece a la CNCF (Cloud Native Computing Foundation).
    Todos los cloud providers (GCP/AWS/Azure/DO) ofrecen servicios de managed k8s utilizando Docker como su container runtime
    Es la plataforma más extensiva para orquestación de servicios e infraestructura

Kubernetes en la práctica

    K8s permite correr varias réplicas y asegurarse que todas se encuentren funcionando.
    Provee un balanceador de carga interno o externo automáticamente para nuestros servicios.
    Definir diferentes mecanismos para hacer roll-outs de código.
    Políticas de scaling automáticas.
    Jobs batch.
    Correr servicios con datos stateful.

Todos los contenedores que viven dentro de un mismo Pod comparten el mismo segmento de red.
