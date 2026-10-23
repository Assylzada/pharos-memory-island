# Pharos: Interactive Memory Island

## 1. Project Overview

Pharos is a gamified mobile application designed to help users preserve, visualize, organize, and revisit personal memories through an interactive virtual island.

Instead of presenting memories only as text entries in a conventional diary, Pharos represents them as meaningful visual elements within a personal digital environment. Users can save experiences, attach media, explore their island, and discover connections between memories.

The initial version uses transparent, rule-based scoring to suggest potentially related memories. The suggestions component is designed behind an interface so it can be replaced or extended later.

## 2. Problem Statement

Personal memories are often scattered across photographs, notes, messages, and separate applications. Conventional storage methods allow users to preserve information but may provide limited opportunities to explore memories through an engaging, connected visual environment.

Pharos addresses this problem by combining personal memory management, interactive island visualization, gamification, and rule-based suggestions for exploring related memories.

## 3. Project Goal

To design, develop, and evaluate a mobile application that transforms personal memories into an interactive virtual island and investigates how AI-assisted processing can improve the organization, discovery, and exploration of saved memories.

## 4. Project Objectives

- Review relevant research and existing applications for digital memory preservation and AI-assisted information organization.
- Identify target-user needs and define functional and non-functional requirements.
- Select appropriate technologies for cross-platform mobile development, local storage, scene rendering, and rule-based suggestions.
- Design the application architecture and user experience.
- Develop the virtual island and personal memory management module.
- Design and implement a rule-based suggestions module behind a replaceable interface.
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
- Store and retrieve memory content locally, with optional REST synchronization as a stretch goal.
- Generate rule-based suggestions using available memory metadata and user-defined signals.
- Identify potentially related memories using transparent, rule-based scoring.
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
- Local database integration and persistence.
- Media storage and retrieval.
- Rule-based memory suggestions and organization.
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

The initial implementation uses a local-first mobile architecture. The core application will run on Android and iOS from a shared codebase. Backend synchronization is optional and is considered a stretch goal.

- **Mobile application:** React Native with Expo
- **Programming language:** TypeScript with strict type checking
- **Scene rendering:** SVG and/or Skia-based 2D rendering for the virtual island
- **Interaction:** Landmark hit-testing for selecting island objects and opening memories
- **Local database:** SQLite, with versioned schema migrations
- **Media storage:** Files stored in the application's sandbox; database records reference stored media
- **Suggestions module:** Rule-based scoring behind a replaceable interface, so the implementation can be replaced later
- **Optional backend and synchronization:** Supabase (PostgreSQL, Auth, Storage) with REST-based synchronization; stretch goal only
- **Testing:** Jest for unit tests, React Native Testing Library for component tests, and Detox or Maestro for end-to-end UI tests
- **Continuous integration:** GitHub Actions
- **Version control and collaboration:** Git and GitHub
- **Task management:** YouTrack (PHA)
- **Documentation and diagrams:** Markdown documentation, Graphviz diagram sources, and Python diagram scripts where useful

The first version prioritizes reliable offline use and local persistence. Supabase synchronization and authentication are optional and are not prerequisites for the core application.

## 9. Team Members and Responsibilities

Both students work as **full-stack mobile developers**. Each contributes across the client, local data layer, testing, and integration. The focus areas below coordinate ownership without creating isolated frontend/backend or AI-only roles; both students should be able to run, understand, review, and maintain the complete application.

### 9.1. Nurbayeva Assylzada — Full-Stack Developer (Memory Organization and Suggestions)

Responsible for end-to-end implementation of memory organization features while contributing to the full application.

Responsibilities include:

