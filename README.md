The backend part of this Expense Tracker project is developed using Spring Boot. It is responsible for handling all the core operations such as adding expenses, updating them, deleting records, and fetching expense details. The backend exposes REST APIs which are used by the frontend to display and manage data.

To make deployment easier and consistent, the backend is Dockerized. This helped in avoiding system-specific issues and made the deployment process smooth. The Dockerized backend is deployed on Render, which provides a public URL for accessing the APIs. Code quality is maintained using SonarCloud, which is integrated through GitHub.

⚠️ Challenges Faced in Backend

Dockerfile location issues
At first, Docker build failed because the Dockerfile was not placed in the correct folder. Since Docker and Render expect the Dockerfile in a specific path, this caused errors. After verifying the project structure and correcting the path, the issue was resolved.

Docker image build errors
While building the Docker image, errors occurred due to incorrect OpenJDK versions. Choosing a stable and supported OpenJDK image fixed the build failures.

Render deployment confusion
Initially, there was confusion while deploying on Render because the platform did not ask to select Java explicitly. Later, it was understood that Render automatically handles the build when Docker is used, and selecting Docker was sufficient.

Environment variable handling
There was confusion between using .env files and Render environment variables. Finally, environment values were configured directly in the Render dashboard, which worked correctly for production.

SonarCloud and GitHub issues
SonarCloud analysis initially failed due to missing commits and incorrect configuration. After properly committing the workflow files and setting the correct tokens, the analysis ran successfully.
