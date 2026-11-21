<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&color=0:0A0A0A,100:1E6FD9&height=160&section=header&text=Break%20Through%20Tech%20AI%2FML&fontSize=48&fontColor=FFFFFF&fontAlignY=40&desc=Cornell%20Tech%20Fellowship%20%C2%B7%20Pedrocia%20De-Sosoo&descSize=20&descAlignY=66" width="100%" alt="Break Through Tech AI/ML Fellowship" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-1E6FD9?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/scikit--learn-1E6FD9?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn" />
  <img src="https://img.shields.io/badge/TensorFlow-1E6FD9?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow" />
  <img src="https://img.shields.io/badge/LangChain-1E6FD9?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/OpenAI-1E6FD9?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI" />
</p>

My work from the **Break Through Tech AI/ML Fellowship at Cornell Tech**. It goes from classic machine learning (data prep, model selection, neural networks) to building with LLMs (multimodal extraction, RAG, and multi-agent systems).

## 📂 What's inside

| | Project | What I built | Tools |
|---|---|---|---|
| 🎓 | [**Labs 5–6 Capstone: Airbnb price classification**](capstone/Capstone.ipynb) | Predicted whether an Airbnb listing is high or low price. Went through the full ML life cycle: EDA, class imbalance, data prep, logistic regression tuned with GridSearchCV, then KNN and a neural network on the same problem to compare. | pandas, scikit-learn, Keras |
| 🧾 | [**Lab 7: Multimodal document extraction**](labs/ExtractAnalyzeDocumentsMultimodalLLMs.ipynb) | Pulled structured data out of expense receipt images with a multimodal LLM, checked the results with a second "self-reflection" LLM call, and analyzed spending patterns. | OpenAI API, pandas |
| 🔎 | [**Lab 8: Document RAG system**](labs/BuildingImprovingDocumentRAGSystem.ipynb) | Built a customer support RAG app for an outdoor gear company (chunking, embeddings, Chroma vector store), then improved retrieval by adding a query rewriting step. | LangChain, Chroma, OpenAI |
| 🤝 | [**Lab 9: Agentic pitch clinic**](labs/BuildingAgenticPitchClinic.ipynb) | Multi-agent system that routes a pitch to the right coach agent, then improves it with an evaluator-optimizer loop graded against a rubric served by my own MCP server. | OpenAI Agents SDK, MCP, Pydantic |
| ⚡ | [**Agentic coding workshop**](agentic_coding_workshop.ipynb) | Directed an AI coding assistant to clean data and predict hotel cancellations with logistic regression, checking its work at each step. | Gemini in Colab |

## 🎓 Capstone highlights

- **Format:** spanned Labs 5 and 6. Lab 5 covered logistic regression, and Lab 6 added a neural network after the unit on deep learning.
- **Problem:** binary classification of Airbnb listings as high or low price, using host behavior and review features.
- **Imbalanced data:** most listings were low price, so I used stratified splits and class weighting, and judged models on **F1**, not just accuracy.
- **Three models, same problem:**

  | Metric | Logistic regression (tuned, class-weighted) | KNN | Neural network |
  |---|---|---|---|
  | Accuracy | 0.567 | 0.715 | 0.749 |
  | F1 score | **0.435** | 0.346 | 0.156 |

- **Takeaway:** accuracy and F1 told opposite stories. The neural network had the highest accuracy but the worst F1, because it mostly predicted the majority class and missed most high-price listings. Class-weighted logistic regression had the lowest accuracy but the best F1, catching 65% of high-price listings. On imbalanced data, the simplest model was the most useful, and more complexity didn't mean a better model.
- **Ethics:** I looked at how location and host features can act as proxies for socioeconomic status or demographics, and who could be harmed by a biased pricing model.

## ▶️ Running the notebooks

The notebooks were built for the fellowship's course environment. Datasets aren't included in this repo. The LLM labs need an `OPENAI_API_KEY` set as an environment variable (never hard-coded).

---

<p align="center"><sub>More about me at <a href="https://github.com/pedrociadesosoo">github.com/pedrociadesosoo</a></sub></p>
