# 🧠 AI Literacy Final Project – Fake News Detector

**Author:** Sigitas Blechertas  
**Course:** AI Literacy – Turing College  
**Date:** [Insert Date]

---

## 1. Problem Definition

**Who:** Internet users and students  
**What:** Struggle to identify fake or misleading online news  
**Why it matters:** Misinformation spreads rapidly, leading to false beliefs and wasted time  
**Success Metric:** Achieve ≥85% precision in classifying fake vs real news articles

> Example formula:  
> [Who] struggle with [what], which causes [impact]. Success = [metric].

✅ *Example (yours):*  
“Internet users struggle to verify online news credibility, leading to misinformation and wasted time.  
Success = precision ≥85% compared to fact-checked sources.”

---

## 2. Current Approach & Its Limits

| Current Process                                 | Limitation                                   | Impact               |
| ----------------------------------------------- | -------------------------------------------- | -------------------- |
| Users rely on intuition or random fact-checking | 5–10 minutes per article                     | Time-consuming       |
| No consistent reliability or scoring            | Different people reach different conclusions | Inconsistent results |
| Sharing links with third-party checkers         | May expose personal data                     | Privacy concerns     |

---

## 3. How AI Will Help (Core Idea)

AI will automatically analyse and classify whether a news article is **Real** or **Suspicious** using labelled datasets such as *FakeNewsNet* on Nexos.ai.

**Input:** Article text or URL  
**Output:** Label (Real/Fake), Confidence (0–100%), Short rationale  
**Model(s):** Compare Claude 3.5 vs GPT‑4 Turbo  
**Human oversight:** Articles below 70% confidence are reviewed manually  
**Metric target:** F1 ≥ 0.8, Precision ≥ 0.85

---

## 4. Solution Workflow on Nexos.ai

| Step | Nexos Tool           | Description                                                                      |
| ---- | -------------------- | -------------------------------------------------------------------------------- |
| 1    | **Project**          | Create workspace; upload dataset (20–50 news samples)                            |
| 2    | **Compare Models**   | Evaluate multiple LLMs on the same dataset                                       |
| 3    | **Assistant**        | Build “Fake News Detector” chatbot for users to input text                       |
| 4    | **Guidelines**       | Enforce rules: rationale required, must include disclaimer, avoid political bias |
| 5    | **Testing**          | Input unseen examples; record predictions and confidence                         |
| 6    | **Evaluation Table** | Summarise metrics and misclassifications                                         |

---

## 5. Prompt Template (Structured Interaction Plan)

**System Prompt:**  
> You are a fake-news analysis expert.  
> Given an article, decide if it is Real or Suspicious.  
> Return:  
> • Label (Real/Fake)  
> • Confidence (0–100%)  
> • Three short reasons based on claim consistency, emotional tone, and factual cues  
> • Disclaimer: “AI output — verify with fact-checking sources.”

---

## 6. Evaluation Method & Quality Criteria

| Metric            | Formula                     | Target | Notes                      |
| ----------------- | --------------------------- | ------ | -------------------------- |
| Accuracy          | Correct predictions / total | ≥ 0.80 | Model reliability          |
| Precision         | TP / (TP + FP)              | ≥ 0.85 | Correctness of Fake labels |
| Recall            | TP / (TP + FN)              | ≥ 0.75 | Fake coverage              |
| Human Review Rate | Low-confidence cases (%)    | ≤ 15%  | Human-in-loop threshold    |

**Evidence required:**  
✅ 3–5 screenshots of model outputs showing predictions + confidence scores  
✅ Comparison summary from Nexos “Compare Models” page

---

## 7. Results (Screenshots & Table)

| Example ID | True Label | Predicted Label | Confidence | Comment                 |
| ---------- | ---------- | --------------- | ---------- | ----------------------- |
| 1          | Fake       | Fake            | 91%        | ✅ Correct               |
| 2          | Real       | Suspicious      | 68%        | ⚠ Human review required |
| 3          | Fake       | Real            | 44%        | ❌ Misclassified         |

> Insert 3–5 screenshots from Nexos results here.

---

## 8. Risks & Mitigation

| Risk                     | Impact               | Mitigation                                     |
| ------------------------ | -------------------- | ---------------------------------------------- |
| Political or source bias | Wrong classification | Use neutral dataset, display transparency note |
| Data privacy             | Exposed user URLs    | Use text snippets only, anonymise inputs       |
| Over-confidence          | Misleading trust     | Show uncertainty + disclaimer                  |
| Misuse (e.g. censorship) | Ethical misuse       | Require human review for any action            |

---

## 9. Privacy & Ethical Statement

No personal or confidential data is used.  
All article texts are anonymised before analysis.  
System adds an automatic disclaimer to all outputs:  
> “AI output — verify with fact-checking sources.”

---

## 10. Conclusion & Next Steps

✅ Problem defined with measurable success criteria  
✅ Solution workflow implemented in Nexos.ai  
✅ Models compared and evaluated  
✅ Risks and ethical concerns addressed

**Next Steps:**  
- Expand dataset size for generalisation  
- Add multilingual support for non-English news  
- Integrate automated API for real-time analysis

---

## 11. Appendix (Optional)

Attach:  
- Screenshots of Nexos workspace  
- “Compare Models” result  
- Assistant chat demonstration  
- Evaluation summary table

---
