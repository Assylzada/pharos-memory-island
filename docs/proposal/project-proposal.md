Pharos: Design and Development of a Gamified Mobile Application for Visualizing and Preserving Personal Memories Through an Interactive Virtual Island



1\. Project Overview



Pharos is a gamified mobile application designed to help users preserve, organize, visualize, and revisit personal memories through an interactive virtual island.



Unlike conventional diary applications that primarily store memories as text entries, Pharos aims to represent memories as interactive visual objects within a personal digital environment. Users will be able to save experiences, attach media, explore their virtual island, and discover potential connections between memories.



The project also explores the use of artificial intelligence and machine learning (AI/ML) to support memory organization and identify potentially related experiences.



2\. Problem Statement



Personal memories are often scattered across photographs, notes, messages, and different digital applications. Although these tools allow users to store personal information, they may not provide an engaging and connected way to revisit and explore memories over time.



Pharos aims to address this problem by combining personal memory management, interactive virtual island visualization, gamification, and AI-assisted memory processing in one mobile application.



3\. Project Aim and Objectives



Aim



To design, develop, and evaluate a mobile application that transforms personal memories into interactive elements of a virtual island and investigates how AI-assisted processing can support memory organization and discovery.



Objectives



Review relevant research and existing applications related to digital memory preservation and organization.



Identify target users and define functional and non-functional requirements.



Select suitable technologies for mobile development, backend services, data storage, and AI/ML integration.



Design the system architecture, data model, and user interface.



Develop the core memory management functionality.



Implement an interactive virtual island that visualizes saved memories.



Develop an AI/ML module for extracting structured information from memory descriptions and suggesting potentially related memories.



Integrate the mobile application, backend, database, and AI/ML components.



Test the application's core functionality and evaluate usability and AI/ML output quality.



4\. Target Users



The primary target users are people who want to preserve personal experiences and revisit them through a visual and interactive environment.



Potential users include:



People who keep personal diaries or digital journals.



People who collect photographs and meaningful life experiences.



Users interested in visual storytelling and personal digital archives.



Users who prefer exploring memories through an interactive environment rather than relying only on chronological text entries.



The needs of these users will guide the design and evaluation of the application.



5\. Proposed Features



The initial version of Pharos is expected to include the following features:



Memory management: Create, view, edit, and delete personal memories.



Media attachments: Attach photographs and other supported media to memories.



Virtual island visualization: Represent saved memories as interactive objects within a personal island.



Memory exploration: Select island objects to access detailed memory information.



Data storage: Store and retrieve memory information through backend services and a database.



AI-assisted processing: Extract structured information from memory descriptions, such as topics, dates, or locations when available.



Memory connection suggestions: Identify potentially related memories using suitable similarity-based methods.



Gamification: Explore basic island progression and other suitable mechanics that encourage users to revisit memories.



Privacy controls: Consider secure data handling and appropriate user control over personal information.



AI-generated information and suggested connections will be treated as recommendations that users can review and correct.



The final feature set will depend on requirements analysis, technical feasibility, and the available development time.



6\. Project Scope



In Scope



Mobile application development.



Personal memory creation and management.



Virtual island visualization and interaction.



Backend API development and database integration.



Media storage and retrieval.



AI/ML-assisted memory processing and connection suggestions.



Basic gamification and island progression.



Functional, integration, AI/ML, and usability testing.



Technical and academic documentation.



Out of Scope for the Initial Version



Public social networking and messaging.



Multiplayer island interactions.



A large-scale 3D open world.



Augmented reality or virtual reality functionality.



Training a large language model from scratch.



Guaranteed automatic reconstruction of incomplete or forgotten memories.



Clinical, diagnostic, or therapeutic functionality.



These boundaries help keep the initial implementation achievable within the project timeframe.



7\. Proposed Technology Stack



The following technologies are proposed for the initial implementation. Final selections may change after technical evaluation.



Mobile application: Flutter and Dart.



Backend and REST API: Python with FastAPI.



Database: PostgreSQL.



Database and authentication services: Supabase, subject to confirmation.



AI/ML: Python and suitable machine learning or language-model libraries or APIs.



Media storage: Supabase Storage or a compatible object-storage service.



Virtual island rendering: Flutter-based 2D rendering and animations.



Version control: Git and GitHub.



Project management: YouTrack.



Containerization: Docker.



Testing: Pytest for Python services and suitable Flutter testing tools.



