# Sentiment Analysis Using Prompt Engineering

## Problem Statement
An online shopping company wants to analyze customer reviews automatically to
understand customer satisfaction. This project designs a prompt that classifies
each customer review by its overall sentiment.

- **Input:** a customer review in natural language
- **Output:** a single word, with no explanation or additional text
- **Allowed outputs:** Positive, Negative, Neutral

## Repository Structure
| File | Purpose |
|---|---|
| `prompt.txt` | The sentiment classification prompt |
| `test_cases.csv` | 30 test reviews with expected labels |
| `README.md` | Project documentation and test results |

## The Prompt
```
(paste the full contents of prompt.txt here)
```

## Design Choices
- **Role and task:** defines the model's job clearly.
- **Label definitions:** removes ambiguity about what each label means.
- **Mixed-review rule:** decides how to label reviews with both praise and complaints, such as "The phone is good, but the battery life is terrible."
- **Negation and sarcasm handling:** covers phrases like "not bad" and "oh great, it broke".
- **Facts are Neutral:** statements of fact without opinion are labelled Neutral.
- **Few-shot examples:** the 7 given examples anchor the output format.
- **Strict output rules:** force a single word with no extra text.
- **Injection guard:** the review is treated as data, so instructions inside it are ignored.

## How to Use
1. Copy the contents of `prompt.txt` into any LLM chat (for example ChatGPT or Claude).
2. Replace `{{customer_review}}` on the last line with the review.
3. The model replies with exactly one word: Positive, Negative or Neutral.

## Test Results
- **Model/tool used:** (fill in)
- **Testing method:** (fill in)
- **Result:** (fill in)/30 correct

(results table goes here)

## Additional Tests (Unseen Reviews)
(to be added after the first round)

## Limitations
- No prompt can guarantee 100% accuracy; sentiment is subjective, and mixed reviews may reasonably be labelled either way.
- Results depend on the model and settings used.
- Reviews were tested in one batch, so earlier reviews may have influenced later answers.
- The test set is small and written by the author, so a perfect score here does not guarantee the same on real customer data.
