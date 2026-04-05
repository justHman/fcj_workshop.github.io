### Week 8 Objectives:

* Construct an interactive User Interface (Gradio) for demonstrations.
* Mature the LLM infrastructure with strict "Tool Calling" logic to allow multiple food calculation in a single API pass.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - First major Repository synchronization (Init project commits) <br> - Construct the `.env` handling structure | 23/02/2026   | 23/02/2026      | Github Commit History |
| 3   | - Support multiple food identification within a single image context <br> - Resolve calculations when NO items versus MULTIPLE items are found | 24/02/2026   | 24/02/2026      |
| 4   | - Construct robust Tool Calling features so LLM outputs strict JSON instead of plain conversational text <br> - Begin metrics tracking on pricing and token counts | 25/02/2026   | 25/02/2026      |
| 5   | - Pass regression testing for local APIs with concurrent multiple objects <br> - Handle exceed bounds rounding for LLM outputs | 26/02/2026   | 26/02/2026      |
| 6   | - Build a Gradio UI directly connecting backend endpoints <br> - Sync testing across Jupyter Notebooks (`test_all.ipynb`) and Web UI | 27/02/2026   | 27/02/2026      | Gradio Library Docs |

### Week 8 Achievements:

* Synchronized early project files officially into Git tracking, ensuring safe source code history.
* Fully transitioned from conversational AI interaction to deterministic LLM Tool Calling; the system now explicitly formats nutrition calculations natively as JSON.
* Solved the multi-object limitation, empowering the pipeline to recognize and calculate totals for multiple distinct food items in a single user picture.
* Rolled out a functional frontend dashboard via Gradio, dramatically improving testing speed and visualizing end-to-end user workflow without using Postman.
* Handled edge cases natively, such as when an image has ZERO recognizable food items or files hitting byte-size restrictions.