Functional and Non-Functional Requirements - Pharos

1. Purpose

This document defines the functional and non-functional requirements for Pharos, a gamified mobile application for preserving, organizing, and exploring personal memories through an interactive virtual island.

The requirements establish the expected behaviour and quality characteristics of the initial version (Minimum Viable Product, MVP).

2. User Roles and Needs

2.1 Registered User

The primary user creates and manages personal memories, attaches supported media, and explores memories through the virtual island.

User needs:

1. Preserve personal experiences in a structured form.
2. Find and revisit previously saved memories.
3. Understand how memories are represented on the island.
4. Maintain control over personal information.

2.2 Project Administrator

An administrator role is not required for the initial MVP unless later security or operational requirements establish a clear need. Administrative functions are therefore outside the current MVP scope.

3. Functional Requirements

Each functional requirement has a unique identifier and a priority.

Priority definitions:

1. Must: Required for the initial MVP.
2. Should: Important, but the MVP can operate without it temporarily.
3. Could: Optional enhancement if time and resources permit.

| ID    | Requirement                                                                                                                                    | Priority |
| ----- | ---------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| FR-01 | The application shall allow a user to create a memory containing a title and text description.                                                 | Must     |
| FR-02 | The application shall allow a user to view a list of saved memories.                                                                           | Must     |
| FR-03 | The application shall allow a user to open and view the details of an individual memory.                                                       | Must     |
| FR-04 | The application shall allow a user to edit an existing memory.                                                                                 | Must     |
| FR-05 | The application shall allow a user to delete a memory after an explicit confirmation.                                                          | Must     |
| FR-06 | The application shall preserve saved memory data between application sessions.                                                                 | Must     |
| FR-07 | The application shall represent saved memories as interactive objects on a virtual island.                                                     | Must     |
| FR-08 | The application shall allow a user to select an island object and open its associated memory.                                                  | Must     |
| FR-09 | The application should allow a user to attach a photograph or other supported media to a memory.                                               | Should   |
| FR-10 | The application should allow a user to search or filter memories using available metadata.                                                     | Should   |
| FR-11 | The application could provide basic island progression or visual rewards for memory exploration.                                               | Could    |
| FR-12 | The application could suggest potentially related memories using AI/ML-based processing.                                                       | Could    |
| FR-13 | If AI/ML suggestions are implemented, the application shall present them as suggestions that users can review rather than as guaranteed facts. | Should   |
| FR-14 | The application shall provide clear feedback when a memory cannot be saved, loaded, edited, or deleted.                                        | Must     |

4. Non-Functional Requirements

4.1 Usability

| ID     | Requirement                                                                                                                 |
| ------ | --------------------------------------------------------------------------------------------------------------------------- |
| NFR-01 | The application shall use consistent navigation and clearly labelled controls for core memory operations.                   |
| NFR-02 | A user shall be able to identify how to create a memory and access a saved memory without relying on external instructions. |
| NFR-03 | The application shall provide understandable confirmation and error messages for important actions.                         |

4.2 Performance

| ID     | Requirement                                                                                                                                                                                                        |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| NFR-04 | Under normal test conditions, the application should display a saved memory's details within 2 seconds for at least 95% of requests using a representative test dataset.                                           |
| NFR-05 | Under normal test conditions, the main memory list and virtual island view should become usable within 3 seconds after the relevant screen is opened, excluding unusually slow network or external service delays. |

These targets are provisional and should be validated on the selected development devices and test environment.

4.3 Privacy and Security

| ID     | Requirement                                                                                                                                         |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| NFR-06 | The application shall not intentionally expose one user's private memories to another user.                                                         |
| NFR-07 | The application shall validate user input and handle errors without exposing sensitive technical details.                                           |
| NFR-08 | Personal memory data and media shall be transmitted using secure connections when network communication is used.                                    |
| NFR-09 | Any external AI/ML service considered for processing memory content shall be evaluated for privacy implications before personal data is sent to it. |

4.4 Reliability and Data Integrity

| ID     | Requirement                                                                                                                                                  |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| NFR-10 | Successfully saved memories shall remain available after the application is closed and reopened, provided the underlying storage service is available.       |
| NFR-11 | The application shall communicate unsuccessful save or delete operations and shall not falsely report them as successful.                                    |
| NFR-12 | The application shall handle unavailable network or backend services gracefully and provide an understandable message when an operation cannot be completed. |

4.5 Maintainability and Compatibility

| ID     | Requirement                                                                                                                                                  |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| NFR-13 | The application source code shall be organized into modules with clearly defined responsibilities.                                                           |
| NFR-14 | The project shall document the selected development technologies and the interfaces between the mobile client, backend, database, and optional AI/ML module. |
| NFR-15 | The initial version shall target the mobile platform or platforms selected by the team and documented in the project setup.                                  |

5. MVP Prioritization

The initial MVP shall prioritize the following capabilities:

1. Create, view, edit, and delete personal memories.
2. Persist memory data between sessions.
3. Display memories in a basic virtual island environment.
4. Open a memory by selecting its island object.
5. Provide basic input validation and clear error feedback.
6. Apply appropriate privacy and secure communication practices for the implemented architecture.

Media attachments, search and filtering, gamification, and AI/ML-based memory suggestions may be added according to available time, feasibility, and the results of technical investigation. Their final priority should be reviewed by the team.

6. Acceptance and Verification

Requirements shall be verified through documented inspection, functional tests, integration tests, or usability checks as appropriate.

1. FR-01 to FR-05: Verify memory creation, listing, viewing, editing, and deletion.
2. FR-06 and NFR-10: Verify that saved memories remain available after restarting the application.
3. FR-07 and FR-08: Verify that island objects represent memories and open the correct memory details.
4. FR-14 and NFR-11 to NFR-12: Verify error handling and feedback when operations fail.
5. NFR-04 and NFR-05: Measure response times in a documented test environment.
6. NFR-06 to NFR-09: Inspect the implemented data access, communication, and external-service handling against the stated privacy and security requirements.

Requirements shall be updated when project scope or technical decisions change. Any requirement that is not implemented in the MVP shall be recorded as outstanding work rather than reported as completed.

7. Known Limitations and Outstanding Decisions

1. The final backend, database, authentication, and media-storage configuration must be confirmed by the team.
2. Performance targets require validation in the selected test environment.
3. The exact implementation of the virtual island and progression mechanics remains subject to prototype evaluation.
4. AI/ML memory suggestions are optional for the initial MVP and require a separate evaluation of usefulness, accuracy, and privacy.
5. Authentication and account-management features must be specified if the final deployment requires individual user accounts.

8. Document Status

This document defines the initial proposed requirements for Pharos. It is a planning baseline, not evidence that every listed feature has already been implemented or tested.
