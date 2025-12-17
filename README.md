Nombre del proyecto:
Calendario con Gestor de Tareas
Objetivo del proyecto:
Desarrollar una aplicación de escritorio en Python utilizando Tkinter que permita a los usuarios gestionar tareas y eventos a través de un calendario interactivo. El sistema integrará funciones CRUD (Crear, Leer, Actualizar, Eliminar) para una gestión completa de tareas con almacenamiento persistente en archivo CSV.
Publico Objetivo:
Características del Usuario:
Estudiantes universitarios: Para organizar tareas, exámenes y trabajos prácticos
Profesionales: Gestión de reuniones, deadlines y proyectos laborales
Personas organizadas: Que necesitan planificar actividades personales
Usuarios técnicos: Confortables con aplicaciones de escritorio simples
Necesidades Cubiertas:
- Organización visual de tareas por fecha
- Categorización de actividades por tipo
- Seguimiento de estado de completitud
- Almacenamiento local sin dependencia de internet
- Interfaz intuitiva y de rápido acceso

Funciones básicas del programa:

leer_tareas(fecha): Lee las tareas del archivo CSV que coinciden con la fecha seleccionada.
escribir_tareas(tareas):	Guarda todas las tareas en el archivo CSV.
mostrar_tareas():	Muestra en pantalla las tareas del día elegido.
agregar_tarea(): Permite añadir una nueva tarea con título, descripción, tipo y hora.
editar_tarea(): Modifica los datos de una tarea existente.
eliminar_tarea()	Borra la tarea seleccionada del listado.
marcar_completada()	Marca o desmarca una tarea como completada.
leer_todas_tareas()	Lee todas las tareas del archivo (sin filtrar por fecha).

Cosas que agregué y cambie en el código actualizado 

1. Almacenamiento SQLite (tareas.db): más seguro, consultas ordenadas, integridad (UNIQUE sobre fecha+titulo+hora).


2. Compatibilidad/Respaldo CSV: tareas.csv sigue existiendo y hay funciones para exportar/importar. Útil para intercambio.


3. Validaciones:

Formato de hora HH:MM (00:00–23:59).

Título obligatorio.

Evita duplicados por UNIQUE(fecha, titulo, hora) (detecta y muestra aviso).


4. Manejo de errores y logging: app.log registra operaciones importantes y excepciones.


5. Export / Import con diálogo: botones para exportar DB a CSV e importar CSV (append o overwrite).


6. UI: botones adicionales (export/import) 






