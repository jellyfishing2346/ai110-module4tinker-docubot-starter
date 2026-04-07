# DocuBot Tinker Activity Summary

## 1. Environment Setup
- Installed all dependencies and configured the `.env` file with my Gemini API key.
- Resolved Python environment issues and confirmed LLM features are enabled.

## 2. Documentation and Code Exploration
- Skimmed the `docs/` folder to understand what information is available.
- Reviewed `docubot.py` and `main.py` to understand how DocuBot works.

## 3. Running DocuBot in Different Modes

### Naive LLM Mode
- The LLM answered all questions, even when the docs didn’t contain the answer.
- Some answers were plausible but not grounded in the actual documentation (hallucinations).

### Retrieval Only Mode
- DocuBot only answered if the information was found in the docs.
- If not found, it responded: “I do not know based on these docs.”
- No hallucinations, but sometimes too strict.

### RAG Mode
- The LLM only answered using retrieved snippets from the docs.
- If nothing relevant was found, it refused to answer.
- Combined fluency with accuracy when the docs contained the answer.

## 4. Comparison and Reflection

| Mode              | Hallucination Risk | Answers if Not in Docs | Trustworthiness |
|-------------------|-------------------|-----------------------|-----------------|
| Naive LLM         | High              | Yes                   | Low             |
| Retrieval Only    | None              | No                    | High            |
| RAG               | None              | No                    | High            |

- **Retrieval and RAG modes** are much more reliable because they only answer when the docs support it.
- **Naive LLM mode** can sound confident but may provide incorrect or unsupported answers.
- **RAG mode** is the best of both worlds: fluent, but only when grounded in real documentation.

---

*This summary reflects my experience completing the DocuBot Tinker activity. I am ready to discuss the differences between the modes and the importance of retrieval for trustworthy AI answers.*
