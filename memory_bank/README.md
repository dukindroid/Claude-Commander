# Banco de Memoria - Proyecto ERP Grupo Minero La Fundición

## Resumen

Este banco de memoria contiene documentación exhaustiva para el proyecto de implementación de ERP basado en Odoo para Grupo Minero La Fundición, una empresa minera que busca optimizar la gestión de flotas, la coordinación de mantenimiento y el control de inventario.

## Estructura de Archivos

### Documentación Principal (Requerida por Cline)
- **`projectBrief.md`** - Documento fundamental que define el alcance del proyecto, usuarios y requisitos técnicos
- **`productContext.md`** - Contexto de negocio, problemas resueltos y visión de éxito
- **`systemPatterns.md`** - Arquitectura técnica, patrones de diseño y rutas de implementación
- **`techContext.md`** - Tecnologías, configuración de desarrollo, dependencias y restricciones
- **`activeContext.md`** - Enfoque de trabajo actual, cambios recientes, próximos pasos y contexto de sesión
- **`progress.md`** - Progreso detallado del proyecto, decisiones de investigación y estado de implementación

### Contexto Adicional
- **`prd-odoo.md`** - Documento de Requisitos de Producto exhaustivo (centrado en Odoo)
- **`prd.md`** - PRD alternativo con enfoque en colaboración de paneles
- **`.clinerules`** - Estructura del banco de memoria y directrices de flujo de trabajo para Cline

## Estado del Proyecto

**Fase Actual**: Planificación y Configuración Inicial de Datos
**Cronograma**: Implementación de 12 semanas en 3 fases
**Plataforma**: Odoo Community 18.0 con despliegue Docker

### Logros Clave
✅ Selección de plataforma (Odoo vs. desarrollo personalizado)
✅ Configuración y prueba del entorno Docker
✅ Configuración de servidores MCP para capacidades mejoradas de IA
✅ Metodología de importación de datos de empleados establecida
✅ Estructura de documentación exhaustiva creada

### Prioridades Inmediatas
🔄 Definir la estructura organizacional y la jerarquía de roles
🔄 Completar el proceso de importación de CSV de empleados
🔄 Configurar el módulo de flota con el registro de vehículos
🔄 Configurar el módulo de inventario con el catálogo de repuestos

## Referencia Rápida

### Usuarios Objetivo
- **40 empleados en total** en operaciones, mantenimiento, administración
- **Módulos principales**: RRHH/Empleados, Gestión de Flotas, Control de Inventario
- **Roles clave**: Operadores, Mecánicos, Supervisores, Personal Administrativo

### Métricas de Éxito
- **≥80% de disponibilidad de flota**
- **25% de reducción en el tiempo de mantenimiento**
- **98% de precisión de inventario**
- **100% de adopción por parte del usuario en 3 meses**

### Pila Tecnológica
- **Plataforma**: Odoo Community 18.0
- **Base de Datos**: PostgreSQL
- **Despliegue**: Docker + Docker Compose
- **Desarrollo**: Python con asistencia de IA (Claude Code/Cline)
- **Importación de Datos**: Plantillas basadas en CSV

## Para Nuevas Sesiones

Al iniciar una nueva sesión, Cline debe:
1. Leer TODOS los archivos del banco de memoria para comprender el contexto del proyecto
2. Revisar `activeContext.md` para el enfoque de trabajo actual y los bloqueadores
3. Consultar `progress.md` para el estado de implementación más reciente
4. Consultar `systemPatterns.md` y `techContext.md` para decisiones técnicas

## Contacto y Recursos

- **Ubicación del Proyecto**: `/home/elduke/MyCodingWorkspaces/Claude Commander`
- **Instancia de Odoo**: `\\wsl.localhost\Ubuntu-22.04\home\elduke\MyCodingWorkspaces\odoo-18-docker-compose`
- **Guía de Importación de Datos**: `../db_init/user_initialization_guide.md`
- **Servidores MCP**: Context7 (Odoo docs), mcp-odoo, whatsapp-mcp, Google Drive MCP

---

*Última Actualización: 26 de enero de 2025*
*Versión del Banco de Memoria: 1.0*
