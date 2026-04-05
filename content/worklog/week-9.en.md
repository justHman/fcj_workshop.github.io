### Week 9 Objectives:

* Standardize project deployments by implementing Containerization (Docker).
* Build foundational capabilities to analyze strictly nutritional Labels from images.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Prepare global `requirements.txt` listing <br> - Author initial `Dockerfile` encapsulating Python dependencies | 02/03/2026   | 02/03/2026      | Docker Reference Docs |
| 3   | - Deep code cleanup: Delete redundant scripts and useless cached files <br> - Configure `.gitignore` and `.dockerignore` | 03/03/2026   | 03/03/2026      |
| 4   | - Clean git cache environments ensuring leaked secrets or heavy DBs aren't tracked | 04/03/2026   | 04/03/2026      |
| 5   | - Shift LLM focus to OCR Label extraction <br> - Configure prompt templates specifically aimed at reading nutrition facts | 05/03/2026   | 05/03/2026      |
| 6   | - Refine label analysis parsing to natively convert printed labels into internal standard JSON objects | 06/03/2026   | 06/03/2026      |

### Week 9 Achievements:

* Successfully Dockerized the application, establishing an environment-agnostic setup where developers from backend or frontend can run the backend without native Python hassle.
* Drastically reduced project payload by aggressively configuring `.gitignore` and `.dockerignore` files, flushing out bloated legacy caches.
* Transitioned the LLM pipeline focus beyond just identifying food elements, natively integrating a Label Extraction workflow capable of scraping tabular values from photographed nutritional facts.