# Project Brief

## Overview

Building an **ERP system for mining operations** based on Odoo Community 18.0 that will **optimize fleet management, maintenance coordination, and inventory control** for Grupo Minero La Fundición, a mining company with approximately 40 employees.

## Core Features

- **Fleet Management**: Real-time tracking of mining vehicles and equipment with operator assignments
- **Maintenance Coordination**: Structured preventive and corrective maintenance workflows with work orders
- **Inventory Control**: Comprehensive spare parts and materials management with procurement integration
- **Employee Management**: Departmental hierarchy and role-based access control
- **Dashboard Interface**: Role-specific views for operators, mechanics, supervisors, and administrators
- **Mobile-Responsive Design**: Field-ready interface for tablets and smartphones

## Target Users

**Primary Users:**
- **Fleet Operators** (~15 users): Need quick access to assigned equipment status and problem reporting
- **Mechanics and Technicians** (~8 users): Require work order management and parts availability information
- **Supervisors and Management** (~5 users): Need operational oversight and decision-making dashboards
- **Administrative Staff** (~12 users): Handle procurement, inventory, and general system administration

**User Roles:**
- Director General
- Operations Supervisor
- Maintenance Supervisor
- Equipment Operators
- Mechanics (Lead and Auxiliary)
- Warehouse/Inventory Staff
- Procurement/Purchasing
- Administrative Personnel

## Technical Preferences

### Required Technologies
- **Platform**: Odoo Community 18.0 (ERP framework)
- **Database**: PostgreSQL
- **Deployment**: Docker containerization
- **Development**: Python (Odoo's native language)

### Development Tools
- **AI Assistant**: Claude Code (Cline) for development support
- **Documentation**: Context7 MCP server for Odoo documentation access
- **Integration**: Custom MCP servers for enhanced capabilities
- **Version Control**: Git for configuration and custom module tracking

### Specific Requirements
- **Data Import**: CSV-based initial data loading for employees, fleet, and inventory
- **Mobile Support**: Responsive web interface (no native mobile app required initially)
- **Performance**: Support 40 concurrent users with sub-2 second response times
- **Security**: Role-based access control using Odoo's built-in authentication
- **Deployment**: Local/on-premise installation for data security

### Constraints
- **Budget**: Minimize costs by using community/open-source solutions
- **Timeline**: 12-week implementation in 3 phases
- **Resources**: Single developer with AI assistance
- **Learning Curve**: Developer new to Python and Odoo platform
- **Scope**: Focus on core modules (HR, Fleet, Inventory) before expanding

## Success Metrics

- **Fleet Availability**: Achieve ≥80% equipment availability
- **Maintenance Efficiency**: 25% reduction in average repair time
- **Inventory Accuracy**: 98% stock record precision
- **User Adoption**: 100% active usage within 3 months
- **System Performance**: 99% uptime during operational hours (6 AM - 6 PM)
