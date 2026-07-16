# Ansible Collection - eclipse.slm

## Summary

This is an Ansible collection named `eclipse.slm` (version 1.0.0) designed to manage the Eclipse SLM (Service Lifecycle Manager) application deployment and lifecycle.

### Structure

- **Namespace:** `eclipse`
- **Name:** `slm`
- **License:** GPL-2.0-or-later
- **Minimum Ansible Version:** 2.2

### Main Components

1. **`env` Role** - The primary role in this collection that:
   - Reads environment variables (`SLM_VERSION`, `SLM_HOSTNAME`, `SLM_IP`, `INSTALL_DIRECTORY`)
   - Validates required inputs using Ansible's assert module
   - Supports custom configuration via optional `env.custom.yml` and `env.override.yml` files
   - Configures Docker Compose settings including Traefik reverse proxy, SLM catalog service, and user management
   - Manages Docker image registries and logging configuration

2. **Playbooks:**
   - `install.yml` - Placeholder for SLM installation (currently incomplete)
   - `uninstall.yml` - Placeholder for SLM removal (currently incomplete)

3. **Testing Infrastructure:**
   - Uses **Molecule** with **Docker** for integration testing
   - Tests run on Ubuntu 24.04 container
   - Configured with environment variables for testing (hostname, IP, version)

### Current Status

The collection is in early development (v1.0.0) with the core `env` role implemented, but the main installation and uninstallation playbooks are still TODO placeholders.
