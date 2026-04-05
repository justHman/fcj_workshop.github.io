### Week 4 Objectives:

* Kickoff the NutriTrack backend project and design the foundational directory structure.
* Research and document nutritional APIs (OpenFoodFacts, USDA) for tracking capabilities.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Initialize the NutriTrack repository <br> - Set up fundamental Python Virtual Environment (`.venv`) <br> - Design folder skeleton (app, docs, third_apis) | 26/01/2026   | 26/01/2026      |
| 3   | - Analyze USDA API integration requirements <br> - Register necessary API Keys <br> - Draft basic test requests using `curl` / Postman | 27/01/2026   | 27/01/2026      | USDA FDC API Docs |
| 4   | - Evaluate OpenFoodFacts API for barcode searching <br> - Study their exact JSON payload responses <br> - Compare data reliability with USDA | 28/01/2026   | 28/01/2026      | OpenFoodFacts API Docs |
| 5   | - Establish initial `.env` handling & environment configurations <br> - Document safe API key handling practices | 29/01/2026   | 29/01/2026      |
| 6   | - Map the theoretical core data structures for nutrition objects (Calories, Macros, Micro-nutrients) <br> - Outline how external API wrappers will be built | 30/01/2026   | 30/01/2026      |

### Week 4 Achievements:

* Successfully established the foundation of the NutriTrack backend structure, properly sandboxing it with Python `.venv`.
* Validated and documented test endpoints for the USDA API, securing proper API tokens for development.
* Researched OpenFoodFacts and outlined a strategy to leverage its database for barcode-based lookups.
* Prepared the exact `.env` strategy to ensure no private keys will be leaked into version control.
* Created a theoretical mapping for unifying arbitrary JSON data from different external APIs into a single internal nutrition format.