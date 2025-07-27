# Memory Bank - Grupo Minero La Fundición ERP Project

## Overview

This memory bank contains comprehensive documentation for the Odoo-based ERP implementation project for Grupo Minero La Fundición, a mining company seeking to optimize fleet management, maintenance coordination, and inventory control.

## File Structure

### Core Documentation (Required by Cline)
- **`projectBrief.md`** - Foundation document defining project scope, users, and technical requirements
- **`productContext.md`** - Business context, problems solved, and success vision
- **`systemPatterns.md`** - Technical architecture, design patterns, and implementation paths
- **`techContext.md`** - Technologies, development setup, dependencies, and constraints
- **`activeContext.md`** - Current work focus, recent changes, next steps, and session context
- **`progress.md`** - Detailed project progress, research decisions, and implementation status

### Additional Context
- **`prd-odoo.md`** - Comprehensive Product Requirements Document (Odoo-focused)
- **`prd.md`** - Alternative PRD with dashboard collaboration focus
- **`.clinerules`** - Memory bank structure and workflow guidelines for Cline

## Project Status

**Current Phase**: Planning and Initial Data Setup
**Timeline**: 12-week implementation in 3 phases
**Platform**: Odoo Community 18.0 with Docker deployment

### Key Accomplishments
✅ Platform selection (Odoo vs. custom development)
✅ Docker environment setup and testing
✅ MCP servers configuration for enhanced AI capabilities
✅ Employee data import methodology established
✅ Comprehensive documentation structure created

### Immediate Priorities
🔄 Define organizational structure and role hierarchy
🔄 Complete employee CSV import process
🔄 Configure fleet module with vehicle registration
🔄 Set up inventory module with spare parts catalog

## Quick Reference

### Target Users
- **40 total employees** across operations, maintenance, administration
- **Primary modules**: HR/Employees, Fleet Management, Inventory Control
- **Key roles**: Operators, Mechanics, Supervisors, Administrative Staff

### Success Metrics
- **≥80% fleet availability**
- **25% reduction in maintenance time**
- **98% inventory accuracy**
- **100% user adoption within 3 months**

### Technical Stack
- **Platform**: Odoo Community 18.0
- **Database**: PostgreSQL
- **Deployment**: Docker + Docker Compose
- **Development**: Python with AI assistance (Claude Code/Cline)
- **Data Import**: CSV-based templates

## For New Sessions

When starting a new session, Cline should:
1. Read ALL memory bank files to understand project context
2. Review `activeContext.md` for current work focus and blockers
3. Check `progress.md` for latest implementation status
4. Refer to `systemPatterns.md` and `techContext.md` for technical decisions

## Contact & Resources

- **Project Location**: `/home/elduke/MyCodingWorkspaces/Claude Commander`
- **Odoo Instance**: `\\wsl.localhost\Ubuntu-22.04\home\elduke\MyCodingWorkspaces\odoo-18-docker-compose`
- **Data Import Guide**: `../db_init/user_initialization_guide.md`
- **MCP Servers**: Context7 (Odoo docs), mcp-odoo, whatsapp-mcp, Google Drive MCP

---

*Last Updated: January 26, 2025*
*Memory Bank Version: 1.0*
