# Pixonomy
_A flexible and efficient image management system._

## Overview
Pixonomy is a powerful, modular image management software designed for organizing, tagging, and browsing large image collections. It features:

- **Customizable tagging and metadata storage**
- **Platform-native applications** for desktop and mobile
- **Plugin-based architecture** for extensibility and user customizability
- **AI-assisted tagging** with manual review

## Project Structure
This repository consists of multiple submodules:

- **[`core`](https://github.com/Pixonomy/pixonomy-core)** - The backend logic and data processing layer.
- **[`desktop`](https://github.com/Pixonomy/pixonomy-desktop)** - The graphical user interface (GUI) for Pixonomy.
- **[`plugins/webserver`](https://github.com/Pixonomy/pixonomy-plugins-webserver)** - A plugin for a web interface.
- **[`plugins/self-sync`](https://github.com/Pixonomy/pixonomy-plugins-self-sync)** - A plugin for self-hosted, direct device-to-device syncing without cloud services.
- **[`plugins/cloud-sync`](https://github.com/Pixonomy/pixonomy-plugins-cloud-sync)** - A plugin for integrating with cloud services such as dropbox.

## Getting Started
To clone Pixonomy with all submodules, run the following:
```sh
git clone --recurse-submodules git@github.com:Pixonomy/pixonomy.git
cd pixonomy
```

For more detailed installation and compilation steps, see the **[Installation Guide](docs/installation.md)**

For full documentation, including requirements, architecture, and the plugin system, see the **[Documentation Index](docs/README.md)**

## License
Pixonomy is released under open-source licenses to ensure long-term transparency and collaboration:

- **Documentation**: Licensed under **Creative Commons**. See [LICENSE](docs/LICENSE) for details.
- **Core Repository**: Licensed under **AGPLv3**, requiring that any modifications, even those deployed as a network service, remain open-source.
- **Desktop Application**: Licensed under **GPLv3**, ensuring all distributed modifications remain open-source while complying with Qt’s licensing requirements.
- **Plugins**: Individual plugins may specify their own licenses, but **must be compatible** with the Pixonomy core’s AGPLv3 license when integrating.

By contributing to this project, you agree to license your contributions under the respective licenses of the affected components.
