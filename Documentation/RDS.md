
## Documento de Requisitos de Software(DRS)

### 1. Introducción
#### 1.1 Propósito
El propósito de este DRS es capturar y definir todos los requisitos funcionales y no funcionales que debe cumplir el Vault Flow. Servirá como base para el desarrollo, las pruebas y la validación del sistema por parte de los desarrolladores, evaluadores y stakeholders.

#### 1.2 Alcance del sistema
Vault Flow tiene como objetivo principal ayudar a los usuarios individuales a registrar, gestionar, visualizar, analizar ingresos y categorizarlos gastos personales para facilitar el control y toma de decisiones financieras. 

No incluye: Integración directa con bancos o dinero real, manejo de impuestos o gestión de finanzas múltiples así como no maneja datos externos mas que lo que el usuario proporciona.

#### 1.3 Definición de acrónimos

### 2. Descripción general del sistema
#### 2.1 Perspectiva del producto
En Vault Flow es un sistema autónomo que opera como aplicación web, independiente.
De momento esta pensado para un uso en una red personal sin integraciones externas pero con la posibilidad de expandirse o incluso que salga disponible al publico este proyecto esta considerado par aun ecosistema personal de productividad y gestión de finanzas

#### 2.2 Funcionalidad del producto
**El sistema permitirá al usuario:**
1. Registro y Autenticación
2. Gestión de Ingresos y Gastos
3. Registro de cuentas o Tarjetas 
4. Gestión de Ahorro
5. Registro de gastos recurrentes
6. Gráficos de movimientos(Talvez)

#### 2.3 Características de usuarios
**Usuario final** 
Individuo con necesidad de tener un registro y control de sus finanzas personales con conocimientos básicos en el uso de aplicaciones web.
Este usuario tiene acceso directo a sus propios datos y funcionalidades completas 

#### 2.4 Restricciones del sistema
- Compatibilidad con los navegadores modernos o mas comunes
- Seguridad de la información de los usuarios 
- Tiempo de desarrollo 
#### 2.5 Suposiciones y dependencias
- Suponemos que el usuario tiene conexión a la red local donde se lanzara la aplicación (de momento)
- Suponemos que el usuario conoce su información al momento de ingresar los datos de las cuentas a gestionar
- Suponemos que el usuario es capaz de mantener en orden sus movimientos entre cuentas y gastos
- Depende del hosteo en el servidor personal 
- Depende de la red personal (de momento)
#### 2.6 Requisitos futuros
- modulo para gestión de inversiones
### 3 Requerimientos Específicos
#### 3.1 Requerimientos Funcionales
**Autenticación y usuario**
- RF01: El sistema permite crear/registrar una cuenta al usuario con email y contraseña
- RF02: El sistema permite iniciar sesión con email y contraseña
- RF03: El sistema permite al usuario modificar información básica de perfil 
- RF04: El sistema permite cerrar sesión

**Gestión de  Transacciones (Ingresos y gastos)**
- RF05: El sistema permite al usuario ingresar un gasto detallando el monto, una categoría y una breve descripción
- RF06: El sistema permite al usuario agregar un ingreso detallando el monto, una descripción,  y la recurrencia de este (regular o irregular)
- RF07: El sistema debe permitir modificar la transacción (gasto o ingreso)agregada
- RF08: El sistema debe permitir eliminar la transacción agregada
- RF09: El sistema debe permitir registrar en un apartado gastos recurrentes como pagos mensuales
- RF10:El sistema debe permitir de manera opcional asociar la transacción a una cuenta registrada o bóveda de ahorro
- RF11: El sistema debe permitir marcar la transacción echa como completada 
- RF21: El sistema debe mostrar el total de cada tipo de transacción (ingresos y gastos)

**Gestión de ahorro**
El sistema tendrá un apartado para la gestión de ahorro y llevar un mejor control de este

- RF12: El sistema debe permitir abrir una bóveda de ahorro donde el usuario ingresa el monto de su ahorro actual
- RF13: El sistema debe mostrar un historial de los movimientos realizados en la bóveda de ahorro
- RF14: El sistema debe permitir realizar retiros del ahorro la cual contendrá una descripción del motivo y el monto
- RF15: El sistema deberá permitir realizar ingresos a la bóveda de ahorro
- RF16: El sistema deberá mostrar una suma de los retiros de la bóveda tiene el fin de que el usuario sienta la responsabilidad de reponer sus ahorros

**Registro de cuentas**
El sistema podrá tener cuentas que el usuario ingresa para llevar un mejor registro de sus transacciones con sus cuentas/tarjetas reales el uso de las cuentas es opcional para una gestión mas avanzada de la finanzas 

- RF17: El sistema permite registrar cuantas el usuario debe ingresar el monto de la cuenta que quiere registrar
- RF18: El sistema debe mostrar un historial de los movimientos realizados en la cuenta
- RF19: El sistema debe permitir realizar ingresos a la cuenta que esta vinculado con las transacciones 
- RF20: El sistema debe permitir realizar retiros a la cuenta mediante las transacciones 


**Reportes** (opcional)
El sistema podrá mostrar gráficos de los movimientos
- RF22: El sistema debe mostrar gráficos sencillos de un resumen de las transacciones (ej. una grafica de pastel de los ingresos)
![[Pasted image 20251203173604.png]]
- RF23: El sistema debe mostrar un balance ingresos- gastos 
- RF24: El sistema debe mostrar una categoría dependiendo del balance
![[Pasted image 20251203173458.png]]

#### 3.2 Requerimientos no funcionales

RNF1: La contraseña de los usuarios debe ser almacenadas con hashing seguro 
RNF2: La aplicación deber ser intuitiva para usuarios nuevos 
RNF3: El cogido debe usar una arquitecta en capas clara y documentada para facilitar futuras modificaciones 

#### 3.3 Requerimientos de interfaz
RI1: La interfaz deber ser responsiva y adaptable entre pantallas de escritorio y móviles
RI2: Todos los campos deben incluir validaciones para asegurar que las cantidades ingresadas sean números correctos
RI3: La comunicación entre el cliente y servidor tiene que ser mediante el protocolo HTTPS

#### 4 Modelos y Diagramas
**Mockups UI**
Link: https://app.banani.co/preview/WukU2AP7RGVD 