- Implementing React Native (Expo) and TypeScript screens and components for creating, editing, browsing, and reviewing memories.
- Designing and implementing memory data models and SQLite persistence, including versioned migrations.
- Implementing media selection, sandbox file storage, and references between media and memory records.
- Developing the rule-based suggestions/scoring module behind a clearly defined interface, so it can be replaced later without changing the rest of the application.
- Integrating suggestions into the user interface and allowing users to review or dismiss them.
- Contributing to the virtual island scene and landmark interactions using SVG and/or Skia.
- Writing Jest unit tests and React Native Testing Library tests; contributing to Detox or Maestro end-to-end tests.
- Reviewing code, documenting design decisions, and participating in integration and release preparation.
- Contributing to optional Supabase REST synchronization if approved as a stretch goal.

**Individual focus deliverable:** An integrated, tested memory-organization workflow with SQLite persistence and a replaceable rule-based suggestions module across the mobile UI and data layer.

### 9.2. Kalzhanov Zhansultan Orazgalievich — Full-Stack Developer (Virtual Island and Local-First Architecture)

Responsible for end-to-end implementation of the virtual island and local-first application foundations while contributing to all major application layers.

Responsibilities include:

- Implementing React Native (Expo) and TypeScript screens and navigation for the virtual island and memory details.
- Developing the 2D island scene using SVG and/or Skia, including landmark hit-testing and selection behavior.
- Designing and implementing SQLite repositories, schema versioning, and database migrations in collaboration with the other developer.
- Implementing create, read, update, and delete flows for memories and connecting island objects to stored memory records.
- Implementing sandbox media-file handling and ensuring the UI and database remain consistent when media is added or removed.
- Establishing shared application architecture, typed interfaces, error handling, and performance practices for the rendering budget defined in NFR-03.
- Writing Jest and React Native Testing Library tests and contributing to Detox or Maestro end-to-end coverage.
- Configuring GitHub Actions CI for relevant checks and tests.
- Contributing to the suggestions module, code review, documentation, and optional Supabase REST synchronization if approved.

**Individual focus deliverable:** An integrated, tested virtual-island workflow with landmark hit-testing, memory details, local persistence, and documented performance and testing results.

### 9.3. Supervisor — Myrzakerimova Alua

Responsibilities include:

- Providing academic supervision and feedback.
- Reviewing project progress and technical documentation.
- Advising on research methodology and evaluation.
- Reviewing the project's alignment with academic requirements.

## 10. Collaboration and Module Integration

The project uses shared full-stack ownership with coordinated feature focus areas:

1. **Memory organization and suggestions:** Nurbayeva Assylzada leads the initial implementation of memory organization and the rule-based scoring interface.
2. **Virtual island and local-first foundations:** Kalzhanov Zhansultan leads the initial implementation of the island scene, landmark hit-testing, and core local-first architecture.
3. **Shared ownership:** Both students contribute to React Native screens, TypeScript models, SQLite persistence, media handling, testing, integration, code review, and documentation. Neither module is owned exclusively at one architectural layer.

The application should define clear interfaces between the scene, memory domain, persistence layer, media handling, and suggestion engine. SQLite is the primary source of local persistence. The suggestion engine returns recommendations through a replaceable interface, and the UI presents these suggestions for user review.

Supabase (PostgreSQL, Auth, and Storage) with REST synchronization is a stretch goal. If implemented, synchronization behavior and conflict handling must be documented and tested separately from the offline core.

## 11. Repository Structure

```
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
│   ├── components/
│   ├── features/
│   │   ├── memories/
│   │   ├── island/
│   │   └── suggestions/
│   ├── database/
│   │   └── migrations/
│   ├── storage/
│   ├── services/
│   ├── navigation/
│   └── types/
├── tests/
│   ├── unit/
│   ├── components/
│   └── e2e/
├── assets/
├── .github/
│   └── workflows/
├── .gitignore
└── README.md

```

The directory structure may evolve as implementation progresses. Secrets, API keys, passwords, and private environment files must not be committed to the repository.

## 12. Project Management and Documentation

