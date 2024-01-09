LLM Benchmarks: What Do They All Mean?
---

**21 LLM benchmarks: The list**


To try and create order out of chaos, I separated the benchmarks into four categories (this isn’t an official classification, but simply my own way of organizing them):

>Natural language processing (NLP)
>
> General knowledge  common sense
>
> Problem-solving  advanced reasoning
>
> Coding tasks


***
>**🗣️NATURAL LANGUAGE PROCESSING (NLP)**
***
These benchmarks are all about the “language” part of large language models. They aim to test things like language understanding, reading comprehension, etc.
***
1. GLUE (General Language Understanding Evaluation)

As the name suggests, GLUE attempts to measure how well LLMs understand language. It’s an umbrella benchmark that’s actually a collection of language tasks from about a dozen other datasets.

GLUE tests language-related abilities like paraphrase detection, sentiment analysis, natural language inference, and more. Here’s the dataset list:
![Alt text](921490d3-0309-49c0-97e9-33ff5d6ee403_1084x592.webp)
> Source: GlueBenchmark.com

Current best scorer: PaLM 540B (95.7 for NLI)

More about GLUE
***
2. HellaSwag

Hellz yeah!

This test measures natural language inference (NLI) by asking LLMs to complete a given passage. What makes this test especially hard is that the tasks have been developed using adversarial filtering to provide tricky, plausible-sounding wrong answers.

Sample HellaSwag question:

![Alt text](88fac6bb-16b0-4630-84f5-8119602d96d4_479x136.webp)

Current best scorer: GPT-4 (95.3)

More about HellaSwag
***
3. MultiNLI (Multi-Genre Natural Language Inference)

This benchmark contains 433K sentence pairs—premise and hypothesis—across many distinct “genres” of written and spoken English data. It tests an LLM’s ability to assign the correct label to the hypothesis statement based on what it can infer from the premise.

Sample questions (correct answer bolded)

![Alt text](79fd2084-d9f8-4c77-8d2e-8eaca6bb74a9_398x189.webp)

Current best scorer: T5-11B (92)


***
4. Natural Questions

This is a collection of real questions people have Googled. The questions are paired with relevant Wikipedia pages, and the task is to extract the right short and long answers. The dataset includes over 300K training examples.

Sample question:

![Alt text](2c684403-0cc2-4254-984d-6a1436f6bd6b_559x284.webp)

Current best scorer: Atlas (64.0)


***
1. QuAC (Question Answering in Context)

QuAC is a set of 14,000 dialogues with 100,000 question-answer pairs. It simulates a dialogue between a student and a teacher. The student asks questions while the teacher must answer with snippets from a supporting article. QuAC pushes the limits of LLMs because its questions tend to be open-ended, sometimes unanswerable, and often only making sense within the context of the dialogue.

Sample dialogue:

![Alt text](16ab8838-dbde-4e69-96e6-500202f53f12_369x513.webp)

Current best scorer: FlowQA (64.1)


***
6. SuperGLUE

