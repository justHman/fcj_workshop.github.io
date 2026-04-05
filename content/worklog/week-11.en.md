### Week 11 Objectives:

* Prepare the project for production environment deployments initially bridging to Fly.io edge networking.
* Automate the CI/CD pipeline ensuring secure and seamless delivery iterations via GitHub Actions.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Write Infrastructure as Code (IaC) via Terraform <br> - Configure Github Actions `.yml` files for CI/CD | 16/03/2026   | 16/03/2026      | GitHub Actions Docs |
| 3   | - Handle and mask critical secrets/variables during CI workflows <br> - Write SSH deployment workflows | 17/03/2026   | 17/03/2026      |
| 4   | - Test initial backend deployments targeting Fly.io edge servers | 18/03/2026   | 18/03/2026      | Fly.io documentation |
| 5   | - Develop logic to upload/download caches through Fly.io volume boundaries via SFTP protocols natively in the Github Action | 19/03/2026   | 19/03/2026      |
| 6   | - Patch the "Virtual Machine died before cache uploaded" errors during Fly.io deployment rollouts | 20/03/2026   | 20/03/2026      |

### Week 11 Achievements:

* Integrated complete edge CI/CD automation through Github Actions. Pushing code now automatically scrubs, builds, and pushes containerized artifacts seamlessly.
* Solved intense secret-leaking issues inside Action logs by masking and safely passing `.env` credentials dynamically.
* Conquered Fly.io distributed volume caching logic by manipulating SFTP logic natively inside pipeline structures, transferring previously localized models over to the Cloud Virtual Machines robustly.
* Successfully stabilized Fly.io VMs mitigating sudden death crashes during heavy CI/CD asset sync procedures.