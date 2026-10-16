Tarea:Ejercicios de Sincronizacion

Hernandez Reyes Rebeca Sarai
Bermejo Flores Jose Tristan

El problema que decidieron resolver:
Problema del servidor web

El lenguaje y entorno en que lo desarrollaron:
Lenguaje: python
Entorno: de multiplataforma, compatible con terminales de varios sistemas operativos
Requisitos: Tener instalado python 3, guardar el código fuente como .py para ejecutarlo en la terminal se debe ir a la ubicacion de la carpeta y ejecutar el programa con el comando: '''bash
python3 servidor.py
'''

La estrategia de sincronizacion (mecanismo/patron) que emplearonpara lograrlo:
se utilizo la estrategia de semaforos, usando un semaforo contador que inicia en 0, los hilostrabajadores invocan 'acquire()' paraque se detengan si no esta operando, y se ejecuta '.release()' para despertar un hilo disponible, tambien se empelan cerrojos para proteger las secciones criticas donde se manupulan la cola compartida de solicitudes y se escribe en la estructura de contabilidad, preveniendo condiciones de carrera.

Si estan implementandoalguno de los refinamientos:
si, implementamos el refinamiento de contabilidad del sistema, ya que cadahilo trabajador, antes de terminar de atender una solicitud, registra de forma segura datos como identificador del trabajador, nombre de la pagina solicitada y marca de tiempo exacta en una bitacora global, ademas de concluir las tareas y apagar el servidor ordenadamente, el progarama despliega un reporte de contabilidad detallado que resumeel historial de rendimiento de los hilos.

cualquier duda que tengan. si notan que alhun pedazo de la implementacion podria mejorar, si algono les termino de quedar bien...: si nos gustaria saber de que forma mejorar el código, tuvimos varias complicaciones porque uno de los impedimientos era usar la verificacion con condicionales, y pues iniciando justo nos fuimos directo por esa rama, entonces puede que nuestra implementacion no sea lo mas pulido o la forma mas eficiente de implementarlo.