- **GitHub repository:** [https://github.com/Assylzada/pharos-memory-island.git](https://github.com/Assylzada/pharos-memory-island.git)
- **YouTrack project:** [https://pharos-island.youtrack.cloud/projects/PHA](https://pharos-island.youtrack.cloud/projects/PHA)
- **Project proposal:** `docs/proposal/project-proposal.md`
- **Literature review:** `docs/research/literature-review.md`
- **Requirements specification:** `docs/requirements/requirements.md`
- **System architecture:** `docs/architecture/architecture.md`
- **API specification:** `docs/api/api-specification.md`
- **Evaluation plan:** `docs/evaluation/evaluation-plan.md`
- **Prototype:** To be added when available.

## 13. Development Status

**Current stage:** Project planning, requirements analysis, and initial architecture design.

**Planned milestones:**

1. Finalize the research background and project requirements.
2. Define module boundaries, data models, and API contracts.
3. Design the mobile interface and virtual island prototype.
4. Implement the core memory management workflow and database.
5. Implement and evaluate the rule-based suggestions module.
6. Integrate both modules.
7. Conduct functional, integration, performance, and suggestion-quality evaluation.
8. Complete documentation and prepare the final demonstration.

Implementation status must be updated as tasks are completed and verified. Planned functionality should not be reported as completed until it has been implemented and tested.

## 14. Setup and Execution

The exact commands and environment requirements should be finalized alongside the first runnable implementation. The intended setup flow is:

1. Install a supported Node.js LTS version and the package manager selected by the project.
2. Clone the repository and install dependencies.
3. Start the Expo development server.
4. Run the application on an Android or iOS simulator, or on a supported physical device using Expo.
5. Run the test suites and lint/type-check commands defined in `package.json`.

The README should be updated with verified commands once the Expo project and its scripts have been committed. SQLite migrations should run safely when the local database schema changes.

If the optional Supabase stretch goal is implemented, document the required environment variables and REST synchronization setup in `.env.example` and the project documentation. Never commit credentials, API keys, passwords, or private environment files.

## 15. Testing and Evaluation

The project will be evaluated through several complementary approaches:

- **Unit testing:** Jest tests for domain logic, data transformations, migrations, and rule-based suggestion scoring.
- **Component testing:** React Native Testing Library tests for memory forms, memory details, suggestion presentation, and island-related UI.
- **End-to-end UI testing:** Detox or Maestro tests for key journeys, including creating a memory, attaching media, selecting a landmark, editing a memory, and reopening saved data.
- **Persistence testing:** Verify SQLite CRUD operations, migration behavior, and data integrity across application restarts.
- **Scene interaction testing:** Verify landmark hit-testing and that selecting a landmark opens the correct memory.
- **Performance evaluation:** Measure scene responsiveness and rendering behavior against the performance budget defined in NFR-03.
- **Integration testing:** Verify interactions among the UI, scene, SQLite repositories, media storage, and suggestions interface.
- **Optional synchronization testing:** If Supabase is implemented, test REST synchronization, authentication, storage access, and conflict/error handling.
- **Usability evaluation:** Collect feedback from test users about navigation, memory organization, and the usefulness of the island-based interface.

GitHub Actions will run the automated checks supported by the repository. Specific metrics, test cases, and acceptance criteria will be defined in the evaluation plan.

## 16. Known Limitations

- Rule-based suggestions may be limited by the rules and signals available in the initial implementation.
- Date, location, and other details may be unavailable if they are not provided by the user or reliably extracted from the available content.
- AI-generated recommendations will require validation and user review.
- The initial implementation will prioritize core functionality over advanced graphics and extensive personalization.
- The quality of suggestions will depend on the scoring rules and the quality of stored memory metadata.
- Privacy, secure storage, and controlled handling of personal memories must be considered throughout development.

## 17. Expected Outcomes

The expected result is a working mobile application prototype that enables users to preserve personal memories as interactive elements on a virtual island.

The project will also deliver a replaceable rule-based suggestions module, integrated full-stack mobile features, a local SQLite persistence layer with versioned migrations, an interactive 2D island scene, and evaluation results covering core functionality, performance, suggestion relevance, and usability.