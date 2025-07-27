# One-pager: Sistema ERP para Empresa Minera

## 1. TL;DR
Implementación de una solución ERP basada en Odoo Community 18.0 para una empresa minera de ~40 empleados. La fase inicial se enfoca en configurar los módulos de Empleados, Flota e Inventario para reducir el tiempo improductivo de la maquinaria pesada en talleres mediante un marco operativo estructurado y actividades programadas.

## 2. Metas
### Metas de negocio
* Reducir el tiempo de inactividad de maquinaria pesada en talleres
* Optimizar la gestión de mantenimiento preventivo de la flota
* Mejorar la eficiencia operativa mediante procesos estructurados
* Establecer un marco de trabajo digital para todas las áreas de la empresa

### Metas de Usuarios
* **Operadores de maquinaria pesada**: Acceso rápido a información de asignación de equipos y reportes de estado
* **Mecánicos**: Gestión eficiente de órdenes de trabajo y acceso a listas de materiales para servicios preventivos
* **Contadores**: Seguimiento preciso de inventario y costos asociados a la flota
* **Socios comerciales**: Acceso controlado a información relevante de inventario y servicios

### Anti-Metas
* Implementación completa de todos los módulos de Odoo en la fase inicial
* Integración con sistemas externos existentes
* Funcionalidades avanzadas de reporting y analytics

## 3. Historias de usuarios
**Mecánico de taller**: "Como mecánico, necesito acceder rápidamente a la lista de materiales y historial de servicios de cada unidad de la flota para realizar mantenimientos preventivos eficientes y evitar paros no programados."

**Operador de maquinaria**: "Como operador, necesito saber qué equipo tengo asignado y reportar cualquier problema o anomalía de manera sencilla para mantener la productividad."

**Contador**: "Como contador, necesito un control preciso del inventario de repuestos y materiales, así como el seguimiento de costos de mantenimiento por unidad de flota."

**Supervisor de operaciones**: "Como supervisor, necesito visibilidad completa del estado de la flota y programación de mantenimientos para optimizar la disponibilidad de equipos."

**Administrativo**: "Como administrativo, necesito tener un dashboard que me proporcione una vista de ojo de águila sobre el status general de la flota, el valor final de inventario y las actividades asignadas para el día para los distintos colaboradores" 

## 4. Requerimentos funcionales
### Prioridad Alta (Fase 1)
* **Módulo Empleados**: Configuración de jerarquía departamental y roles
* **Módulo Inventario**: Sistema de gestión de repuestos y materiales con script de importación de datos iniciales
* **Módulo Flota**: Registro de unidades con asignación de operadores y listas de materiales para servicios preventivos

### Prioridad Media (Fase 2)
* **Gestión de servicios**: Registro detallado de mantenimientos realizados
* **Reportes de problemas**: Sistema de tickets para fallas y reparaciones
* **Programación de mantenimientos**: Calendario de servicios preventivos

### Prioridad Baja (Futuras fases)
* Integración con sistemas de terceros
* Dashboards avanzados y reportes personalizados
* Módulos adicionales según necesidades identificadas

## 5. Experiencia de usuario
### Flujo principal de usuario
* **Login y dashboard**: Acceso basado en roles con vista personalizada según perfil
* **Gestión de flota**: Navegación intuitiva entre unidades, asignaciones y estados
* **Inventario**: Búsqueda rápida de materiales y actualización de stocks
* **Servicios**: Creación y seguimiento de órdenes de trabajo paso a paso

### Casos límite y notas de UI
* Acceso fuera de línea limitado para operadores en campo
* Interfaz responsiva para dispositivos móviles y tablets
* Validaciones de datos críticos (stocks negativos, asignaciones duplicadas)
* Notificaciones automáticas para mantenimientos vencidos

## 6. Narrativa
Es lunes por la mañana. Carlos, supervisor de operaciones, inicia su jornada revisando el dashboard de flota en su tablet. Ve que tres camiones requieren mantenimiento preventivo esta semana. Con un clic, programa las citas y asigna los recursos necesarios.

Meanwhile, María, mecánica del taller, recibe una notificación en su dispositivo móvil sobre el camión CAT-001 que llegará para servicio. Accede al historial de la unidad, revisa la lista de materiales requeridos y verifica que todos los repuestos estén disponibles en inventario. Todo está listo—no hay sorpresas ni demoras.

Pedro, el operador de CAT-001, reporta una vibración inusual a través de la app móvil. El sistema genera automáticamente un ticket de mantenimiento y notifica al taller. En lugar de esperar hasta el próximo servicio programado, el problema se atiende de inmediato, evitando una falla mayor y costosa.

## 7. Success metrics
* **Reducción del tiempo de inactividad**: Disminución del 25% en horas de maquinaria fuera de servicio
* **Eficiencia de mantenimiento**: Reducción del 30% en tiempo promedio de servicios preventivos
* **Precisión de inventario**: 98% de exactitud en registros de stock
* **Adopción del sistema**: 100% de usuarios activos en los módulos implementados dentro de 3 meses
* **Satisfacción del usuario**: Puntuación mínima de 4/5 en evaluaciones de usabilidad

## 8. Milestones & sequencing
### Fase 1: Fundamentos (Semanas 1-4)
* Configuración de Docker con Odoo Community 18.0
* Configuración del módulo Empleados con jerarquía departamental
* Implementación del módulo Inventario con script de importación
* Configuración básica del módulo Flota

### Fase 2: Operatividad (Semanas 5-8)
* Registro detallado de unidades de flota con asignación de operadores
* Implementación de listas de materiales para servicios preventivos
* Sistema de registro de servicios y problemas
* Pruebas de usuario y refinamiento

### Fase 3: Optimización (Semanas 9-12)
* Capacitación completa del equipo
* Migración de datos históricos
* Monitoreo de métricas de éxito
* Planificación de fases futuras basada en feedback del usuario 