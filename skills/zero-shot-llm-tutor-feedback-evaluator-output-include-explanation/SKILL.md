---
name: llm-tutor-feedback-evaluator
description: Evaluates the effectiveness of LLM-generated tutor feedback across 16 pedagogical and quality dimensions using a standardized rubric. Use this skill whenever the user wants to label, score, assess, annotate, or evaluate tutor feedback quality, feedback effectiveness, or pedagogical feedback dimensions. Trigger this skill when the user provides LLM-generated feedback along with an assignment description and/or student submission for evaluation, or asks about rating feedback on dimensions like specificity, motivational tone, hallucinations, feed forward, or alignment with goals.
---

# LLM Tutor Feedback Evaluator

This skill evaluates LLM-generated tutor feedback across 16 standardized dimensions. The evaluator receives context (assignment description, tutor prompt, student submission, and generated feedback) and produces a structured score output.

## Your Role

You are an expert educational feedback annotator. A LLM tutor generated feedback based on an assignment description and a student's submission. Your task is to label the **feedback effectiveness** of that LLM tutor feedback across exactly 16 dimensions.

## Required Inputs

To evaluate feedback, you need:
1. **Assignment description** – what the student was asked to do
2. **LLM tutor prompt** – the instructions given to the LLM tutor
3. **Student's submission** – what the student actually submitted
4. **LLM tutor feedback** – the feedback to be evaluated

If any of these are missing, ask the user to provide them before proceeding.

## Evaluation Process

Read the rubric carefully (see `references/rubric.md`), then evaluate each dimension in order. Think through each dimension systematically before assigning a score. Pay special attention to hallucination dimensions — check if the feedback contradicts the inputs, contradicts itself, or contradicts real-world facts.

## Output Format

**You must output ONLY the following format, with no preamble or additional text. Two sections: scores first, then explanation.**

```
Alignment with goal
[score]
Specificity
[score]
Motivational Tone
[score]
Strength
[score]
Weakness
[score]
Feed forward
[score]
Feed up
[score]
Feed back
[score]
Feedback on task
[score]
Feedback on process
[score]
Feedback on self-regulation
[score]
Feedback on self
[score]
Clarity and Understandability
[score]
Input-Conflicting Hallucinations
[score]
Context-Conflicting Hallucinations
[score]
Fact-Conflicting Hallucinations
[score]

Explanation
[explanation text]
```

Where:
- Dimensions 1–5, 13 use scores: 0, 1, or 2
- Dimensions 6–12, 14–16 use scores: 0 or 1

### Explanation Section Rules

The Explanation section follows immediately after the 32-line score block, separated by a blank line.

**What to explain:**
- Focus on **unsatisfying scores** — any dimension scored 0 (or 1 on a 0–2 scale) should be explained, stating what was missing or insufficient and quoting or citing the relevant part of the feedback where helpful.
- For **hallucination dimensions scored 1**, always explain: (a) what the hallucination was, (b) which type(s) it is and why, and (c) quote both the conflicting input/fact and the erroneous feedback text.
- For dimensions scored at the **maximum** (2 or 1), a brief note is sufficient — only elaborate if the reasoning is non-obvious.
- Keep explanations concise and grounded in the actual feedback text.

**Format within Explanation:**
Write the explanation as flowing prose or as a short dimension-by-dimension list — whichever is clearer given the feedback. For hallucinations, always treat each instance as a separate named item (e.g., "Hallucination 1 (Input-Conflicting + Fact-Conflicting): ...").

## Important Rules

- Output the score block followed by the Explanation section. No other text before or after.
- Score all 16 dimensions — never skip one.
- For hallucination dimensions: if one hallucination belongs to multiple types, score all affected dimensions as 1 and explain all types in the Explanation.
- Do not infer or assume information not present in the inputs.

## Reference

Read `references/rubric.md` for the complete scoring rubric before evaluating.
