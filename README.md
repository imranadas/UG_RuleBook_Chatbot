# UG RULEBOOK Helper AI Chat

Quickly summarize the content of UG RuleBook and get the information you need in **real-time** from private large unstructured documents in your [Dropbox](https://dropbox.com/). The same tool can be used with [OneDrive](https://onedrive.live.com/login/).

#### Prerequisites

1. Make sure that [Docker](https://www.docker.com/products/docker-desktop/)installed on your machine.
2. Create an [OpenAI](https://openai.com/) account and generate a new API Key: To access the OpenAI API, you will need to create an API Key. You can do this by logging into the [OpenAI website](https://openai.com/product) and navigating to the API Key management page.
3. Use your Dropbox/OneDrive account.

Then, follow the easy steps to install and get started using the sample app.

#### Step 1: Clone the repository

This is done with the `git clone` command followed by the URL of the repository:

```bash
git clone https://github.com/imranadas/UG_RuleBook_Chatbot
```

Next,  navigate to the project folder:

```bash
cd UG_RuleBook_Chatbot
```

#### Set environment variables and Run With Docker

1. Create `.env` file in the root directory of the project, copy and paste the below config. Replace the `OPENAI_API_TOKEN` configuration value with your key `{OPENAI_API_KEY}` and replace `PATH_TO_DROPBOX` with a relative path where Dropbox folder is located `{REPLACE_WITH_DROPBOX_RELATIVE_PATH}` in the parent directory. For example, if the current project folder is `DROPBOX-SEARCH-TOOL`, you navigate to the Dropbox path in the parent directory: `../../../mnt/c/Users/bumur/Dropbox/documents`. Other properties are optional to change and be default.

```bash
OPENAI_API_TOKEN={OPENAI_API_KEY}
EMBEDDER_LOCATOR=text-embedding-ada-002
EMBEDDING_DIMENSION=1536
MODEL_LOCATOR=gpt-3.5-turbo
MAX_TOKENS=200
TEMPERATURE=0.0
PATH_TO_DROPBOX={REPLACE_WITH_DROPBOX_RELATIVE_PATH}
```

2. From the project root folder, open your terminal and run `docker compose up`.
3. Navigate to `localhost:8501` on your browser when docker installion is successful.
