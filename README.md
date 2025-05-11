# Business-Specific RAG Chat Interface  
*Built with LangFlow & DataStax Astra DB*


## 📖 Overview  
This project implements a secure Retrieval-Augmented Generation (RAG) system using **LangFlow** and **DataStax Astra DB** for querying internal business data that is not exposed to public LLMs. It supports synonym mapping, glossary integration, and real-time API responses.

---

## ✨ Key Features  
- **Visual RAG Pipeline** via LangFlow  
- **Astra DB Vector Search** for fast, private semantic retrieval  
- **Custom Glossary Mapping** to interpret internal business terms

---

## 🧠 Workflow  
1. **Ingest Data**: Upload internal PDFs/CSVs into LangFlow  
2. **Vectorize**: Convert terms into embeddings and store in Astra DB  
3. **Query & Respond**: Use natural language to retrieve relevant context → generate answers

---

## 🔬 Demo Example: Medical Use Case  

**Glossary Term Example**  
| Term         | Meaning                                                        |
|--------------|----------------------------------------------------------------|
| Coalin 10XR  | Narrowing of the stomach outlet due to scarring/inflammation  |

- Vectorized only `condition` terms across `patients`, `conditions`, `visits` collections  
- Terms like "Coalin 10XR" are random to ensure retrieval happens solely via vector search, not LLM memory

**User Query**:  
*"Does Coalin 10XR have a treatment plan in any patient record?"*
