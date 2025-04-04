Este proyecto simula un sistema automatizado de puerta para perros que responde a ladridos y utiliza sensores para garantizar la seguridad al abrir y cerrar la puerta. A continuación, te explico los componentes principales del proyecto:

1. main.py
Este archivo contiene el punto de entrada del programa y simula el flujo de interacción con el sistema.

Flujo del programa:
Se crea una instancia de SistemaPuertaPerruna.
El perro (Bobby) ladra dos veces para salir, y el sistema procesa el ladrido.
Después de un tiempo, Bobby regresa, ladra nuevamente, y el sistema lo deja entrar.
La puerta se abre y se cierra automáticamente después de un tiempo, verificando que sea seguro cerrarla.
Código relevante:
Este método activa el sistema para abrir la puerta si detecta un ladrido válido.

2. SistemaPuertaPerruna
Este es el núcleo del sistema. Coordina los sensores y el actuador de la puerta.

Componentes principales:
Sensores: Detectan si el sonido es un ladrido y verifican si es seguro cerrar la puerta.
ActuadorPuerta: Controla el estado de la puerta (abierta o cerrada).
Método procesar_ladrido: Si el ladrido es válido, abre la puerta y activa un cierre automático.
Cierre automático:
El método _iniciar_cierre_automatico utiliza un hilo (threading.Thread) para cerrar la puerta después de 5 segundos, verificando constantemente si es seguro cerrarla.

3. Sensores
Simula los sensores del sistema.

Funciones principales:
detectar_ladrido: Reconoce si el sonido es un ladrido válido.
es_seguro_cerrar: Simula la detección de movimiento cerca de la puerta para evitar cerrarla si no es seguro.
4. ActuadorPuerta
Controla el estado de la puerta.

Funciones principales:
abrir: Cambia el estado de la puerta a "abierta".
cerrar: Cambia el estado de la puerta a "cerrada".
5. Pruebas unitarias (unittest)
El archivo incluye pruebas unitarias para validar el comportamiento del sistema.

Caso de prueba: "Salir de casa"
Simula que el perro ladra y el sistema reconoce el ladrido.
Verifica que la puerta se abra correctamente.
Simula el cierre automático de la puerta, asegurándose de que sea seguro cerrarla.
Código relevante:
Estas pruebas aseguran que el sistema responde correctamente a los ladridos y controla el estado de la puerta.

6. Simulaciones
El proyecto utiliza simulaciones para simplificar el comportamiento del sistema:

random.random(): Simula la probabilidad de que sea seguro cerrar la puerta.
time.sleep(): Simula tiempos de espera para abrir/cerrar la puerta.
Mejoras posibles
Reconocimiento avanzado de ladridos: Usar modelos de aprendizaje automático para identificar ladridos específicos.
Interfaz gráfica o API: Permitir al usuario monitorear y controlar el sistema desde una aplicación.
Persistencia de datos: Guardar registros de cuándo se abrió/cerró la puerta.
Este proyecto es un buen ejemplo de cómo combinar sensores, actuadores y lógica de control para resolver un problema cotidiano de manera automatizada. ¿Te gustaría profundizar en algún componente o agregar nuevas funcionalidades?