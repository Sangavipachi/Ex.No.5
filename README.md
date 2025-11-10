

# EXP 5: COMPARATIVE ANALYSIS OF DIFFERENT TYPES OF PROMPTING PATTERNS AND EXPLAIN WITH VARIOUS TEST SCENARIOS

# Aim: To test and compare how different pattern models respond to various prompts (broad or unstructured) versus basic prompts (clearer and more refined) across multiple scenarios.  Analyze the quality, accuracy, and depth of the generated responses 

### AI Tools Required: 

# Explanation: 

Here’s a **comprehensive 20-mark style answer** on the topic:

---

## **Comparative Analysis of Different Types of Prompting Patterns and Explanation with Test Scenarios**

### **Introduction**

Prompting refers to the way in which instructions, questions, or cues are given to an artificial intelligence model or learner to elicit the desired response. In the context of Artificial Intelligence (AI), Machine Learning (ML), and particularly Large Language Models (LLMs), **prompting patterns** determine how effectively a system understands and generates relevant, accurate, and context-aware outputs. A comparative analysis of different prompting techniques helps in identifying the most efficient strategies for various problem types and domains.

---

### **1. Types of Prompting Patterns**

#### **a) Zero-Shot Prompting**

**Definition:**
In zero-shot prompting, the model is given only the task description without any example. The model must use its pre-trained knowledge to generate the answer.

**Example Prompt:**
“Translate the following English sentence to French: *I am going to school.*”

**Advantages:**

* No prior examples required.
* Saves time and resources.
* Useful for general-purpose tasks.

**Limitations:**

* May produce inconsistent or inaccurate outputs for domain-specific tasks.

**Test Scenario:**

* *Input:* “Classify this review as positive or negative: ‘The product broke in two days.’”
* *Expected Output:* “Negative.”
* *Outcome:* Zero-shot may succeed if model understands sentiment well but can fail on complex, sarcastic inputs.

---

#### **b) One-Shot Prompting**

**Definition:**
One example is provided along with the instruction, giving the model a hint about the expected format or reasoning style.

**Example Prompt:**
“Translate English to French.
Example: English: I am happy → French: Je suis heureux.
Now translate: English: I am hungry.”

**Advantages:**

* Guides the model toward the expected output format.
* Helps with slightly more complex tasks than zero-shot.

**Limitations:**

* Single example may not capture all variations.

**Test Scenario:**

* *Task:* Classify emails as spam or not spam.
* *Example Input:* “Get a free trip now!” → *Spam.*
* *Test Input:* “Meeting agenda for tomorrow.”
* *Expected Output:* “Not spam.”

---

#### **c) Few-Shot Prompting**

**Definition:**
The model is provided with multiple examples (usually 2–10) showing input-output pairs before being asked to complete a new task.

**Example Prompt:**
“Summarize the following texts in one sentence:

1. Text: ‘The book describes life in rural India.’ → Summary: ‘It’s about rural Indian life.’
2. Text: ‘The movie tells the story of a young scientist.’ → Summary: ‘It’s about a young scientist.’
   Now summarize: ‘The novel portrays a queen’s rise to power.’”

**Advantages:**

* Higher accuracy and reliability.
* Better understanding of task pattern.

**Limitations:**

* Prompt length increases.
* Computationally more expensive.

**Test Scenario:**

* *Task:* Identify parts of speech in sentences.
* *Outcome:* Model performs better when given several labeled examples compared to zero/one-shot.

---

#### **d) Chain-of-Thought (CoT) Prompting**

**Definition:**
Encourages the model to **think step-by-step** before arriving at an answer. Useful for reasoning, mathematics, or logic-based questions.

**Example Prompt:**
“Q: A train travels 60 km in 1 hour. How far will it travel in 3 hours?
Let’s think step-by-step.”

**Advantages:**

* Improves logical consistency and interpretability.
* Helps the model explain its reasoning process.

**Limitations:**

* Longer outputs.
* Sometimes over-elaborates on simple tasks.

**Test Scenario:**

* *Task:* Math word problem or logical puzzle.
* *Outcome:* CoT improves accuracy on reasoning-heavy questions.

---

#### **e) Self-Consistency Prompting**

**Definition:**
The model is prompted multiple times with slightly varied CoT prompts, and the most consistent or majority answer is selected.

**Advantages:**

* Enhances reliability.
* Reduces random errors in reasoning tasks.

**Limitations:**

* Computationally expensive.

**Test Scenario:**

* *Task:* Solving riddles or multi-step problems.
* *Outcome:* The correct answer is chosen from multiple reasoning paths.

---

#### **f) Instruction Prompting**

**Definition:**
The prompt is framed as a **clear directive** — explaining what is to be done, what format to use, and how to respond.

**Example Prompt:**
“You are an expert accountant. Explain the difference between accrual and cash accounting in three bullet points.”

**Advantages:**

* High clarity.
* Effective for professional and structured tasks.

**Limitations:**

* May restrict creative or open-ended responses.

**Test Scenario:**

* *Task:* Write a business summary or report section.
* *Outcome:* Consistent, professional tone and structure.

---

#### **g) Role-Based Prompting**

**Definition:**
The model is assigned a **specific role or persona** to influence tone and style of response.

**Example Prompt:**
“Act as a cybersecurity expert and explain phishing attacks to beginners.”

**Advantages:**

* Ensures domain-specific context.
* Produces specialized and stylistically appropriate answers.

**Limitations:**

* Requires domain knowledge.
* May generate biased content if role not well-defined.

**Test Scenario:**

* *Task:* Customer support simulation.
* *Outcome:* Model adapts tone (polite, informative, empathetic) as expected.

---


### **3. Test Scenarios Summary**

1. **Text Classification:** Few-shot and instruction prompting outperform zero-shot.
2. **Mathematical Reasoning:** Chain-of-thought and self-consistency provide best accuracy.
3. **Creative Writing:** Role-based and few-shot prompting yield better contextual depth.
4. **Translation Tasks:** One-shot or few-shot prompting improves linguistic precision.
5. **Professional Reports:** Instruction prompting ensures structured, formal responses.

---

---


# OUTPUT
| Prompt Type       | Context Examples | Complexity | Accuracy  | Ideal Use Case                |
| ----------------- | ---------------- | ---------- | --------- | ----------------------------- |
| Zero-shot         | None             | Low        | Moderate  | General tasks                 |
| One-shot          | 1 Example        | Low        | Moderate+ | Simple pattern tasks          |
| Few-shot          | 2–10 Examples    | Medium     | High      | Classification, summarization |
| Chain-of-Thought  | Step reasoning   | High       | Very High | Logical or math reasoning     |
| Self-Consistency  | Multiple CoT     | Very High  | Very High | Complex problem-solving       |
| Instruction-based | Clear directive  | Medium     | High      | Professional outputs          |
| Role-based        | Persona assigned | Medium     | High      | Domain-specific communication |

# RESULT: The prompt for the above said problem executed successfully
Different prompting patterns serve different purposes depending on task complexity, data availability, and required accuracy. While zero-shot is efficient for general tasks, few-shot and chain-of-thought prompting demonstrate superior performance for structured reasoning and domain-specific contexts. The evolution from simple to advanced prompting patterns reflects a shift toward context-aware, structured, and explainable AI behavior, making prompt engineering a vital skill in AI interaction and performance optimization.