SuperGLUE—a “super” version built on the GLUE benchmark above (see #1)—contains a set of more challenging and diverse language tasks.

Sample question:

![Alt text](6bd311ff-051f-4024-ba9c-d76595898093_694x66.webp)

Current best scorer: ST-MoE-32B (92.4 for Question Answering)


***
7. TriviaQA

TriviaQA is a reading comprehension test with 950K questions from a wide range of sources like Wikipedia. It's quite challenging because the answers aren't always straightforward and there’s a lot of context to sift through. It includes both human-verified and computer-generated questions.

Sample question (correct answer bolded):

![Alt text](08e2dc37-e308-4164-bed2-628e6033786c_474x299.webp)

Current best scorer: PaLM 2-L (86.1)


***
8. WinoGrande

WinoGrande’s a massive set of 44,000 problems based on the Winograd Schema Challenge. They take the form of nearly-identical sentence pairs with two possible answers. The right answer changes based on a trigger word. This tests the ability of LLMs to properly grasp context based on natural language processing.

Sample questions:

![Alt text](edca6e48-8895-4c70-81b8-5fc4914df2fd_990x224.webp)

Current best scorer: GPT-4 (87.5)

***
>**👩‍🎓GENERAL KNOWLEDGE & COMMON SENSE**
***
These benchmarks measure an LLM’s ability to answer world knowledge questions and/or apply common sense reasoning to arrive at correct responses. Knowledge questions can be general or focus on specific industries and subjects.
***
9. ARC (AI2 Reasoning Challenge)

ARC tests LLMs on grade-school science questions. It’s quite tough and requires deep general knowledge, as well as the ability to reason. There are two sets: Easy and Challenge (with especially difficult tasks).

Sample questions:

![Alt text](23e30a71-ee6c-452e-b6c2-af2333a63593_454x205.webp)

Current best scorer: GPT-4 (96.3)

***

10. MMLU (Massive Multitask Language Understanding)

MMLU1 measures general knowledge across 57 different subject areas. These range from STEM to social sciences and vary in difficulty from elementary to advanced professional level.

Sample question (correct answer bolded):

![Alt text](db1a351f-0be2-4363-8e82-e9a24c0361f7_783x123.webp)

Current best scorer: GPT-4 (86.4)


***
11. OpenBookQA

OpenBookQA is designed to simulate open-book exams. The test contains close to 6,000 elementary science questions. The tested LLM is expected to answer these by relying on 1,326 core science facts (provided in the test) as well as broad common knowledge from its own training data.

Sample question (with supporting facts and required knowledge)

![Alt text](342a4771-485c-415a-b94d-9d29c2c09f6b_430x278.webp)

Current best scorer: PaLM 540B (94.4)

***
12. PIQA (Physical Interaction: Question Answering)

PIQA measures a model’s knowledge and understanding of the physical world. The benchmark contains hypothetical situations with specific goals, followed by pairs of right and wrong solutions.

Sample questions:

![Alt text](67a1c21b-d07d-45cf-8367-3437b53b72ec_325x222.webp)

Current best scorer: PaLM 2-L (85.0)
***
13. SciQ

The SciQ dataset contains 13,679 multiple-choice questions with four possible answers each. These mainly revolve around natural science subjects like physics, chemistry, and biology. Many of the questions include additional supporting text that contains the correct answer.

Sample questions:

![Alt text](e088319c-3ed1-4684-9e23-80d09098f78e_1114x592.webp)
> Source: [Papers With Code](https://paperswithcode.com/dataset/sciq)

Current best scorer: LLaMA-65B+CFG (96.6)
***
14. TruthfulQA

This benchmark tries to see if LLMs end up spitting out wrong answers based on common misconceptions. The questions come from categories including health, law, fiction, and politics.

Sample questions (with incorrect answers by GPT-3):

![Alt text](40cd6c5a-7b5b-4d4c-abed-739dff5d771a_503x480.webp)

Current best scorer: Vicuna 7B + Inference Time Intervention (88.6)

***

>**🧩PROBLEM SOLVING & ADVANCED REASONING**

I chose to make this a separate category, because these benchmarks are especially challenging for LLMs and often require multistep reasoning.

***
15. AGIEval

AGIEval is a collection of 20 real-world exams including SAT and law school tests. It goes beyond language understanding to see how well LLMs can reason through problems in the same way humans do.

Sample question: SAT questions

Current best scorer: ???

***
16. BIG-Bench (Beyond the Imitation Game)

This one’s a holistic and collaborative benchmark with a set of 204 tasks ranging from language to math to biology to societal issues. It is designed to probe LLMs ability for multi-step reasoning.2

Sample task:

![Alt text](6e4564d5-bcce-495c-9098-a5b8711482d0_604x119.webp)

Current best scorer: PaLM 2 (100 for logical reasoning)

***
17. BooIQ

BoolQ pulls together over 15,000 real yes/no questions from Google searches. Each of these is paired with a Wikipedia passage that may contain the answer. It’s challenging for LLMs because it requires correctly inferring answers from context that might not explicitly contain them.

Sample question:

![Alt text](508c338b-9e81-4a8d-81f1-3dcd688e8d63_426x105.webp)

Current best scorer: ST-MoE-32B (92.4)

***

18. GSM8K

GSM8K is a set of 8.5K grade-school math problems. Each takes two to eight steps to solve using basic math operations. The questions are easy enough for a smart middle schooler to solve and are useful for testing LLMs’ ability to work through multistep math problems.

Sample question:

![Alt text](e6af1840-1ec4-418e-af55-94c7b44693f7_886x115.webp)

Current best scorer: GPT-4 Code Interpreter (97.0)

***
>**💻CODING**

This category of LLM benchmarks evaluate a model’s ability to work with code: writing code from scratch, completing code, summarizing code in natural language, etc.
***
19. CodeXGLUE (General Language Understanding Evaluation benchmark for CODE)

CodeXGLUE tests how well LLMs can understand and work with code. It measures code intelligence across different types of tasks, including:

* Code-to-Code: Fixing code errors, finding duplicate code, etc.

* Text-to-Code: Searching for code using natural language

* Code-to-Text: Explaining what code does

* Text-to-Text: Translating technical documentation

Here’s the full list of included tasks, datasets, programming languages, etc.:
![Alt text](b3245e9c-7ac1-4e21-84c2-065d75f7cdbf_2495x1324.webp)
> Source: [GitHub](https://github.com/microsoft/CodeXGLUE)

Current best scorer: CodeGPT-adapted (75.11 for Code Completion)

***
1.  HumanEval

HumanEval contains 164 programming challenges for evaluating how well an LLM can write code based on instructions. It requires the LLM to have knowledge of basic math, algorithms, and language understanding. The resulting code has to not only be correct but function as expected.

Sample problem (prompt in white, completion in yellow):
![Alt text](91a18328-0b68-4ddb-866f-7e56bc352ba0_760x208.webp)

Current best scorer: GPT-4 (91.0)

***
21. MBPP (Mostly Basic Python Programming)

MBPP includes 1,000 Python programming problems that should be easy for entry-level programmers. Each problem has a task description, code solution, and 3 test cases.

Sample task:

![Alt text](1791ef54-2115-4d83-b04f-aae19adf3ebf_405x127.webp)

Current best scorer: LEVER + Codex (68.9)

***

