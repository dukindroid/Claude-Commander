# Resumen del Proyecto

## Visión General

Construcción de un **sistema ERP para operaciones mineras** basado en Odoo Community 18.0 que **optimizará la gestión de flotas, la coordinación de mantenimiento y el control de inventario** para Grupo Minero La Fundición, una empresa minera con aproximadamente 40 empleados.

## Características Principales

- **Gestión de Flotas**: Seguimiento en tiempo real de vehículos y equipos mineros con asignaciones de operador
- **Coordinación de Mantenimiento**: Flujos de trabajo de mantenimiento preventivo y correctivo estructurados con órdenes de trabajo
- **Control de Inventario**: Gestión integral de repuestos y materiales con integración de adquisiciones
- **Gestión de Empleados**: Jerarquía departamental y control de acceso basado en roles
- **Interfaz de Panel**: Vistas específicas de roles para operadores, mecánicos, supervisores y administradores
- **Diseño Adaptable a Móviles**: Interfaz lista para el campo para tabletas y teléfonos inteligentes

## Usuarios Objetivo

**Usuarios Principales:**
- **Operadores de Flota** (~15 usuarios): Necesitan acceso rápido al estado del equipo asignado y reporte de problemas
- **Mecánicos y Técnicos** (~8 usuarios): Requieren gestión de órdenes de trabajo e información de disponibilidad de piezas
- **Supervisores y Gerencia** (~5 usuarios): Necesitan supervisión operativa y paneles de toma de decisiones
- **Personal Administrativo** (~12 usuarios): Manejan adquisiciones, inventario y administración general del sistema

**Roles de Usuario:**
- Director General
- Supervisor de Operaciones
- Supervisor de Mantenimiento
- Operadores de Equipo
- Mecánicos (Líder y Auxiliar)
- Personal de Almacén/Inventario
- Compras/Adquisiciones
- Personal Administrativo

## Preferencias Técnicas

### Tecnologías Requeridas
- **Plataforma**: Odoo Community 18.0 (marco ERP)
- **Base de Datos**: PostgreSQL
- **Despliegue**: Contenerización Docker
- **Desarrollo**: Python (lenguaje nativo de Odoo)

### Herramientas de Desarrollo
- **Asistente de IA**: Claude Code (Cline) para soporte de desarrollo
- **Documentación**: Servidor MCP Context7 para acceso a la documentación de Odoo
- **Integración**: Servidores MCP personalizados para capacidades mejoradas
- **Control de Versiones**: Git para el seguimiento de la configuración y los módulos personalizados

### Requisitos Específicos
- **Importación de Datos**: Carga inicial de datos basada en CSV para empleados, flota e inventario
- **Soporte Móvil**: Interfaz web responsiva (no se requiere una aplicación móvil nativa inicialmente)
- **Rendimiento**: Soporte para 40 usuarios concurrentes con tiempos de respuesta inferiores a 2 segundos
- **Seguridad**: Control de acceso basado en roles utilizando la autenticación incorporada de Odoo
- **Despliegue**: Instalación local/en las instalaciones para la seguridad de los datos

### Restricciones
- **Presupuesto**: Minimizar costos utilizando soluciones comunitarias/de código abierto
- **Cronograma**: Implementación de 12 semanas en 3 fases
- **Recursos**: Desarrollador único con asistencia de IA
- **Curva de Aprendizaje**: Desarrollador nuevo en Python y la plataforma Odoo
- **Alcance**: Enfoque en módulos principales (RRHH, Flota, Inventario) antes de expandir

## Métricas de Éxito

- **Disponibilidad de Flota**: Lograr ≥80% de disponibilidad de equipos
- **Eficiencia de Mantenimiento**: 25% de reducción en el tiempo promedio de reparación
- **Precisión de Inventario**: 98% de precisión en el registro de existencias
- **Adopción por el Usuario**: 100% de uso activo en 3 meses
- **Rendimiento del Sistema**: 99% de tiempo de actividad durante las horas de operación (6 AM - 6 PM)
