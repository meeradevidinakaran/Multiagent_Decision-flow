# Pre-requisite Setup
Install Docker Desktop Docker Desktop is a free application that lets you run Docker containers on your computer. Visit the official Docker Desktop download page: https://www.docker.com/products/docker-desktop/ Download OS specific Version, Install and restart to see docker instance running. Use command prompt to ensure docker isntallation is successful - "docker --version"

langflow on docker With Docker running, use this single command to download and start Langflow: "docker run -it -p 7860:7860 langflowai/langflow:latest" Once Completed,Open your web browser and go to: http://localhost:7860

# Steps to get started on Langflow.
Start Creating workflows on langflow local instance. 
User a Chat Input and connect it to an Agent. Within each agent Connect to the Open AI using a valid API Key and select preferred LLM models. Provide agent instructions in System prompts.

# Create Notion Workspace

Use https://www.notion.com/ and select "Get notion for free" and signup using your google account. 

Once done create your own workspace. In Your workspace create a New Page - name it "Decision Memo" and select Share button on the same page and select from Options 1. Anyone with the link can edit or
2. Invite people to edit/ view the page.

# Integrate Notion with Langflow 
Navigate to https://app.notion.com/developers/  and set up an **Integration / Connection** provide a name (ex: Langflow integration)and hit Connect.
Once a new connection is established Copy the API secret key . We will later use the same in the **Add content to page** Notion node in langflow.
