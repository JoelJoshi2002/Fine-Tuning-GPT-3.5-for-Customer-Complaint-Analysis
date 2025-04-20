# 🧠 Fine-Tuning GPT-3.5 for Customer Complaint Analysis

Welcome to my personal project where I fine-tune OpenAI’s GPT-3.5 model to help PulseNet, a telecommunications company, automatically analyze customer complaints. This project demonstrates an end-to-end pipeline—from data preparation to model evaluation—to extract key information and measure customer dissatisfaction in real time.

## 🎯 Project Overview

PulseNet provides internet, television, and phone services to a large customer base and receives thousands of complaints daily. Manually reviewing each complaint is time-consuming and prone to inconsistency. My objective is to develop a fine-tuned GPT-3.5 model that:

- Identifies the **topic** of a complaint (e.g., Internet, Billing, TV)
- Extracts the detailed **problem** description
- Calculates a **dissatisfaction index** (0–100) representing customer frustration

I use a provided dataset of 50 annotated complaints to train and validate the model.

## 🗂️ Repository Structure

```
LLM_FineTuning_pynb.ipynb   # Jupyter notebook with the full workflow
complaints_dataset.json     # Dataset of 50 annotated customer complaints
README.md                   # This README file
```

## 🧰 Tech Stack

- **Model**: GPT-3.5 (OpenAI API)
- **Language**: Python (3.x)
- **Environment**: Jupyter Notebook
- **Key Libraries**:
  - `openai`
  - `pandas`
  - `tqdm`
  - `json`

## 🚀 Workflow

1. **Setup**  
   - Install dependencies  
   - Configure `OPENAI_API_KEY`

2. **Data Preparation**  
   - Load and inspect the annotated complaints  
   - Format data into prompt-completion pairs

3. **Fine-Tuning**  
   - Upload formatted data to OpenAI  
   - Launch the fine-tuning job for GPT-3.5

4. **Testing & Evaluation**  
   - Run the fine-tuned model on new complaints  
   - Validate JSON outputs  
   - Compute simple accuracy checks

5. **Results & Insights**  
   - Review model performance  
   - Identify areas for further improvement

## ⚙️ Getting Started

1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/llm-fine-tuning-pulse.git
   cd llm-fine-tuning-pulse
   ```

2. Install Python dependencies:  
   ```bash
   pip install openai pandas tqdm
   ```

3. Set your OpenAI API key as an environment variable:  
   ```bash
   export OPENAI_API_KEY="your_api_key_here"
   ```

4. Launch the Jupyter notebook and follow the steps:  
   ```bash
   jupyter notebook LLM_FineTuning_pynb.ipynb
   ```

## 📊 Expected Output

When you input a complaint, the fine-tuned model returns a JSON object:

```json
{
  "topic": "Internet",
  "problem": "Slow connection during evening hours",
  "dissatisfaction_index": 75
}
```

## 👤 Author

Joel Joshi

## 📜 License

This project is for educational purposes. For commercial use, please refer to OpenAI’s terms of service.
