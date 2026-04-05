### Week 6 Objectives:

* Construct the underlying image handling and compression utility systems.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Write custom image utility methods to intercept and resize big images | 09/02/2026   | 09/02/2026      | Python Pillow Docs |
| 3   | - Fix compression modes ignoring `RGBA` formats, catch P-mode palette errors | 10/02/2026   | 10/02/2026      |
| 4   | - Handle dynamic temporary saving logic for intercepted files before they go to model inference | 11/02/2026   | 11/02/2026      |
| 5   | - Implement logic to purge temporary image files safely to prevent memory leaks | 12/02/2026   | 12/02/2026      |
| 6   | - Comprehensive code review on the media processing pipelines and error handling | 13/02/2026   | 13/02/2026      |

### Week 6 Achievements:

* Built fundamental image compression components utilizing Pillow effectively handling format errors (`OSError`: palette-based 'P').
* Refined input file sanitization pipelines which act prior to AI analysis loops.
* Ensured high performance and low memory overhead by efficiently purging temporary files post-inference.