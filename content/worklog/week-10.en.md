### Week 10 Objectives:

* Complete testing and syncing operations for Barcode APIs internally and externally.
* Heavily optimize LLM token usage, speed delays, and monitor infrastructure cost pricing metrics.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Retrieve extended datasets internally <br> - Test barcode formatting algorithms cross-referenced against all 3 third-party clients (OpenFoodFacts, FDB, USDA) | 09/03/2026   | 09/03/2026      |
| 3   | - Implement caching methodologies to bypass redundant queries <br> - Set up server to halt console logging on AWS ECS `LOG_TO_FILE` logic | 10/03/2026   | 10/03/2026      |
| 4   | - Modify prompt structure entirely to decrease context-token costs <br> - Optimize Clear functionalities to scrub dirty outputs before JSON parsing | 11/03/2026   | 11/03/2026      |
| 5   | - Implement metrics tracking measuring input/output Bedrock tokens alongside latency execution speeds and raw USD prices per inference | 12/03/2026   | 12/03/2026      |
| 6   | - Refine optimization loops across Both the Food Identifying pipeline and the Label reading pipeline <br> - Perform overall benchmark to confirm speed enhancements | 13/03/2026   | 13/03/2026      |

### Week 10 Achievements:

* Uniformly synced output mapping logic across all three third-party Barcode identification API providers, preventing UI breakage issues regardless of which datasource returned the nutrition.
* Optimized prompt logic drastically, stripping thousands of hidden tokens out of the pipeline, which directly decreased raw processing price limits while drastically increasing latency execution speeds.
* Finished testing standard data crawlers/caching utilities to avoid slamming the live APIs repeatedly for identical static foods.
* Embedded internal metadata metrics allowing the API backend to calculate input tokens, output tokens, time per request, and API cost per endpoint request.