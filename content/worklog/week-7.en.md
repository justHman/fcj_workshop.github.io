### Week 7 Objectives:

* Integrate Amazon Bedrock Large Language Models (LLM) to perform initial food recognition on images.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Configure Boto3 client to access AWS Bedrock API | 16/02/2026   | 16/02/2026      | Boto3 Bedrock Docs |
| 3   | - Test inferences using Claude 3 models via Bedrock <br> - Pass compressed images from Week 6 securely to the VLM endpoint | 17/02/2026   | 17/02/2026      |
| 4   | - Draft prompt engineering instructions defining the LLM's goal: "Identify foods in this image" | 18/02/2026   | 18/02/2026      | Authored Prompt templates |
| 5   | - Combine LLM outputs with the Mock Data logic previously built | 19/02/2026   | 19/02/2026      |
| 6   | - Refactor backend model layers to abstract LLM usage <br> - Set up environment token validations | 20/02/2026   | 20/02/2026      |

### Week 7 Achievements:

* Authorized AWS credentials to securely access Amazon Bedrock inference services via `boto3`.
* Established the vital image-to-text bridge by feeding compressed user images securely into the Cloud LLM pipeline and receiving food recognition classifications.
* Orchestrated early Prompt Engineering iterations to limit the AI's "hallucinations" and strictly capture nutrition item variables.