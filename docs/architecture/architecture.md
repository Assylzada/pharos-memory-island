Pharos - Application Architecture and Data Model

1. Purpose

This document describes the proposed system architecture and data model for the Pharos mobile application. Pharos is designed to help users preserve personal memories and explore them through an interactive virtual island.

The architecture is a design proposal. Implementation details may change during development.

2. Main Application Components

2.1 Presentation Layer

The presentation layer is the user-facing part of the application, planned with Flutter and Dart.

Memory Management UI: allows users to create, view, edit, and delete personal memories.
Interactive Virtual Island: visualizes memories as objects in a virtual environment.
Validation and User Feedback: provides input validation and communicates the results of user actions.
2.2 Application Layer

The application layer is planned as a Python backend using FastAPI.

FastAPI REST API: receives requests from the mobile application and returns responses.
Request Validation: checks incoming data before processing.
Memory Management Logic: handles memory-related operations.
Island Object Logic: manages the relationship between memories and their virtual island representations.
Data Access Layer: handles communication between application logic and the database.
2.3 Data Storage Layer

PostgreSQL is the proposed relational database. It stores memory records, island object information, and metadata for optional media attachments.

2.4 Optional AI/ML Integration

An AI/ML module may provide memory suggestions in a future development stage. This integration is optional and is not considered a confirmed MVP feature.

3. Component Interactions

The user interacts with the Flutter mobile application.
The mobile application sends requests to the FastAPI backend through an HTTPS REST API using JSON.
The backend validates incoming requests and passes them to the appropriate application service.
The application services use the data access layer to read or write information in PostgreSQL.
The backend returns a response to the mobile application, which updates the interface and provides feedback to the user.
The optional AI/ML integration may be connected to the application logic in a later stage.

4. Proposed Memory Data Model

4.1 Memory

Represents a personal memory created by the user.

id - unique identifier.
title - memory title.
content - memory description or text.
memory_date - date associated with the memory.
created_at - record creation timestamp.
updated_at - last update timestamp.
4.2 IslandObject

Represents the virtual island object associated with a memory.

id - unique identifier.
memory_id - reference to the associated memory.
object_type - type of virtual object.
position_x - horizontal position.
position_y - vertical position.
position_z - depth position.
4.3 MediaAttachment

Represents optional media associated with a memory.

id - unique identifier.
memory_id - reference to the associated memory.
file_name - original or display file name.
media_type - type of media.
storage_path - location or reference to the stored file.
uploaded_at - upload timestamp.
5. Entity Relationships

The proposed data model defines these relationships:

Each Memory is associated with one IslandObject.
One Memory may have zero or more MediaAttachment records.
Each IslandObject belongs to one Memory.
Each MediaAttachment belongs to one Memory.
These relationships are design assumptions and should be confirmed against the final application requirements.

6. Architecture and Data Model Diagrams

The editable Mermaid diagram source files are stored in docs/diagrams/.

System Context Diagram
Use Case Diagram
Component Architecture Diagram
Data Model / ER Diagram
The context diagram shows the system boundary and external interactions. The use case diagram describes user activities. The component diagram describes the main application layers and their interactions. The ER diagram describes the proposed data entities and relationships.

7. Design Status and Open Decisions

This document describes the proposed architecture, not a verified implementation.

The following decisions remain subject to confirmation:

Final authentication and user-account requirements.
Media file storage location and upload limits.
Whether AI/ML suggestions will be included in the MVP.
Final virtual island object types and positioning rules.
Whether one memory should always correspond to exactly one island object.
The architecture and data model should be updated if these decisions change.
