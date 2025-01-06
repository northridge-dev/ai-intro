# Introduction to Artificial Intelligence

v. 2.0.0

## Course Details

[Northridge Prep](https://northridgeprep.org) Spring 2025

Dr. Nicholas Kruckenberg
[nkruckenberg@northridgeprep.org](mailto:nkruckenberg@northridgeprep.org)

## Course Description

In the second semester of this year-long course, we'll learn about artificial
intelligence by trying to recreate Google's NotebookLM. We'll learn about neural
networks, build and train a large language model from scratch, implement a
retrieval-augmented generation system, and (if there's time) try to build our
own podcast generator. Along the way, we'll extend our knowledge of Python and
learn about databases, APIs, web servers, UI development, and the process of
building complex software.

We'll also read some papers, articles, and blog posts and use our experience
building intelligent systems to ground philosophical discussions about the
nature of intelligence and what the existence of intelligent machines means for
us humans.

## Goals

By the end of the semester, you should:

1. Understand how a large language models work, their abilities and limitations.
2. Understand how semantic search works and how it can be used to augment a
   large language model.
3. Articulate what it means for a machine or system to be _intelligent_.
4. (With help) build components of a complex software system.
5. Become a stronger programmer.
6. Develop your problem-solving muscles. We'll focus on a few techniques:

   - _decomposing_ big problems into smaller, more tractable ones
   - using _abstraction_ to manage complexity

7. Improve your ability to communicate technical concepts and decisions to both
   technical and non-technical audiences.

## The Plan

We'll spend most of our time building KnotebookLM (our version of Google's
NotebookLM). We'll build as fast as we can, but we'll also take time to
experiment, read, and discuss.

I will publish a more detailed schedule at the beginning of each week, but here
is a rough sketch of the plan:

1. high-level system design of KnotebookLM
2. precursors: summarization and text generation before neural networks (to
   better judge what it means to say that a large language model is "just" a
   next-word predictor)
3. neural network basics
4. build and train a large language model

   - preparing text for training
   - coding the neural network and transformer architecture
   - pretraining the model
   - fine-tuning the model
   - evaluating the model

5. adding notebook sources; start with plain text
6. producing summaries of notebook sources (using more powerful models via API)
7. storing generated artifacts
8. asking questions of notebook sources; searching sources
9. storing chat sessions
10. adding other tools: e.g., generate follow up questions, study guides, etc.
11. adding other source types: e.g., PDFs, websites, images, audio, video
12. generate podcast scripts; more about fine-tuning (for personality, etc.)
13. generate, store, and play podcast audio

## Grades

Quarter and semester grades will be composed of the following elements and
assigned according to the Northridge grading scale.

### Journal Club (20%)

Most weeks, you'll read a paper, article, or blog post outside of class and
discuss it in class. You'll be graded on a short in-class writing assignment and
discussion participation. (~15 equally weighted grades)

### Code Contributions (40%)

You'll submit a pull request -- your code and a detailed explanation of how it
works -- for each module we build. At least once, you'll be asked to present
your pull request to the class. Pull requests will be judged on code quality and
the clarity and accuracy of your technical descriptions. I'll select one or more
strong versions of each module to merge into the shared codebase. (~10 equally
weighted grades)

### Blog Posts (20%)

You'll write two blog posts:

- a technical write up about a project module
- an elaboration of one of our journal club discussions

These blog posts will be published for the world to read. I'll share the
schedule and grading criteria early in the semester.

### Exams (20%)

You'll write two exams, one at the end of each quarter. Each exam will consist
of coding questions and short answer/essay questions.

## Materials

Please bring to class every day:

1. Something to write with (pen or pencil, as you prefer)
2. A notebook or binder with paper for notes
3. A folder or binder to keep and organize handouts and other materials

## Tools

- [Northridge Dev](https://northridge.dev): https://northridge.dev
- [KnotebookLM](https://knotebooklm.northridge.dev):
  https://knotebooklm.northridge.dev
- [KnotebookLM blog](https://knotebooklm.github.io):
  https://knotebooklm.github.io

Web-based tools for which you'll need an account. Some require phone
verification.

- [GitHub](https://github.com)
- [Google Colab](https://colab.research.google.com)
- [Hugging Face](https://huggingface.co)
- [Kaggle](https://kaggle.com)

## Responsible Use of Technology

Follow the Computer and Network Technology policy in the student handbook.

If you feel like you need to hide your screen, switch tabs or windows, or clear
your browser history, you're falling short of the mark.

## AI as a Tool for Learning and Building

We'll explore how best to use artificial intelligence to learn about AI and
build our own AI learning tool.
