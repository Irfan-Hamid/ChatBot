
# LLM Character Based Chatbot using LLaMA 2

This project fine-tunes Meta's `LLaMA-2-7b-chat-hf` model to behave like a character-based chatbot (specifically inspired by Spider-Man,Peter Parker). The model is trained using a Q&A dataset and responds in a witty, heartfelt tone, capturing the iconic persona of the superhero.

## Model Summary

- **Base Model:** meta-llama/Llama-2-7b-chat-hf
- **Fine-tuning Method:** LoRA (Low-Rank Adaptation) using `peft`
- **Quantization:** 4-bit (via `bitsandbytes`)
- **Prompt Format:** Chat template using the model's built-in `apply_chat_template`
- **Training Framework:** Hugging Face `transformers.Trainer`

## Trained Model & Dataset on Hugging Face

- **Fine-tuned LoRA Adapter:** [ChatBot-lora-7b](https://huggingface.co/IrfanHamid/ChatBot-lora-7b)
- **Training Dataset:** [chat-dataset](https://huggingface.co/datasets/IrfanHamid/chat-dataset)

## Project Structure

```
CHATBOT/
├── LLM_ChatBot_Training.ipynb      # Notebook for dataset preparation, LoRA fine-tuning, and model upload to Hugging Face
├── LLM_Chatbot_Gradio.ipynb        # Notebook for loading the model from Hugging Face and running the Gradio interface
├── spiderman_chatbot_dataset.csv   # The Q&A dataset used for fine-tuning
├── README.md                       # Project overview
├── Instructions.md    # Setup and usage guide, including important notes on replacing user-specific commands

```

## Demo

Use the fine-tuned model interactively via a Gradio app that lets you chat with the Spider-Man-inspired persona.

Here’s a snapshot of the chatbot in action:

<img width="1401" alt="Screenshot 2025-04-08 at 03 22 26" src="https://github.com/user-attachments/assets/1b51c45b-c64c-4c10-a47c-0385268109b1" />

## Notes

- This project is for **educational and personal portfolio purposes only**.
- All character likeness, names, and styles related to Spider-Man are property of **Marvel**.
- No part of this project is intended for **commercial** or **promotional** use.
- The use of fictional personas is intended purely for technical exploration and learning.

---
