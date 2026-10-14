# Pharos: Interactive Memory Island

## 1. Project Overview

Pharos is a gamified mobile application designed to help users preserve, visualize, organize, and revisit personal memories through an interactive virtual island.

Instead of presenting memories only as text entries in a conventional diary, Pharos represents them as meaningful visual elements within a personal digital environment. Users can save experiences, attach media, explore their island, and discover connections between memories.

The project also explores the integration of machine learning and artificial intelligence to make memory organization more intelligent and personalized.

## 2. Problem Statement

Personal memories are often scattered across photographs, notes, messages, and separate applications. Conventional storage methods allow users to preserve information but may provide limited opportunities to explore memories through an engaging, connected visual environment.

Pharos addresses this problem by combining personal memory management, interactive island visualization, gamification, and AI-assisted memory processing.

## 3. Project Goal

To design, develop, and evaluate a mobile application that transforms personal memories into an interactive virtual island and investigates how AI-assisted processing can improve the organization, discovery, and exploration of saved memories.

## 4. Project Objectives

- Review relevant research and existing applications for digital memory preservation and AI-assisted information organization.
- Identify target-user needs and define functional and non-functional requirements.
- Select appropriate technologies for mobile development, backend services, data storage, and AI integration.
- Design the application architecture and user experience.
- Develop the virtual island and personal memory management module.
- Design and implement the AI/ML module for processing memory content and identifying potentially related memories.
- Integrate the application components through clearly defined interfaces.
- Test the core functionality, AI outputs, and data-handling workflows.
- Evaluate usability, reliability, and the perceived usefulness of the application.

## 5. Target Users

The initial target audience consists of individuals who want to preserve personal experiences and revisit them through a visual, interactive environment rather than relying exclusively on a conventional text-based diary.

Potential users include people who enjoy personal journaling, collecting meaningful experiences, visual storytelling, and exploring their memories over time.

## 6. Initial Feature Set

- Create, edit, view, and delete personal memories.
- Attach photographs and other supported media to memories.
- Represent memories as interactive objects within a virtual island.
- Open detailed memory information by selecting an island object.
- Store and retrieve memory content through backend services.
- Use AI to extract structured information from memory descriptions.
- Identify potentially related memories using content similarity and other suitable methods.
- Suggest connections between memories for user review.
- Support basic island progression and gamification.
- Protect personal information and provide appropriate controls over saved data.

AI-generated information and suggested connections will be treated as recommendations that users can review and correct.

The final feature set will be confirmed through requirements analysis and implementation feasibility.

## 7. Project Scope

### In Scope

- Mobile application development.
- Virtual island visualization and interaction.
- Personal memory creation and management.
- Backend API development and database integration.
- Media storage and retrieval.
- AI/ML-assisted memory processing and organization.
- Basic gamification and island progression.
- Integration testing, AI evaluation, and usability testing.
- Technical and academic documentation.

### Out of Scope for the Initial Version

- Public social networking and messaging.
- Multiplayer island interactions.
- A large-scale 3D open world.
- Augmented or virtual reality.
- Training a large language model from scratch.
- Guaranteed automatic reconstruction of incomplete or forgotten memories.
- Clinical, diagnostic, or therapeutic functionality.

## 8. Technology Stack

The following technologies are proposed for the initial implementation. Final selections may be adjusted according to feasibility testing and project requirements.

- **Mobile application:** Flutter
- **Mobile programming language:** Dart
- **Backend and REST API:** Python with FastAPI
- **Database:** PostgreSQL
- **Database and authentication services:** Supabase, if confirmed during implementation
- **AI/ML development:** Python and suitable machine learning or language-model libraries/APIs
- **Media storage:** Supabase Storage or another compatible object-storage solution
- **Virtual island rendering:** Flutter-based 2D rendering and animations
- **Version control:** Git and GitHub
- **Task management:** YouTrack
- **Containerization:** Docker
- **Testing:** Pytest for Python services, plus appropriate Flutter testing tools
- **UI/UX design:** To be selected and documented during the design phase

## 9. Team Members and Responsibilities

### 9.1. Nurbayeva Assylzada — AI/ML Module

Responsible for the design, development, and evaluation of the AI/ML component of Pharos.

Responsibilities include:

- Researching and selecting suitable AI/ML approaches for personal memory processing.
- Designing the AI/ML module architecture and its integration with the backend.
- Developing functionality to extract structured information from user-provided memory descriptions, such as entities, locations, dates, topics, and relevant keywords, where available.
- Implementing methods for identifying potentially related memories using semantic similarity, embeddings, or other suitable approaches.
- Developing AI-assisted recommendations for organizing memories and suggesting connections between them.
- Designing prompts, processing pipelines, and validation mechanisms for AI-generated results, where applicable.
- Evaluating the quality, relevance, and consistency of AI-generated outputs using a defined testing methodology.
- Documenting the ML/AI approach, experiments, limitations, and evaluation results.
- Collaborating with the full-stack developer to define API contracts and integrate the AI/ML component into the application.

**Individual deliverable:** A functional AI/ML module that processes memory descriptions, produces structured memory information, and identifies potentially related memories, together with documented integration interfaces and evaluation results.

The initial implementation will focus on feasible, measurable functionality rather than training a custom large language model from scratch.

### 9.2. Kalzhanov Zhansultan Orazgalievich — Full-Stack Development of the Virtual Island and Memories Module

Responsible for the full-stack development of the virtual island and memory management module.

Responsibilities include:

