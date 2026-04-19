# Producto

# Descripción general
MediaPro es un sistema de base de datos diseñado para gestionar una productora audiovisual. Permite administrar producciones, personal, equipos técnicos, localizaciones, rodaje y procesos de postproducción.
Este proyecto implementa funciones y triggers en MySQL con el objetivo de automatizar procesos y optimizar la gestión de información.

# Instrucciones de uso
1. Abrir HeidiSQL o cualquier otro gestor de base de datos compatible con MYSQL.

2. Seleccionar la base de datos donde se ejecutarán los scripts.

3. Ejecutar el archivo Scrip - FuncionesMediapro.txt, el cual contiene las funciones y triggers.

3. Verificar que las funciones fueron creadas correctamente:
     SHOW FUNCTION STATUS WHERE Db = 'mediapro';

4. Para verificar los triggers:
     SHOW TRIGGERS;

Notas
- Asegúrese de ejecutar primero el script de la base de datos antes de las funciones y triggers.
- Verifique que las tablas estén correctamente creadas antes de ejecutar los demás archivos.

# Estructura de módulos implementados

1. Módulo de Producción

   Encargado de gestionar la información de las producciones audiovisuales y sus clientes.

   *Tablas: Cliente, Produccion

2. Módulo de Personal

   Gestiona el personal técnico y creativo asignado a cada producción.

   *Tablas: Personal, Produccion_Personal
 
3. Módulo de Rodaje

   Planifica y organiza los días de grabación, incluyendo escenas, actores y recursos.

   *Tablas: Plan_Rodaje, Plan_Rodaje_Escena, Plan_Rodaje_Actor, Plan_Rodaje_Equipo

4. Módulo de Escenas y Actores

   Administra las escenas, personajes y actores que participan en la producción.

   *Tablas: Escena, Actor, Personaje, Escena_Actor

5. Módulo de Equipos Técnicos

   Gestiona los equipos utilizados en las producciones y su mantenimiento.

   *Tablas: Equipo_Tecnico, Mantenimiento, Produccion_Equipo

6. Módulo de Localización

   Administra las locaciones donde se realizan las grabaciones, incluyendo permisos, costos y características.

   *Tablas: Localizacion, Produccion_Localizacion

7. Módulo de Material Grabado

   Registra el material audiovisual generado durante el rodaje.

   *Tablas: Material_Grabado, Audio

8. Módulo de Postproducción

   Controla los procesos de edición, versiones y aprobación del material audiovisual.

   *Tablas: Postproduccion, Material_Postproduccion, Versiones, Aprobacion

9. Módulo de distribución

   Gestiona la distribución y promoción de las producciones audiovisuales.

   *Tablas: Distribucion, Material_Promocional
