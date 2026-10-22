**Pharos - Application Architecture and Data Model**

1\. Purpose

This document describes the proposed system architecture and data model for the Pharos mobile application. Pharos is designed to help users preserve personal memories and explore them through an interactive virtual island.

The architecture is a design proposal. Implementation details may change during development.

2\. Main Application Components

2.1 Presentation Layer

The presentation layer is the user-facing part of the application, planned with Flutter and Dart.

1. Memory Management UI: allows users to create, view, edit, and delete personal memories.
2. Interactive Virtual Island: visualizes memories as objects in a virtual environment.
3. Validation and User Feedback: provides input validation and communicates the results of user actions.

2.2 Application Layer

The application layer is planned as a Python backend using FastAPI.

1. FastAPI REST API: receives requests from the mobile application and returns responses.
2. Request Validation: checks incoming data before processing.
3. Memory Management Logic: handles memory-related operations.
4. Island Object Logic: manages the relationship between memories and their virtual island representations.
5. Data Access Layer: handles communication between application logic and the database.

2.3 Data Storage Layer

PostgreSQL is the proposed relational database. It stores memory records, island object information, and metadata for optional media attachments.

2.4 Optional AI/ML Integration

An AI/ML module may provide memory suggestions in a future development stage. This integration is optional and is not considered a confirmed MVP feature.

3\. Component Interactions

1. The user interacts with the Flutter mobile application.
2. The mobile application sends requests to the FastAPI backend through an HTTPS REST API using JSON.
3. The backend validates incoming requests and passes them to the appropriate application service.
4. The application services use the data access layer to read or write information in PostgreSQL.
5. The backend returns a response to the mobile application, which updates the interface and provides feedback to the user.

The optional AI/ML integration may be connected to the application logic in a later stage.

4\. Proposed Memory Data Model

4.1 Memory

Represents a personal memory created by the user.

1. id - unique identifier.
2. title - memory title.
3. content - memory description or text.
4. memory_date - date associated with the memory.
5. created_at - record creation timestamp.
6. updated_at - last update timestamp.

4.2 IslandObject

Represents the virtual island object associated with a memory.

1. id - unique identifier.
2. memory_id - reference to the associated memory.
3. object_type - type of virtual object.
4. position_x - horizontal position.
5. position_y - vertical position.
6. position_z - depth position.

4.3 MediaAttachment

Represents optional media associated with a memory.

1. id - unique identifier.
2. memory_id - reference to the associated memory.
3. file_name - original or display file name.
4. media_type - type of media.
5. storage_path - location or reference to the stored file.
6. uploaded_at - upload timestamp.

5\. Entity Relationships

The proposed data model defines these relationships:

1. Each Memory is associated with one IslandObject.
2. One Memory may have zero or more MediaAttachment records.
3. Each IslandObject belongs to one Memory.
4. Each MediaAttachment belongs to one Memory.

These relationships are design assumptions and should be confirmed against the final application requirements.

6\. Architecture and Data Model Diagrams

The editable Mermaid diagram source files are stored in `docs/diagrams/`.

1. [System Context Diagram](diagrams/system-context.mmd)
2. [Use Case Diagram](diagrams/use-case.mmd)
3. [Component Architecture Diagram](diagrams/system-architecture.mmd)
4. [Data Model / ER Diagram](diagrams/data-model.mmd)

The context diagram shows the system boundary and external interactions. The use case diagram describes user activities. The component diagram describes the main application layers and their interactions. The ER diagram describes the proposed data entities and relationships.

7\. Design Status and Open Decisions

This document describes the proposed architecture, not a verified implementation.

The following decisions remain subject to confirmation:

1. Final authentication and user-account requirements.
2. Media file storage location and upload limits.
3. Whether AI/ML suggestions will be included in the MVP.
4. Final virtual island object types and positioning rules.
5. Whether one memory should always correspond to exactly one island object.

The architecture and data model should be updated if these decisions change.
