# 🥑 AI Nutrition Expert: Multimodal Prompt Engineering & Evaluation

A high-performance nutritional analysis system based on **Large Language Models (LLMs)**, enabling precise calorie and macronutrient tracking. The system processes text descriptions and images (e.g., food labels) using **Multimodal RAG** and **OCR** technology.

---

## 🚀 Key Features

- **Multimodal Intelligence**: Real-time analysis of food labels and meal images powered by **Gemini 3 Flash**.
- **Automated Evaluation**: 100% test coverage for core logic using **promptfoo**, ensuring mathematical accuracy.
- **Advanced Guardrails**: Hardened against **Prompt Injection** and adversarial persona-breaking attempts.
- **Model Benchmarking**: Comparative analysis between **Gemini 3 Flash** and **GPT-4o-mini** regarding precision, latency, and cost.

---

## 🛠 Advanced Prompt Engineering Techniques

| Technique                  | Implementation            | Goal                                                       |
| :------------------------- | :------------------------ | :--------------------------------------------------------- |
| **Chain of Thought (CoT)** | `<thought_process>` block | Eliminating mathematical hallucinations.                   |
| **Self-Reflection**        | Self-verification loop    | Auditing results before final output.                      |
| **Few-Shot Prompting**     | Contextual examples       | Enforcing rigid Markdown table structures.                 |
| **Persona Pattern**        | "Expert Nutritionist"     | Maintaining professional boundaries and attack resistance. |

---

## 📊 Evaluation & Quality (LLMOps)

The system utilizes the **promptfoo** framework to automate testing and ensure quality in the production cycle:

- **Deterministic Validation**: JS scripts verify that the sum of proteins, fats, and carbs matches the product weight.
- **Semantic Consistency**: Regex assertions ensure the model always considers the "Training Day" context.
- **Security Testing**: Negative assertions block attempts to exit the assigned role (e.g., "Developer" or "Pirate" modes).

---

## 🏗 Project Structure

    ai_project/
    ├── core/                 # Master System Prompts
    │   └── system_prompt.md
    ├── evaluation/           # PromptFoo test suites & assets
    │   ├── images/           # OCR samples for multimodal testing
    │   └── promptfooconfig.yaml
    ├── monitoring/           # Observability (LangFuse Integration)
    ├── .env                  # API Keys (Protected via .gitignore)
    └── README.md             # Technical documentation

---

## ⚙️ Getting Started

### Prerequisites

- **Node.js (v18+)**: Essential for running the evaluation framework.
  - **On Windows/macOS/Linux**: It is highly recommended to use **nvm** (Node Version Manager).
    1. Install nvm from [github.com/nvm-sh/nvm](https://github.com/nvm-sh/nvm).
    2. Run: `nvm install node` to get the latest version.
  - **Alternative**: Download the "LTS" (Long Term Support) installer directly from the [official Node.js website](https://nodejs.org/).
- **promptfoo CLI**: Install globally once Node.js is ready:
  `npm install -g promptfoo`
- **Active API keys**: Required for **Google AI Studio (Gemini)** or **OpenAI**.

### Installation & Setup

1. **Clone the repository**:
   `git clone https://github.com/your-username/ai-nutrition-expert.git`

2. **Configure the .env file** in the root directory:
   `GOOGLE_API_KEY=your_key_here`
   `OPENAI_API_KEY=your_key_here`

### Running Evaluations

1. **Execute the test suite**:
   `promptfoo eval -c evaluation/promptfooconfig.yaml`

2. **View the results**:
   `promptfoo view`

---

## 📈 Roadmap

- [ ] **LangFuse Integration**: Implementation of production-grade tracing and observability.
- [ ] **Multimodal Expansion**: Dataset growth to include handwritten meal logs and complex restaurant menus.
- [ ] **LLM-as-a-Judge**: Automated analysis of response tone and empathy.
- [ ] **Technical Summary**: Preparation of the "About" section for GitHub.
- [ ] **LinkedIn Promotion**: Crafting a post highlighting the use of `promptfoo` and `Gemini 3 Flash`.

---
