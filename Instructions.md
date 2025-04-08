
### Instructions for Use

Follow these steps to use and adapt the chatbot in your own Google Colab setup:

---

#### 1. Set Up Google Drive

- Create a folder named `CHATBOT` inside your Google Drive.
- Upload the dataset file:
  - `spiderman_chatbot_dataset.csv`

---

#### 2. Open Colab Notebooks

- Go to https://colab.research.google.com/
- Open the notebooks:
  - `LLM_ChatBot_Training.ipynb` – used for preparing the dataset, training, and pushing the model.
  - `LLM_Chatbot_Gradio.ipynb` – used for loading and running the chatbot.

---

#### IMPORTANT: Replace or Skip Author-Specific Commands

Throughout the notebooks, you will see commands like:

```python
model.push_to_hub("IrfanHamid/ChatBot-lora-7b")
tokenizer.push_to_hub("IrfanHamid/ChatBot-lora-7b")
upload_file(..., repo_id="IrfanHamid/chat-dataset", ...)
```

And in GitHub automation:

```python
repo_url = "github.com/Irfan-Hamid/Chatbot.git"
push_to_github(my_key, repo_url)
```

These use the author's Hugging Face and GitHub accounts and are:

✅ For reference only  
❌ Do NOT run them as-is

If you'd like to push your own model or dataset, replace `"IrfanHamid/...` and `Irfan-Hamid/...` with your own usernames and repository names.

---

#### 3. Training

- Running `LLM_ChatBot_Training.ipynb` will:
  - Load and format the dataset
  - Tokenize the data
  - Fine-tune `meta-llama/Llama-2-7b-chat-hf` using LoRA
  - (Optionally) Upload the model and dataset to Hugging Face

---

#### 4. Deploying the Chatbot

- `LLM_Chatbot_Gradio.ipynb`:
  - Loads the base model + LoRA adapters
  - Launches an interactive Gradio interface
  - Styled with a comic-style background
  - Lets you chat in the voice of Spider-Man (or any other persona you train for)

---

This is meant for personal or educational experimentation, not production use.