These technologies are proposed rather than all being fully implemented or configured at the current stage.



8\. System Overview



Pharos is planned as a system consisting of several cooperating components:



Mobile client: Provides the user interface, memory management screens, and virtual island interaction.



Backend API: Handles application requests and coordinates data storage and retrieval.



Database: Stores structured memory information and related metadata.



Media storage: Stores photographs and other supported media.



AI/ML module: Processes memory descriptions and returns structured information or suggestions about potentially related memories.



The mobile client and AI/ML module will communicate through documented interfaces coordinated with the backend. The architecture and API contracts will be refined during the design and implementation stages.



9\. Team Roles and Responsibilities



Nurbayeva Assylzada - AI/ML Module



Responsible for researching, designing, developing, and evaluating the AI/ML component.



Responsibilities include:



Selecting suitable methods for processing memory descriptions.



Extracting structured information where available.



Identifying potentially related memories.



Designing validation mechanisms for AI-generated results.



Evaluating output quality and documenting limitations.



Coordinating API contracts and integration with the full-stack component.



Kalzhanov Zhansultan - Full-Stack Development



Responsible for developing the mobile client, virtual island, and memory management module.



Responsibilities include:



Designing and implementing the mobile interface.



Developing virtual island visualization and interactions.



Implementing backend services and database integration.



Supporting memory creation, retrieval, editing, and deletion.



Integrating the mobile client with backend services.



Testing and documenting the full-stack functionality.



Supervisor - Myrzakerimova Alua



Provides academic supervision, feedback on project progress, and guidance on research methodology, technical decisions, and evaluation.



10\. Expected Outcomes



The expected outcome is a working mobile application prototype that enables users to preserve personal memories as interactive objects on a virtual island.



Additional expected outcomes include:



A documented system architecture and data model.



A functional memory management module.



An interactive virtual island interface.



An AI/ML module for structuring memory content and suggesting potential relationships between memories.



Integration interfaces between the main application components.



Test results covering core functionality, AI/ML output quality, and usability.



Technical documentation and a final project demonstration.



These are intended outcomes; each feature will be reported as completed only after implementation and verification.



11\. Evaluation Approach



The project will be evaluated through several methods:



Functional testing: Verify memory creation, viewing, editing, deletion, and island interaction.



Integration testing: Check communication between the mobile client, backend, database, and AI/ML module.



AI/ML evaluation: Assess the correctness of extracted information and the relevance of suggested memory connections using documented test cases and criteria.



Usability evaluation: Assess whether users can understand the interface, manage memories, and navigate the virtual island.



Reliability checks: Examine input validation, error handling, and data persistence.



Specific test cases, metrics, and acceptance criteria will be documented in the evaluation plan.



12\. Risks and Limitations



Potential risks and limitations include:



AI-generated information or suggested memory connections may be incomplete or incorrect.



Some memory details may be unavailable if users do not provide them.



Integration between the mobile application, backend, database, and AI/ML module may require additional development.



Advanced graphics and extensive personalization may be limited in the initial version.



The quality of AI/ML results will depend on the selected methods and evaluation data.



Personal memories may contain sensitive information, so privacy and secure data handling must be considered throughout development.



AI-generated recommendations will require validation and user review.



13\. Project Development Stages



The planned development stages are:



Complete the project proposal, research background, and initial requirements.



Define system architecture, data models, and API contracts.



Design the user interface and interactive prototype.



Implement the core memory management functionality and database integration.



Develop the AI/ML memory processing module.



Implement and integrate the virtual island visualization.



Conduct functional, integration, AI/ML, and usability evaluation.



Finalize documentation and prepare the project demonstration.



The order and scope of individual tasks may be adjusted according to progress and technical feasibility.



14\. Current Project Status



The project is currently in the planning, requirements analysis, and initial architecture design stage.



The repository contains initial project documentation and a proposed repository structure. The implementation status of individual features will be updated as development progresses.



The project proposal, requirements, architecture, prototype, and evaluation documents will be maintained in the GitHub repository.



15\. Conclusion



Pharos aims to provide a more visual and interactive approach to personal memory preservation by combining memory management, a virtual island environment, gamification, and AI-assisted organization.



The project will investigate the feasibility and usefulness of this approach through prototype development, technical testing, and usability evaluation. The final implementation and conclusions will be based on the features successfully developed and the evidence collected during evaluation.

