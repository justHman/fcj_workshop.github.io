### Week 5 Objectives:

* Set up the core FastAPI backend foundation.
* Construct robust Python wrapper classes the chosen external APIs.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Install and configure FastAPI and `uvicorn` framework <br> - Outline backend routing modules in `app/api` | 02/02/2026   | 02/02/2026      | FastAPI Documentation |
| 3   | - Draft Python wrapper classes linking to the USDA endpoint <br> - Develop internal HTTP client handles | 03/02/2026   | 03/02/2026      |
| 4   | - Construct wrapper mechanisms connecting to OpenFoodFacts <br> - Test JSON response decoding against sample barcodes | 04/02/2026   | 04/02/2026      |
| 5   | - Standardize a centralized Mock Data logic strategy to use as fallback data when valid API tokens are missing | 05/02/2026   | 05/02/2026      |
| 6   | - Merge endpoints into root API.py <br> - Test local server status using FastAPI automatically-generated `/docs` Swagger UI | 06/02/2026   | 06/02/2026      | Swagger UI Docs |

### Week 5 Achievements:

* Built a functional bare-bones FastAPI backend instance ready to handle complex HTTP web requests.
* Completed Python wrapper client logic capable of successfully fetching USDA API nutrition metrics.
* Completed Python wrapper mechanisms for the OpenFoodFacts service, ensuring barcode lookups map correctly.
* Secured a Mock Data fallback workflow allowing the backend codebase to test smoothly even without raw live API credentials.
* Verified backend configuration through FastAPI Swagger UI visual interface testing.