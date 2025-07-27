# Technical Context

## Technologies Used

### Core Platform
- **Odoo Community 18.0**: Primary ERP platform
- **Python**: Odoo's underlying programming language
- **PostgreSQL**: Database management system
- **Docker**: Containerization and deployment
- **Docker Compose**: Multi-container orchestration

### Development Tools
- **Claude Code (Cline)**: AI-assisted development and documentation
- **VSCode**: Primary development environment
- **Git**: Version control (implied for project management)

### MCP Servers and Integrations
- **Context7**: Odoo 18 documentation access for Claude
- **mcp-odoo**: Custom MCP server for Odoo integration
- **whatsapp-mcp**: WhatsApp integration capabilities
- **Google Drive MCP**: Document and file management
- **Memory Bank MCP**: Potential future context management

## Development Setup

### Local Environment
- **Operating System**: Linux (WSL Ubuntu 22.04)
- **Docker Installation**: Local Docker environment
- **Odoo Instance**: `\\wsl.localhost\Ubuntu-22.04\home\elduke\MyCodingWorkspaces\odoo-18-docker-compose`
- **Project Location**: `/home/elduke/MyCodingWorkspaces/Claude Commander`

### Container Configuration
```yaml
# Docker Compose setup for Odoo 18
services:
  odoo:
    image: odoo:18.0
    depends_on:
      - postgres
    ports:
      - "8069:8069"
    volumes:
      - odoo-data:/var/lib/odoo
      - ./config:/etc/odoo
      - ./addons:/mnt/extra-addons
  
  postgres:
    image: postgres:15
    environment:
      POSTGRES_DB: postgres
      POSTGRES_USER: odoo
      POSTGRES_PASSWORD: odoo
    volumes:
      - postgres-data:/var/lib/postgresql/data
```

## Technical Constraints

### Platform Limitations
- **Odoo Community**: Limited to community features (no enterprise modules)
- **Python Knowledge Gap**: Developer learning Python and Odoo simultaneously
- **Docker Learning Curve**: New technology for the development team
- **Resource Constraints**: Single developer with AI assistance

### Performance Requirements
- **User Load**: Support ~40 concurrent users
- **Response Time**: Sub-2 second page loads for critical operations
- **Availability**: 99% uptime during operational hours (6 AM - 6 PM)
- **Mobile Performance**: Responsive design for tablets and smartphones

### Security Constraints
- **Authentication**: Odoo's built-in user management
- **Authorization**: Role-based access control (RBAC)
- **Data Protection**: Local deployment for sensitive mining operation data
- **Backup Strategy**: Regular database backups and disaster recovery

## Dependencies

### Core Dependencies
- **Odoo Modules**:
  - `hr` (Human Resources/Employees)
  - `fleet` (Fleet Management)
  - `stock` (Inventory Management)
  - `base` (Core Odoo functionality)

### Development Dependencies
- **Docker Engine**: Container runtime
- **Docker Compose**: Multi-container management
- **PostgreSQL**: Database server
- **Python 3.8+**: Odoo runtime requirement

### External Integrations
- **CSV Import/Export**: Standard data exchange
- **REST API**: Future integration capabilities
- **Mobile Browser Support**: Chrome, Safari, Firefox mobile

## Tool Usage Patterns

### Development Workflow
1. **Claude Code**: Primary development assistant and documentation
2. **Memory Bank**: Context preservation between sessions
3. **MCP Servers**: Enhanced capabilities for documentation and integration
4. **Docker**: Consistent development and deployment environment

### Data Management
- **CSV Templates**: Structured data import for initial setup
- **Odoo Import Tools**: Built-in data import wizards
- **Database Backups**: Regular PostgreSQL dumps
- **Version Control**: Track configuration and custom module changes

### Testing Strategy
- **Manual Testing**: User acceptance testing with stakeholders
- **Browser Testing**: Cross-platform mobile and desktop compatibility
- **Performance Testing**: Load testing with expected user volumes
- **Data Integrity**: Validation of import/export processes

## Configuration Management

### Environment Variables
```bash
# Odoo Configuration
ODOO_DB_HOST=postgres
ODOO_DB_PORT=5432
ODOO_DB_USER=odoo
ODOO_DB_PASSWORD=odoo

# Application Settings
ODOO_ADMIN_PASSWORD=admin
ODOO_ADDONS_PATH=/mnt/extra-addons
```

### Custom Configurations
- **User Roles**: Custom role definitions for mining operations
- **Module Configurations**: Tailored settings for fleet and inventory
- **Dashboard Layouts**: Role-specific interface customizations
- **Workflow Rules**: Automated processes for maintenance and reporting

## Future Technical Considerations

### Scalability Planning
- **Horizontal Scaling**: Multiple Odoo instances with load balancing
- **Database Optimization**: Query optimization and indexing strategies
- **Caching Strategy**: Redis integration for improved performance
- **CDN Integration**: Static asset delivery optimization

### Integration Roadmap
- **Mobile App**: Native mobile application development
- **IoT Integration**: Equipment sensor data integration
- **Third-party APIs**: Supplier and vendor system integration
- **Advanced Analytics**: Business intelligence and reporting tools
