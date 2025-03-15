# Image Management Software Requirements

## Core Objective

To create software that makes organizing and finding images in a personal library easy.

---

## Key Features & Design Priorities

### 1. Image Organization

- **Tagging System:**
  - Many-to-Many Relationship – A single image can have multiple tags, and vice versa.
  - Users can apply custom tags to images for better organization.
  - **Hierarchical Tagging:** Support nested or structured categories, allowing tags to be grouped (e.g., 'Anime/One Piece' where 'One Piece' is a sub-tag of 'Anime').

- **AI-Assisted Tagging Suggestions:**
  - AI can suggest tags, but all tag assignments must be **manually confirmed** by the user before being applied.
  - AI should **learn from manual user corrections** over time.
  - AI must be able to **distinguish multiple characters** in an image, similar to facial recognition but for non-human/anime characters.
  - **Batch Review Mode:** Users can confirm/correct multiple AI-generated tag suggestions at once.
  - **Tag Blacklist:** Users can maintain a stored blacklist of tags, preventing the AI from repeatedly suggesting tags they have explicitly denied.

- **Metadata Viewing & Editing:** Allow users to see and edit image metadata with clear differentiation between metadata fields.

- **Customizable In-Database Metadata Fields:** Users can define what metadata fields to store in the database, allowing flexibility for different use cases (e.g., Pixiv links for artists, geolocation for photographers).

- **Database for Tags & Source Info:** Store tags and external source information (e.g., Pixiv links) in a database rather than embedding them in metadata.

### 2. Image Search & Filtering

- **Fast Search Engine:** Find images by filename, tags, metadata, or content.
- **Advanced Filtering:** Filter by date, file type, resolution, aspect ratio, etc.
- **Boolean Operators:** Enable searches like "tag1 AND tag2 NOT tag3" for precision.

### 3. Image Management & Viewing Tools

- **Batch Tagging & Editing:** Modify metadata and tags for multiple images at once.
- **Smart Grouping:** Automatically suggest collections based on usage patterns.
- **Integrated Image Viewer:**
  - Support both a **tabular details view** and a **thumbnail grid view** with an adjustable icon size slider.
  - **Preview Pane:** Toggleable preview pane with **zoom and pan functionality** for quick image inspection.
  - **Rotation & Cropping:** Built-in tools for rotating and cropping images.
  - **External Editor Support:** Provide an option to open images in external editors (e.g., GIMP).

### 4. Cross-Device Usability & OS Integration

- **Local-Only Storage:** No enforced cloud dependency.
- **Responsive UI:** Optimized for both desktop and mobile usage. Each targeted platform should have a native feel.
- **Lightweight & Efficient:** Prioritizes speed and efficiency to ensure **responsiveness**, even on minimal hardware.
- **Keyboard Shortcuts & Customizable UI:** Efficient navigation for power users.
- **Operating System Interoperability:** Enable drag-and-drop functionality so images behave as expected when dragged into web browsers, Discord, and other applications, similar to Windows Explorer.

### 5. Extensibility & Data Integrity

- **Non-Destructive Editing:** Changes should be reversible, avoiding data loss.
- **Plugin System or API:** Allow for third-party extensions or custom scripts.
- **Optional AI Features:** AI-assisted tagging and related functionalities should be **opt-in**, potentially handled through the plugin system.
- **Portable & Open Data Formats:** Use standard formats like JSON, SQLite, or open-source database structures.

### 6. User Customization & Simplicity

- **Extensive User Settings:** Allow deep customization of functionality and UI preferences.
- **Customizable Layout:** Users can toggle, reposition, and configure UI elements like sidebars to fit their workflow.
- **Avoiding Complexity Overload:** Ensure that settings remain **clear and intuitive**, avoiding excessive acronyms or overwhelming options.
- **Guided Setup & Explanations:** Provide tooltips, onboarding, or descriptions for settings to help users make informed choices.

---

## Challenges to Address

- **Handling large image libraries efficiently.**
- **Ensuring fast searches without excessive indexing overhead.**
- **Designing a UI that balances power-user needs with simplicity.**
- **Providing robust customization without making the software confusing to use.**
- **Guaranteeing speed and responsiveness without unnecessary resource consumption.**
- **Minimum Hardware Target:** The proposed minimum hardware requirements serve as a **loose goal** rather than a strict target, as there is no currently available machine to verify a true "minimum viable" system. The rough performance target is based on older hardware, ideally running on at least a **1st Gen Intel Core i-series processor** (or equivalent AMD CPU), **2GB RAM**, and **minimal disk footprint (~50MB or less)**. AI features may require higher specifications and are **optional** to maintain lightweight performance. The software should be capable of running on **Windows 7 or later** (or Linux/macOS equivalents). The goal is to keep the software efficient without prematurely defining a rigid hardware floor.
