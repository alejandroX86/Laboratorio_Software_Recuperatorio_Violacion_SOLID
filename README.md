README.md
Catedra: Laboratorio de Software
Profesor: Daniel Alejandro Fernandez
Alumno: Omar Alejandro Bazar

Proyecto: Taller de Mantenimiento
Este proyecto viola los 5 principios SOLID de la siguiente manera:

1. Principio de Responsabilidad Única (Single Responsibility Principle)
La clase MantenimientoFacturacionInventarioManager viola este principio al tener múltiples responsabilidades: realizar mantenimiento, enviar facturas y gestionar el inventario. Cada una de estas responsabilidades debería estar en una clase separada.

2. Principio de Abierto/Cerrado (Open/Closed Principle)
La clase MotorGasolinaElectrico viola este principio al no estar abierta a la extensión. Si se quisiera agregar un nuevo tipo de motor, habría que modificar esta clase en lugar de crear una nueva que extienda su funcionalidad.

3. Principio de Segregación de Interfaces (Interface Segregation Principle)
La interfaz ITrabajoComidaCapacitacion viola este principio al definir métodos que no están relacionados con su responsabilidad principal. Por ejemplo, los métodos Trabajar y Descansar no están relacionados con Comer y Capacitarse.

4. Principio de Sustitución de Liskov (Liskov Substitution Principle)
La clase AutomovilCamion viola este principio al heredar de VehiculoBase y asumir que todos los vehículos tienen un motor. Un camión podría tener un motor diferente al de un automóvil, lo que haría que la sustitución no sea válida.

5. Principio de Inversión de Dependencias (Dependency Inversion Principle)
La clase Taller viola este principio al depender de clases concretas (AutomovilCamion, Automovil, Camion) en lugar de abstracciones. Esto hace que el código sea menos flexible y más difícil de mantener.

Para cumplir con los principios SOLID, se recomienda refactorizar el código siguiendo las mejores prácticas de diseño orientado a objetos, como la separación de responsabilidades, el uso adecuado de interfaces y clases abstractas, y la inyección de dependencias.
