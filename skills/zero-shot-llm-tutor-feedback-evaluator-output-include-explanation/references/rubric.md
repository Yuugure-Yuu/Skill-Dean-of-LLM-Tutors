# LLM Feedback Annotation Rubric

Complete scoring rubric for all 16 evaluation dimensions.

---

## Dimensions with scores 0 / 1 / 2

### 1. Alignment with Goal
Evaluates to what extent most comments are aligned to specific goals.
- **Score 0**: No reference to assignment goals in specific comments.
- **Score 1**: References goals partly and vaguely.
- **Score 2**: References goals clearly in most comments.

### 2. Specificity
- **Score 0**: Most comments have low-level specifics (e.g., broad area noted) and lack illustrative examples.
- **Score 1**: Some comments have moderate specifics, some are not. No concrete example(s) of how to improve.
- **Score 2**: All comments offer detailed, actionable guidance, and the feedback includes any concrete example(s) of how to improve.

### 3. Motivational Tone
- **Score 0**: Tone is negative, discouraging, or disrespectful, containing many negative elements.
- **Score 1**: Tone is generally neutral with occasional positive or encouraging elements, but not positive all the way.
- **Score 2**: Tone is consistently positive, encouraging, and respectful.

### 4. Strength
- **Score 0**: No strength mentioned.
- **Score 1**: Mention general strength of the assignment, but no specifics.
- **Score 2**: Mention strength of specific aspect(s) of the assignment.

### 5. Weakness
- **Score 0**: No weakness mentioned explicitly.
- **Score 1**: Mention general weakness of the assignment, but no specifics.
- **Score 2**: Mention weakness of specific aspect(s) of the assignment.

### 13. Clarity and Understandability
Measures how clear and easy to understand the language is.
- **Score 0**: Unclear and Confusing — difficult to understand, with ambiguous or vague language.
- **Score 1**: Generally Clear and Understandable — mostly straightforward, but may require some context.
- **Score 2**: Crystal Clear and Intuitive — concise, well-structured, perfectly clear, easily accessible.

---

## Dimensions with scores 0 / 1 (binary presence)

### 6. Feed Forward
"Where to next?" — next steps in learning, next tasks and activities, or how to improve the assignment.
- **Score 0**: Feedback does not contain Feed forward.
- **Score 1**: Feedback contains Feed forward.

### 7. Feed Up
"Where am I going?" — reminders about goals, judgements about success in goal attainment, increasing learners' awareness of goals.
- **Score 0**: Feedback does not contain Feed up.
- **Score 1**: Feedback contains Feed up.

### 8. Feed Back
"How am I going?" — student's progress towards achieving the learning goal; comments on errors and correct forms.
- **Score 0**: Feedback does not contain Feed back.
- **Score 1**: Feedback contains Feed back.

### 9. Feedback on Task
Feedback about how well a task is being accomplished or performed: distinguishing correct from incorrect answers, acquiring more or different information, building surface knowledge.
- **Score 0**: Feedback does not contain Feedback on task.
- **Score 1**: Feedback contains Feedback on task.

### 10. Feedback on Process
Directive developmental guidance directed at the process used to create a product or complete a task; directed to information processing or learning processes required to understand or complete the task.
- **Score 0**: Feedback does not contain Feedback on process.
- **Score 1**: Feedback contains Feedback on process.

### 11. Feedback on Self-Regulation
Informative developmental guidance focused on self-assessment or confidence skills; addresses self-monitoring, self-direction, and self-discipline; provides cues or prompts to help students plan, monitor, and evaluate their strategies and efforts.
- **Score 0**: Feedback does not contain Feedback on self-regulation.
- **Score 1**: Feedback contains Feedback on self-regulation.

### 12. Feedback on Self
Feedback directed to the person/self, often unrelated to task performance.
- **Score 0**: Feedback does not contain Feedback on self.
- **Score 1**: Feedback contains Feedback on self.

---

## Hallucination Dimensions (scores 0 / 1)

> If one hallucination belongs to multiple types, score ALL affected dimensions as 1.

### 14. Input-Conflicting Hallucinations
Tutor feedback conflicts with the student assignment, assignment description, or feedback generation instructions (e.g., misquoting student work, attributing incorrect content to the student, misrepresenting the assignment task).
- **Score 0**: No Input-Conflicting Hallucinations.
- **Score 1**: Input-Conflicting Hallucinations exist.

### 15. Context-Conflicting Hallucinations
Tutor feedback contains contradictory information within itself (self-contradictions within the same feedback).
- **Score 0**: No Context-Conflicting Hallucinations.
- **Score 1**: Context-Conflicting Hallucinations exist.

### 16. Fact-Conflicting Hallucinations
Tutor feedback contradicts established real-world facts (e.g., incorrect domain knowledge claims).
- **Score 0**: No Fact-Conflicting Hallucinations.
- **Score 1**: Fact-Conflicting Hallucinations exist.
