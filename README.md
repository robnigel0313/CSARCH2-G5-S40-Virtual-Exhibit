# ☁️ Cloud Vault: The Architecture Behind Cloud Storage

## Authors

- CO, Caitlyn Hope
- DE LA CALZADA, Wanda Jude
- LI, Bowen
- RODRIGO, Betina Heart
- ROGACION, Rob Nigel

---
*MID-MILESTONE DOCUMENTATION*

---

# Website Deployment
**Live URL:** https://robnigel0313.github.io/CSARCH2-G5-S40-Virtual-Exhibit/

# Challenges Faced
### Astro Integration & Deployment
- Navigated versioning conflicts when upgrading the template environment to Astro 6. This was solved by using the `--legacy-peer-deps` flag to bypass the strict requirements of the outdated `package-lock.json` file.
- Encountered production build crashes because `const` declarations were placed above `import` statements in the Astro frontmatter of the provided template.
- Discovered that mixing Astro's native `Astro.glob()` function with MDX pages causes a compilation bug (`Astro2.glob is not a function`) during the production build. Addressed the problem by swapping Astro's function for Vite's native `import.meta.glob` to successfully bypass the compiler error and deploy the site.

---
*PROJECT PROPOSAL*

---

# Topic Theme

## How Cloud Storage Works: The Architecture Behind Cloud Storage

Cloud storage services such as **Google Drive**, **Dropbox**, **OneDrive**, and **iCloud** allow users to access files from anywhere with an internet connection.

While the process appears simple from the user's perspective, cloud storage relies on a large-scale architecture composed of:

- Client devices
- Communication networks
- Servers
- Storage systems
- Data centers

This exhibit explores the complete journey of a file after it is uploaded to the cloud. Visitors will learn:

- How files travel through the Internet
- How cloud servers receive and process requests
- How data is stored inside data centers
- How replication mechanisms provide fault tolerance and reliability

The exhibit also explains:

- Synchronization between multiple devices
- User authentication
- Encryption techniques
- Redundancy strategies used by cloud providers

By connecting cloud storage concepts to underlying computer architecture components such as servers, storage arrays, distributed systems, and data center infrastructure, the exhibit demonstrates how modern computing systems manage data at scale.

---

# Main Exhibit Sections

## Section 1 — What is Cloud Storage?

- Definition of cloud storage
- Difference between local storage and cloud storage
- Examples of cloud storage services
- Why cloud storage became important

---

## Section 2 — Uploading a File

- User initiates upload
- File segmentation into data packets
- Network transmission
- Request handling by cloud servers

---

## Section 3 — Cloud Servers and Data Centers

- What happens when a file reaches a server
- Physical servers and storage devices
- Data center architecture
- Distributed storage systems

---

## Section 4 — Replication and Redundancy

- Creation of backup copies
- Multiple server locations
- Fault tolerance
- High availability

---

## Section 5 — Synchronization Across Devices

- Updating files across devices
- Version control concepts
- Real-time synchronization

---

## Section 6 — Security and Encryption

- Authentication
- Access control
- Encryption in transit
- Encryption at rest

---

## Section 7 — Why Cloud Storage Works

- Summary of the complete architecture
- Key takeaways
- Modern cloud storage challenges

---

# Group Tech Stack Plan

The project will be developed using the provided **Astro Museum Template** and follow all required software versions.

## Frameworks and Technologies

| Technology | Version |
|------------|---------|
| Astro | 6 |
| React | JSX Components |
| MDX | Latest |
| CSS Modules | Supported |
| Node.js | 26 |

---

## Repository Structure

```text
src/
├── components/
│   ├── CloudJourneySimulator.jsx
│   ├── ArchitectureDiagram.jsx
│   └── CloudQuiz.jsx
│
├── layouts/
│   └── ExhibitLayout.astro
│
├── pages/
│   └── cloud-storage.mdx
│
└── assets/
    ├── images/
    └── icons/
```

---

## Content Integration

The exhibit content will be written in **MDX** to allow React components to be embedded directly inside explanatory sections.

This approach ensures compatibility with the central museum website while maintaining interactivity.

---

# Proposed Interactive Element

## Follow the File: Cloud Storage Journey Simulator

### Purpose

The simulator allows visitors to visualize the complete lifecycle of a file after upload.

