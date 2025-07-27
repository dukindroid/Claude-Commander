# Progreso del proyecto

## TL;DR

Aquí se documenta el camino y avance que ha tenido el proyecto. Se hizo una investigación previa para encontrar cual sería la plataforma de desarrollo más adecuada a usar. Una vez decidido esto hicimos una planeación general del proyecto mediante el uso de un documento de requerimentos de proyecto, instalamos y probamos las herramientas que nos parecieron necesarias y se comenzó a trabajar sobre la carga inicial de datos de la empresa, tomando como inicio la importación de la lista de usuarios y su vinculación con su cuenta de empleado.

Posteriormente se continuará trabajando sobre la carga inicial de roles, información sobre la flota e inventario, y una vez realizado esto, se procederá con la implementación.

## Investigación previa

Para el desarrollo de este proyecto se consideraron dos vertientes posibles de trabajo:

* Desarrollo de una plataforma ERP desde cero sobre una plataforma de desarrollo popular (Vite, Tailwind CSS, Postgresql)

* Desarrollo a partir de la solucion ERP Odoo. 

Al ponderar los beneficios y dificultades que podría llegar a tener cada linea de desarrollo en la práctica, se decidió por la opción con Odoo, ya que esta herramienta en sí ya provee la mayor parte de la funcionalidad que se requiere para el proyecto. La principal limitante en un inicio para no tomar esta vertiente es mi falta de experiencia tanto con la plataforma Odoo como con el lenguaje Python en el que está escrito, pero después de trabajar algunos días con Claude Code me convencí que Claude puede ayudarme a solventar e incluso aprender a fondo la manera en que funciona Python y Odoo.

A manera de ejemplo de lo anterior, hace dos semanas que inició este proyecto yo desconocía por completo la manera de usar Docker, situación que le externé a Claude y prolíficamente se me proveyó una lista de pasos detallada a seguir y una explicación general de como instalar y usar la herramienta Docker. 

Caso contrario, se decidiera empezar con un desarrollo desde cero, el tiempo de desarrollo e implentación se alargaría considerablemente, al tener que reformular soluciones ya probadas y comprobadas (módulos de usuarios, empleados, flota, inventario) que el sistema Odoo ya incluye. 

# Planeación de necesidades y recursos

Actualmente nos encontramos en la fase de planeación, explorando las diferentes herramientas que pudieran llegar a ser útiles o necesarias para el desarrollo del proyecto y familiarizándonos con su instalación y uso. 

Al realizar la investigación previa, resolvimos en integrar un Documento de Requerimentos de Producto (PRD), tanto porque es un elemento necesario en cualquier proyecto de desarrollo formal, como por lo útil que resulta este documento al momento de crear contexto adecuado para Claude Code. Este documento (progress.md) es consecuencia de darle a este PRD forma y orden en todo lo largo del desarrollo del proyecto.

Con la integración del PRD, notamos que las siguientes herramientas iban a ser vitales para un desarrollo ágil:

* Claude Code
* Servidores MCP
    * Manejo local de archivos
    * Acceso a Google Drive (mediante conexión interna MCP de Claude)
    * Acceso a documentación de Odoo: Se configuró la herramienta [Context7](https://context7.com/context7/odoo) para proveer a Claude con la documentación completa de Odoo 18
    * Servidor MCP de Odoo: [mcp-odoo](\\wsl.localhost\Ubuntu-22.04\home\elduke\MyCodingWorkspaces\mcp-odoo)
    * Acceso a Whatsapp: [whatsapp-mpc](\\wsl.localhost\Ubuntu-22.04\home\elduke\MyCodingWorkspaces\whatsapp-mcp)
* Bancos de memoria: Por el momento estamos usando el archivo CLAUDE.md en conjunto con el PRD (@memory_bank/prd-odoo.md) para integrar algo similar a lo que usa la herramienta Cline para mantener una ventana de contexto precisa para Claude. Si llegara a ser necesario, se considerará el uso de herramientas de memoria externas como [Memory Bank MCP server](https://playbooks.com/mcp/alioshr-memory-bank)
* Docker 
* imagen odoo 18 de docker: [Instalación local](@\\wsl.localhost\Ubuntu-22.04\home\elduke\MyCodingWorkspaces\odoo-18-docker-compose)

Cada una de estas herramientas se instaló y se probó su funcionamiento básico. El propósito de estas herramientas es la de proveer un entorno de desarrollo completo en el que Claude cuente con el acceso a documentación y datos para proveer cambios en el sistema que se adhieran a mejores prácticas. 

## Integración e inicialización de datos de la plataforma Odoo

Una vez que identificamos y nos familiarizamos lo mejor posible con las herramientas antes mencionadas, se pide apoyo a Claude Code para integrar paso a paso la metodología y archivos necesarios para la inicialización de la base de datos de Odoo con la información pertinente de la empresa. Se identificaron como primordiales para esta primera fase del proyecto las siguientes tablas de datos:

* Usuarios: Se inicializará en base a una lista del personal de la mina guardado en Google Drive. Claude se encargó de explicarme cómo debe estructurarse un archivo CSV adecuado para la importación directa hacia el sistema Odoo. Este excelente trabajo por parte de Claude lo podemos encontrar en @db_init/user_initialization_guide.md y generará la plantilla inicial de empleados del sistema.

* Roles: Falta establecer un organigrama de la empresa, para a partir de ahí extraer los distintos departamentos y tipos de trabajo (mecánico, mecánico auxiliar, director general, contador, recursos humanos, planta física, electricista, herrero, operador) y formar el archivo CSV para su importación en Odoo. De hecho creo que este paso debería de ser previo al anterior, ya que para ingresar empleados a partir de los usuarios necesitamos saber que rol tiene cada uno.

* Flota: Estamos a la espera de que se nos proporcione información general de la flota de la empresa, para que igual que con los usuarios y roles, se formule un archivo de carga inicial a la base de datos.

## Implementación y pasos posteriores

El siguiente paso en este primer ciclo de desarrollo del proyecto sería su puesta en marcha en producción. Desconosco los pasos para hacer llegar a los usuarios finales (empleados, directivos) de manera efectiva el conocimiento del uso de la herramienta que genere este proyecto. 

## Notas adicionales

Me estoy dando cuenta ahorita que no detallé en lo más mínimo los distintos archivos que habría que formular para la carga inicial de inventario, respecto de los temas de clasificación de los distintos items que se le vayan a agregar, el uso de locaciones específicas para cada item, incluso definir las varias bodegas que tenemos.

