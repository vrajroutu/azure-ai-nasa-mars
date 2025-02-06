
# 🚀 NASA Mars Missions Chatbot (Powered by Azure AI) 🌌

This project demonstrates how to build an **AI-powered chatbot** using **Azure AI Agent Service**, capable of answering questions about **NASA Mars Missions**. The chatbot integrates **local NASA documents**, **Bing search for real-time information**, and **custom Python functions** to provide informative and structured responses.


![Mars Rover](https://upload.wikimedia.org/wikipedia/commons/3/3a/NASA_Mars_Perseverance_Rover.jpg)

---

## 📌 Features

- 🤖 **AI Agent with GPT-4o (or other Azure models)**
- 🔍 **Search NASA documents** using a **Vector Store** (text or PDF)
- 🌍 **Fetch live data** via **Bing search grounding**
- 🛰️ **Call custom functions** (e.g., upcoming rocket launches)
- 🎨 **User-friendly Chat Interface** built with **Gradio**
- 🌐 **Deployable on Azure, Local Machine, or GitHub Codespaces**

---

## 🛠️ Setup & Installation

### 1️⃣ Prerequisites

- An **Azure AI Projects** account (Preview)
- An **Azure AI Agent Service** with a **Bing search connection**
- A local folder **`nasa-data/`** with **at least one** public-domain NASA document (text/PDF)
- Python **3.8+**
- Required Python Packages:

```bash
pip install azure-ai-projects azure-identity gradio python-dotenv
```
## 2️⃣ Clone the Repository

git clone https://github.com/yourusername/azure-ai-nasa-mars.git
cd azure-ai-nasa-mars

## 3️⃣ Set Up Environment Variables

Create a .env file in the project root and add:

PROJECT_CONNECTION_STRING="your_azure_ai_project_connection_string"
BING_CONNECTION_NAME="your_bing_search_connection_name"
MODEL_DEPLOYMENT_NAME="gpt-4o"

	Where do I find these?
		•	PROJECT_CONNECTION_STRING: In your Azure AI Projects resource.
	•	BING_CONNECTION_NAME: After setting up a Bing search connection in Azure AI Agent.
	•	MODEL_DEPLOYMENT_NAME: Your deployed model (default is gpt-4o).

## 4️⃣ Add NASA Documents

Create a folder nasa-data/ and place at least one .txt or .pdf file with public NASA Mars data (e.g., Perseverance Rover Mission Summary).

Example:

mkdir nasa-data
echo "NASA's Perseverance Rover landed on Mars on February 18, 2021, to search for signs of ancient life." > nasa-data/perseverance.txt

🚀 Running the Chatbot

## 1️⃣ Run the Jupyter Notebook

Launch Jupyter and open nasa_mars_agent_demo.ipynb:

jupyter notebook nasa_mars_agent_demo.ipynb

	•	Runs the AI agent, connects to Bing search, and loads NASA documents.
	•	Creates a vector store for document search.
	•	Starts a Gradio chat interface.

## 2️⃣ Run as a Standalone Python App

Alternatively, convert the notebook to a Python script and run it:

jupyter nbconvert --to script nasa_mars_agent_demo.ipynb
python nasa_mars_agent_demo.py

🎨 Using the Chatbot

1️⃣ Ask a question (e.g., “What is the Perseverance rover?”)
2️⃣ Wait for the response (the AI will search local docs & Bing if needed)
3️⃣ Interact with additional features (e.g., “When is the next NASA rocket launch?”)



## ❌ Cleanup (Optional)

If you want to delete all created Azure resources, run:

```Uncomment and run in Jupyter Notebook```

```project_client.agents.delete_agent(agent.id)```
```project_client.agents.delete_thread(thread.id)```
```project_client.agents.delete_vector_store(vector_store_id)```

## 🤝 Contributing

🚀 Want to improve this chatbot? PRs are welcome!
	1.	Fork the repo
	2.	Create a feature branch (git checkout -b my-feature)
	3.	Commit changes (git commit -m "Added new Mars function")
	4.	Push to branch (git push origin my-feature)
	5.	Create a Pull Request

## 📜 License

This project is licensed under the MIT License.

## 💡 Acknowledgments
	•	NASA Open Data (nasa.gov/open-data)
	•	Microsoft Azure AI (azure.com/ai)
	•	OpenAI GPT models (openai.com)

🌟 If you found this helpful, give us a ⭐ on GitHub!
📢 Follow vrajroutu for more AI projects!

---

## 🔹 Summary of README.md

- **Clear introduction**: Explains what the project does and why it's useful.
- **Installation guide**: Step-by-step setup for running the chatbot.
- **Deployment instructions**: Covers **local** and **Azure** deployment.
- **Usage guide**: Shows how to interact with the chatbot.
- **Cleanup section**: Provides resource deletion instructions.
- **Contribution & License**: Encourages open-source contributions.