---

## User Flow

### Stage 1 — Upload

**Interaction**

- Visitor presses an **Upload** button.
- A file icon appears beside a laptop illustration.

**Explanation**

> "Your device prepares the file for transmission to cloud servers."

---

### Stage 2 — Network Transmission

**Interaction**

- Animated packets travel through network pathways.

**Explanation**

> "The file is divided into packets and transmitted through the Internet."

---

### Stage 3 — Cloud Server Processing

**Interaction**

- Packets arrive at a cloud server.

**Explanation**

> "The cloud server authenticates the user and processes the upload request."

---

### Stage 4 — Storage

**Interaction**

- File is stored in a primary storage node.

**Explanation**

> "The uploaded file is written into distributed storage infrastructure."

---

### Stage 5 — Replication

**Interaction**

- Additional copies are generated.

**Explanation**

> "Replication creates redundant copies to prevent data loss."

---

### Stage 6 — Synchronization

**Interaction**

- Additional devices receive updated versions.

**Explanation**

> "Changes are synchronized across connected devices."

---

## Technical Implementation

The simulator will be implemented as a React component.

### Features

- State-based progression
- Animated transitions
- Interactive buttons
- Step indicators
- Reset functionality
- Educational tooltips

### Deployment Notes

No backend services are required.

All interactions are:

- Client-side
- Static-site compatible
- Fully deployable through Astro

---

# Additional Interactive Element

## Cloud Storage Knowledge Check

At the end of the exhibit, visitors may answer a short quiz consisting of **five multiple-choice questions**.

### Example Questions

1. Why is replication important?
2. What is a data center?
3. What does synchronization do?
4. What is encryption?
5. What happens after a file is uploaded?

### Features

- Immediate feedback
- Educational explanations
- Lightweight client-side implementation

---

# Desktop and Mobile Responsive Layout Plan

The exhibit will be designed to work properly on both desktop and mobile screens while following the museum website template.

---

## Desktop Layout

A spacious **two-column layout**.

### Left Column

- Main explanations
- Definitions
- Step-by-step descriptions
- Key takeaways

### Right Column

- Diagrams
- Server illustrations
- Interactive animations
- Architecture visuals

The **Cloud Storage Journey Simulator** will occupy a dedicated full-width section.

---

## Mobile Layout

A **single-column layout** optimized for smaller screens.

### Mobile Adjustments

- Text and visuals stacked vertically
- Simulator resized proportionally
- Larger tap targets
- Shorter text blocks
- Scaled diagrams
- Card-based section arrangement
- Reduced animation sizes
- Improved spacing

---

## Responsive Behavior

| Device | Layout |
|--------|--------|
| Desktop | Two-column |
| Mobile | Single-column |

This ensures readability and usability across laptops and smartphones.

---

# Tentative Style Guide Snapshot

## Design Theme

**Modern Data Center / Cloud Infrastructure**

---

## Color Palette

| Element | Color |
|---------|-------|
| Primary Background | `#0F172A` |
| Secondary Background | `#1E293B` |
| Accent Blue | `#38BDF8` |
| Accent Cyan | `#22D3EE` |
| Success Green | `#22C55E` |
| Text | `#F8FAFC` |

---

## Typography

| Usage | Font |
|-------|------|
| Headings | Inter Bold |
| Body Text | Inter Regular |
| Technical Labels | JetBrains Mono |

---

## Visual Elements

- Cloud icons
- Server rack illustrations
- Data center diagrams
- Network packet animations
- Storage node graphics
- Device synchronization visuals

---

## Visual Inspiration

The exhibit should resemble a guided tour through a modern cloud data center, allowing visitors to follow a file's journey from a personal device to distributed cloud infrastructure.

---

# Expected Learning Outcomes

After completing the exhibit, visitors should be able to:

- Explain the purpose of cloud storage.
- Describe how files travel from a device to cloud servers.
- Identify the role of data centers in cloud storage.
- Explain replication and redundancy.
- Understand synchronization across devices.
- Recognize the importance of encryption and authentication.
- Relate cloud storage services to underlying computer architecture components.

---

## Project Goal

> To provide visitors with an engaging and technically accurate understanding of how cloud storage systems function, connecting everyday cloud services with the computer architecture principles that make them possible.