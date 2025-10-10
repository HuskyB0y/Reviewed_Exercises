# 🧠 AI Literacy Final Project – Fake News Detector

**Author:** Sigitas Blechertas  
**Course:** AI Literacy – Turing College  
**Date:** [Insert Date]

---

## 1. Problem Definition

**Who:** Internet users and students  
**What:** Struggle to identify fake or misleading online news  
**Impact:** Leads to misinformation, wasted time, and loss of trust in online content  
**Success Criteria:** ≥85% precision in detecting fake articles vs. known fact-checked data

---

## 2. Current Approach & Limits

| Current Behaviour                         | Limitation                            | Impact                    |
| ----------------------------------------- | ------------------------------------- | ------------------------- |
| Rely on intuition or random fact-checking | Time-consuming (5–10 min per article) | Inconsistent accuracy     |
| Manual searches on fact-check sites       | Limited coverage                      | Misses emerging fake news |
| No clear scoring or explanation           | User confusion                        | Trust issues              |

---

## 3. How AI Will Help (Core Idea)

AI will:  
Detect and classify whether a given news article text is **Real** or **Suspicious**, using Nexos.ai models trained on labelled datasets (e.g., *FakeNewsNet*).

**Input:** Article text or URL  
**Output:** Label (Real/Fake), Confidence score, and Short rationale

**Quality Check:** F1 ≥ 0.8 on validation set  
**Human-in-loop:** Manual review for low-confidence (<70%) results

---

## 4. Solution Workflow on Nexos

| Step | Tool             | Purpose                                                           |
| ---- | ---------------- | ----------------------------------------------------------------- |
| 1    | Nexos Project    | Create workspace, upload small dataset (20–50 samples)            |
| 2    | Compare Models   | Test multiple LLMs (Claude 3.5 vs GPT‑4 Turbo)                    |
| 3    | Assistant        | Build “Fake News Detector” chatbot where user pastes article text |
| 4    | Guidelines       | Add rules: rationale + disclaimer; no political bias              |
| 5    | Testing          | Input unseen examples, log confidence scores                      |
| 6    | Evaluation Table | Summarise accuracy, precision, recall, and misclassified samples  |

---

## 5. Example Prompt Template

**System Prompt:**  
> You are a fake‑news analysis expert.  
> Given an article, decide if it is Real or Suspicious.  
> Return:
> - Label (Real/Fake)  
> - Confidence (0–100%)  
> - Three short reasons based on claim consistency, emotional tone, and factual cues.  
> - Disclaimer: “AI output — verify with fact‑checking sources.”

---

## 6. Evaluation Method

| Metric            | Description                   | Target |
| ----------------- | ----------------------------- | ------ |
| Accuracy          | Correct predictions / total   | ≥ 0.80 |
| Precision         | Correct Real/Fake predictions | ≥ 0.85 |
| Recall            | Coverage of fake news         | ≥ 0.75 |
| Human review rate | % of low‑confidence cases     | ≤ 15%  |

**Include screenshots:** 3–5 test runs with predicted labels + confidence scores.

---

## 7. Results Section

| Example ID | True Label | Predicted  | Confidence | Notes              |
| ---------- | ---------- | ---------- | ---------- | ------------------ |
| 1          | Fake       | Fake       | 91%        | Correct            |
| 2          | Real       | Suspicious | 68%        | Needs human review |
| ...        | ...        | ...        | ...        | ...                |

---

## 8. Risks & Mitigation

| Risk                     | Impact                 | Mitigation                                        |
| ------------------------ | ---------------------- | ------------------------------------------------- |
| Political or source bias | Wrong labels           | Train/test on neutral data; add transparency note |
| Data privacy             | Sharing links publicly | Use anonymised text snippets only                 |
| Over‑confidence          | Misleading users       | Display uncertainty + disclaimer                  |
| Misuse (e.g. censorship) | Ethical risk           | Require human review before action                |

---

## 9. Privacy & Ethical Considerations

All data will be anonymised before uploading to Nexos.  
The model will not store URLs or identifiable information.  
The chatbot includes a disclaimer: “AI output — verify with fact‑checking sources.”

---

## 10. Conclusion & Next Steps

✅ Problem defined and metrics established  
✅ Workflow tested on Nexos.ai  
✅ Preliminary results recorded  
✅ Ethical and privacy considerations reviewed  

**Next steps:**  
- Expand dataset beyond 50 samples  
- Compare more models for consistency  
- Deploy small demo chatbot version  

---

**Appendix:**  
Attach screenshots of Nexos workspace, Compare Models, Assistant chat demo, and Evaluation Table.

---
