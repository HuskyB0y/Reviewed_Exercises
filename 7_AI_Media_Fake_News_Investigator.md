
# 🧠 AI Media Fake News Investigator – Fake News Detector  
### Turing College – AI Literacy Final Project  

---

## 🎯 Project Overview
This project presents a **single expert-level AI assistant** built with the **Nexos.ai** platform.  
The assistant — **AI Media Fake News Investigator** — analyses online information to detect **fake news, bias, propaganda, and harmful narratives**, while keeping its internal reasoning hidden for clarity and safety.

It evolved from an earlier multi-agent setup (Fact Checker, Bias Analyst, Propaganda Detector, Aggregator) into one refined, self-contained model.  
The design focuses on reliable scoring, ethical operation, and concise, explainable outputs.

---

## 🤖 Assistant Description

### 🕵️ Role: AI Media Fake News Investigator
**Purpose:** Examine text or web links for factual accuracy, neutrality, propaganda intent, safety, and negative influence.  
**Platform:** Nexos.ai  
**Models tested:** GPT-5, Claude Opus, Gemini 2.5 Pro, Mistral 7B  
**Output:** Final numeric scores and a short factual summary — no reasoning displayed.

---

## ⚙️ Output Structure

| Field                         | Description                                                   |
| ----------------------------- | ------------------------------------------------------------- |
| **Credibility Score (0–100)** | Factual correctness (0 = false / fabricated, 100 = verified). |
| **Neutrality Score (0–100)**  | Degree of balance and absence of bias.                        |
| **Propaganda Score (0–100)**  | Presence of manipulative or ideological patterns.             |
| **Safety Score (0–100)**      | Reliability of source and domain safety.                      |
| **Propaganda Direction**      | If detected — which side or ideology it supports.             |
| **Negative Influence**        | Whether the content promotes war, hate, fear, or division.    |
| **Summary**                   | One short, neutral verdict (max ≈ 15 words).                  |
| **Sources Checked**           | Verification references or “no data available.”               |
| **Warnings**                  | Notes on unsafe links or unverifiable content.                |

---

## 🧩 Example Outputs

### Example 1 – Satirical / Fake News  
![onion_news](Resources/Capstone_project/onion_news.png)

**Input:** [The Onion – “Limbless Slippery RFK Jr…”](https://www.theonion.com/limbless-slippery-rfk-jr-becoming-an-eel-is-a-sign-of-good-health/)

- Credibility Score: 0  
- Neutrality Score: 50  
- Propaganda Score: 10  
- Safety Score: 100  
- Propaganda Direction: Not applicable  
- Negative Influence: Does not promote war, hate, or fear.  
- **Summary:** Satirical content. Intentionally false for comedic effect.  
- Sources Checked: Information about The Onion as a satire website.  
- Warnings: None  

---

### Example 2 – Verified Real News  
![delfi](Resources/Capstone_project/delfi.png)

**Input:** [Delfi – “Lietuviškojo Taurus šarvuočio detektyvas…”](https://www.delfi.lt/saugu/ekonomika/lietuviskojo-taurus-sarvuocio-detektyvas-tesiasi-policija-pradejo-ikiteismini-tyrima-120159535)

- Credibility Score: 90  
- Neutrality Score: 75  
- Propaganda Score: 15  
- Safety Score: 95  
- Propaganda Direction: Not applicable  
- Negative Influence: Does not promote war, hate, or fear.  
- **Summary:** Reliable news reporting on a factual event with minor editorial bias.  
- Sources Checked: Reputation of *delfi.lt* and related articles.  
- Warnings: None  

---

### Example 3 – Limited Access / Lifestyle Content  
![15min](Resources/Capstone_project/15min.png)

**Input:** [15min – Article on relationships](https://www.15min.lt/gyvenimas/naujiena/santykiai/issiskyrusi-karina-atsikrate-tabu-nauja-meile-sutiko-svingeriu-klube-atvirai-ka-reiskia-tokie-santykiai-1024-2540832)

- Credibility Score: 50  
- Neutrality Score: 50  
- Propaganda Score: 50  
- Safety Score: 95  
- Propaganda Direction: Not applicable  
- Negative Influence: Not determinable due to restricted content.  
- **Summary:** Could not fully analyse; source is a verified news portal.  
- Sources Checked: No verification data available.  
- Warnings: None  

---

### Example 4 – Ideologically Biased News (War Topic)  
![fox_news](Resources/Capstone_project/fox_news.png)

**Input:** [Fox News – Ukraine conflict coverage](https://www.foxnews.com/category/world/conflicts/ukraine)

- Credibility Score: 30  
- Neutrality Score: 10  
- Propaganda Score: 80  
- Safety Score: 60  
- Propaganda Direction: Right / Conservative  
- Negative Influence: Promotes misinformation and social division.  
- **Summary:** Highly biased coverage with recurrent propaganda themes.  
- Sources Checked: Search results on “Fox News reliability and bias.”  
- Warnings: None  

---

### Example 5 – Malicious / Phishing Link  
![netflix](Resources/Capstone_project/netflix.png)

**Input:** [Fake Netflix Login Page](http://www.netflix-login-update.cc/verify-account/us007)

- Credibility Score: 0  
- Neutrality Score: 0  
- Propaganda Score: 100  
- Safety Score: 0  
- Propaganda Direction: Financial fraud / Data theft  
- Negative Influence: Promotes identity and financial fraud.  
- **Summary:** Phishing attempt. Highly deceptive and unsafe.  
- Sources Checked: Articles on Netflix phishing scams and official security advice.  
- Warnings: Unsafe and malicious — do not visit.  

---

## 🧠 Design Principles
- Unified multi-disciplinary analysis (fact-checking, bias, safety, propaganda).  
- Ethical AI behaviour — no hallucinated data or exposed reasoning.  
- Concise, measurable results for easy comparison.  
- Entirely no-code implementation in Nexos.ai.  
- Fully aligned with AI Literacy learning goals: reasoning, transparency, risk awareness.  

---

## 🧪 Testing Procedure
1. Paste a text or link into Nexos for the AI Media Fake News Investigator.  
2. Wait for the assistant to generate scores and a short summary.  
3. Compare fake vs real vs propaganda sources.  
4. Record scores and screenshots.  
5. Reflect on strengths and weaknesses observed across tests.  

---

## 🧭 Reflection
The original four-assistant architecture (Fact Checker, Bias Analyst, Propaganda Detector, Aggregator) was merged into a single refined model performing all roles simultaneously.  
This simplified the workflow, eliminated redundancy, and improved result consistency.

**Key learnings**
- Prompt design has greater impact than model choice for this task.  
- LLMs can support digital literacy and fact-checking but still need human oversight.  
- Concealing reasoning reduces hallucination risk and keeps outputs clear.  

---

## 📁 Submission Checklist

| Item                                      | Status             |
| ----------------------------------------- | ------------------ |
| Nexos project created                     | ✅                  |
| Unified assistant prompt implemented      | ✅                  |
| Tests with fake / real / propaganda links | ✅                  |
| Screenshots of outputs                    | ✅                  |
| README.md (this file)                     | ✅ Ready for upload |

---

**Author:** Sigitas Blechertas  
**Date:** October 2025  
**Course:** Turing College – AI Literacy Final Project  
**Project:** AI Media Fake News Investigator (Fake News Detection System)
