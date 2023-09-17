**Exercise: Setting Up a GitLab CI/CD Pipeline for a "Hello World" Web Application**

**Objective:** Create a GitLab CI/CD pipeline to automate the build and deployment of a "Hello World" web application.

**Prerequisites:**

1. Access to a GitLab account or instance.
2. A GitLab project.
3. Basic knowledge of Git and GitLab CI/CD.

**Instructions:**

1. **Create a GitLab Repository:**

   If you haven't already, create a GitLab repository for your "Hello World" web application or use an existing one.

2. **Set Up the Web Application:**

   Create a simple "Hello World" web application in the repository. You can use HTML, CSS, and JavaScript to create a basic webpage with a "Hello, World!" message.

   - Create an `index.html` file:

     ```html
     <!DOCTYPE html>
     <html>
     <head>
         <title>Hello World</title>
     </head>
     <body>
         <h1>Hello, World!</h1>
     </body>
     </html>
     ```

   - Commit and push the `index.html` file to your GitLab repository.

3. **Create a `.gitlab-ci.yml` File:**

   In your project's root directory, create a `.gitlab-ci.yml` file to define the CI/CD pipeline. Start with a basic configuration:

   ```yaml
   stages:
     - build
     - deploy

   build:
     stage: build
     script:
       - echo "Building the web application..."
       # You can add build commands here if needed

   deploy:
     stage: deploy
     script:
       - echo "Deploying the web application..."
       # You can add deployment commands here if needed
   ```

   This configuration defines two stages: `build` and `deploy`. The jobs in these stages currently echo messages.

4. **Commit and Push the `.gitlab-ci.yml` File:**

   Add the `.gitlab-ci.yml` file to your Git repository, commit it, and push the changes:

   ```bash
   git add .gitlab-ci.yml
   git commit -m "Add .gitlab-ci.yml"
   git push origin master  # Or your branch name
   ```

5. **Trigger the Pipeline:**

   Open your GitLab project, and navigate to "CI/CD" > "Pipelines." You should see a new pipeline triggered by the push you made in step 4. Click on it to view the pipeline's progress.

6. **Observe the Pipeline Execution:**

   As the pipeline runs, you'll see the stages and jobs being executed. In this basic example, the jobs only print messages. However, you can replace these script commands with actual build and deployment commands for your web application.

. **Explore Advanced Features:**

    Once you have a basic pipeline working, explore GitLab CI/CD's more advanced features, such as caching dependencies, deploying to different environments, and integrating with external services.