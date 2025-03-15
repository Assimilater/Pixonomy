# Pixonomy Architecture

## Overview
Pixonomy is structured as a **multi-repository project** to keep components modular and independent. This allows each major part of the system to be developed and licensed separately while maintaining clear integration points.

## Repository Structure
The Pixonomy project is split into multiple repositories:

### **1. Core (`pixonomy-core`)**
**Location:** [`core/`](https://github.com/Pixonomy/pixonomy-core)
**Purpose:**
- The **backend engine** responsible for metadata storage, image indexing, and tagging logic.
- Acts as the **central processing hub** that other components interact with.

### **2. Desktop Application (`pixonomy-desktop`)**
**Location:** [`desktop/`](https://github.com/Pixonomy/pixonomy-desktop)
**Purpose:**
- Provides a **native GUI** for managing images.
- Communicates with `core` to retrieve and manipulate image metadata.
- Implements **OS-native features** for a seamless user experience.

### **3. Plugins (`pixonomy-plugins-*`)**
**Location:** `plugins/`
**Purpose:**
- Plugins extend Pixonomy’s functionality without modifying the core.
- Each plugin is developed as a separate repository.

#### **Current Plugins**
| Plugin Name | Repository | Purpose |
|-------------|------------|---------|
| **Web Interface** | [`plugins/webserver`](https://github.com/Pixonomy/pixonomy-plugins-webserver) | Enables remote access and management via a web UI. |
| **Self-Hosted Sync** | [`plugins/self-sync`](https://github.com/Pixonomy/pixonomy-plugins-self-sync) | Provides device-to-device sync without relying on cloud services. |
| **Cloud Sync** | [`plugins/cloud-sync`](https://github.com/Pixonomy/pixonomy-plugins-cloud-sync) | Integrates with third-party cloud services such as Dropbox and Google Drive. |

### **4. Mobile Applications (Future)**
**Planned repositories:** `pixonomy-mobile-ios`, `pixonomy-mobile-android`
**Purpose:**
- Native mobile applications for iOS and Android.
- Will integrate with `core` for browsing and organizing images on mobile.

## Folder Structure Within the Main Repository
📌 **If you are working in the main `pixonomy` repository**, here’s how it is structured:
```
pixonomy/
│── core/                      # Backend logic and metadata management
│── desktop/                   # Desktop GUI application
│── plugins/                   # Plugin folder (contains submodules)
│   ├── webserver/             # Web-based UI for remote access
│   ├── self-sync/             # Self-hosted device-to-device sync
│   ├── cloud-sync/            # Cloud integration (Dropbox, Google Drive, etc.)
│── docs/                      # Documentation
│── README.md                  # Project overview
```

## Development Approach
- **The core repository (`core/`) is the foundation**: All other components interact with it.
- **Plugins are separate repositories** but are included as **submodules** in the `plugins/` directory.
- **The desktop and mobile apps will be native** rather than a shared cross-platform framework.

## Conclusion
Pixonomy is designed to be **modular, extensible, and independent**, allowing for future expansion with additional plugins and integrations.

For detailed documentation on development setup and APIs, refer to the **[Documentation Index](README.md)**.