- Designing and implementing the mobile client interface for the virtual island and memory timeline.
- Developing interactive island visualization and the presentation of memory objects.
- Implementing backend services using Python and FastAPI for uploading, processing, retrieving, and storing media files and geolocation metadata.
- Designing the PostgreSQL database schema for structured storage and representation of personal memories.
- Implementing the backend functionality required to create, retrieve, update, and delete memories.
- Connecting the mobile client to the backend services.
- Integrating the island visualization with stored memory records.
- Containerizing relevant application components using Docker.
- Testing the core full-stack memory management workflow and documenting the implementation.

**Individual deliverable:** An end-to-end module consisting of the mobile client, backend services, and configured PostgreSQL database for representing, storing, retrieving, and visualizing memories on the virtual island.

### 9.3. Supervisor — Myrzakerimova Alua

Responsibilities include:

- Providing academic supervision and feedback.
- Reviewing project progress and technical documentation.
- Advising on research methodology and evaluation.
- Reviewing the project's alignment with academic requirements.

## 10. Collaboration and Module Integration

The project is divided into two main technical areas:

1. **Virtual Island and Memories Module:** Developed by Kalzhanov Zhansultan. It provides the mobile interface, memory persistence, media handling, database integration, and island visualization.
2. **AI/ML Module:** Developed by Nurbayeva Assylzada. It processes memory descriptions, generates structured information, and identifies potentially related memories.

The modules will communicate through documented API contracts. The AI/ML module will receive the necessary memory content and return structured results or suggested connections. The full-stack module will manage persistence, present the results to users, and allow users to review or modify suggestions.

The final integration approach will be documented in the architecture and API specifications.

## 11. Repository Structure

```text
pharos-memory-island/
├── docs/
│   ├── proposal/
│   │   └── project-proposal.md
│   ├── research/
│   │   └── literature-review.md
│   ├── requirements/
│   │   └── requirements.md
│   ├── architecture/
│   │   └── architecture.md
│   ├── api/
│   │   └── api-specification.md
│   └── evaluation/
│       └── evaluation-plan.md
├── diagrams/
├── prototype/
├── src/
│   ├── mobile/
│   ├── backend/
│   └── ai-ml/
├── tests/
├── config/
│   └── .env.example
├── .gitignore
└── README.md
```

The directory structure may evolve as implementation progresses. Secrets, API keys, passwords, and private environment files must not be committed to the repository.

## 12. Project Management and Documentation

- **GitHub repository:** https://github.com/Assylzada/pharos-memory-island.git
- **YouTrack project:** https://pharos-island.youtrack.cloud/projects/PHA
- **Project proposal:** `docs/proposal/project-proposal.md`
- **Literature review:** `docs/research/literature-review.md`
- **Requirements specification:** `docs/requirements/requirements.md`
- **System architecture:** `docs/architecture/architecture.md`
- **API specification:** `docs/api/api-specification.md`
- **Evaluation plan:** `docs/evaluation/evaluation-plan.md`
- **Prototype:** To be added when available.

## 13. Development Status

**Current stage:** Project planning, requirements analysis, and initial architecture design.

**Planned milestones:**

1. Finalize the research background and project requirements.
2. Define module boundaries, data models, and API contracts.
3. Design the mobile interface and virtual island prototype.
4. Implement the core memory management workflow and database.
5. Develop the AI/ML processing and memory-connection functionality.
6. Integrate both modules.
7. Conduct functional, integration, and AI/ML evaluation.
8. Complete documentation and prepare the final demonstration.

Implementation status must be updated as tasks are completed and verified. Planned functionality should not be reported as completed until it has been implemented and tested.

## 14. Setup and Execution

Setup and execution instructions will be added when the first runnable implementation is available.

The final instructions will document:

- Required software and dependencies.
- Repository cloning and environment setup.
- Environment variable configuration.
- Database setup and migrations.
- Backend startup.
- Mobile application startup.
- AI/ML module configuration and startup, if deployed separately.
- Instructions for running tests.

API keys and other credentials must be configured through environment variables and must never be included directly in source code.

## 15. Testing and Evaluation

The project will be evaluated through several complementary approaches:

- **Functional testing:** Verify memory creation, editing, deletion, retrieval, and island-object interaction.
- **API testing:** Verify request validation, responses, error handling, and integration between modules.
- **Database testing:** Verify data persistence and relationships between stored records.
- **AI/ML evaluation:** Assess the correctness of extracted information and the relevance of suggested memory connections using a documented test dataset and evaluation criteria.
- **Integration testing:** Verify communication between the mobile client, backend, database, and AI/ML module.
- **Usability evaluation:** Collect feedback from test users about navigation, memory organization, and the usefulness of the island-based interface.

Specific metrics, test cases, and acceptance criteria will be defined in the evaluation plan.

## 16. Known Limitations

- AI-generated metadata and memory connections may be incomplete or incorrect.
- Date, location, and other details may be unavailable if they are not provided by the user or reliably extracted from the available content.
- AI-generated recommendations will require validation and user review.
- The initial implementation will prioritize core functionality over advanced graphics and extensive personalization.
- The quality of AI/ML results will depend on the selected models, available resources, and evaluation data.
- Privacy, secure storage, and controlled handling of personal memories must be considered throughout development.

## 17. Expected Outcomes

The expected result is a working mobile application prototype that enables users to preserve personal memories as interactive elements on a virtual island.

The project will also deliver a documented AI/ML module for structuring memory content and suggesting relationships between memories, a working full-stack memory management module, an integrated application architecture, and evaluation results covering core functionality, AI/ML output quality, and usability.
