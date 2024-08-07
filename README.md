Certainly! Here's the updated GitHub README with information about the attached `catHerder.py` script:

```markdown
# CatHerder: Reflective LLM Code Creator & Debugger

<img src="cat_herder.png" alt="CatHerder Debugger" width="150" height="200" align="left" style="margin-right: 20px;"/>

## Overview

CatHerder is a simple and intuitive code creator and debugger that utilizes Large Language Model (LLM) reflection to help you debug Python code effectively. By iteratively refining code with the assistance of an LLM, this tool aims to make the debugging process smoother and more efficient.

You can also use it to gradually add features to existing code.  This is where the cat herding really begins...

## Features

- **Automated Debugging**: Automatically debug code using LLM reflections.
- **Iterative Refinement**: Continuously refine the code based on LLM feedback.
- **Error Handling**: Detects and handles repeated errors to avoid infinite loops.
- **User-Friendly**: Allows users to input new code or modify existing code.

### Description of Reflexion

**Reflexion** is a framework designed to enhance the capabilities of language models (LLMs) through a process of self-evaluation and iterative improvement. The key idea is to enable language models to reflect on their outputs, identify errors or areas for improvement, and refine their responses based on this self-assessment. This process mimics human-like reflective thinking and learning, allowing the model to improve its performance over time through verbal reinforcement learning.

In practice, Reflexion involves the following steps:
1. **Self-Evaluation**: The model reviews its own generated content or the content produced by other models to identify issues, inconsistencies, or errors.
2. **Feedback Generation**: The model generates feedback or suggestions for improvement based on its self-evaluation.
3. **Iterative Refinement**: The model refines its outputs iteratively, using the feedback to improve its responses in subsequent iterations.

This approach aims to make language models more robust, adaptive, and capable of producing high-quality outputs through continuous learning and self-improvement.  

For more details, refer to the paper:
> S. Shinn, E. Gao, A. Andreassen, D. Hendrycks. **"Reflexion: Language Agents with Verbal Reinforcement Learning."** NeurIPS 2023. [arXiv link](https://arxiv.org/abs/2303.11366).

## Usage

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/galenwilkerson/CatHerder-reflective-LLM-debugger.git
    cd CatHerder-reflective-LLM-debugger
    ```

2. **Set Up OpenAI API Key**:
    - Save your OpenAI API key in a file named `api_key.txt` in the root directory of the project.

3. **Run the Debugger**:
    - You can run the provided Jupyter notebook or use the script to start debugging your Python code.
    - To run the Jupyter notebook:
      ```bash
      jupyter notebook "Cat Herder - Simple Debugger using LLM Reflection.ipynb"
      ```

4. **Interacting with the Debugger**:
    - The debugger will prompt you to enter a new code prompt or modify existing code.
    - It will then generate initial code, attempt to execute it, and debug iteratively based on the errors encountered.

## Example

Here's a simple example to illustrate how CatHerder works:

1. **Input Code Prompt**:
    ```
    print 'hello world'
    ```

2. **Generated Code**:
    ```python
    print('hello world')
    ```

3. **Execution and Debugging**:
    - If the code fails to execute, CatHerder will provide suggestions to fix the errors.
    - The process will repeat until the code executes successfully or the same error is encountered consecutively, in which case the process stops.
  
## Detailed example
```
Do you want to (1) enter a new code prompt or (2) modify existing code? Enter 1 or 2: 1
Please enter the code prompt: create a fibonacci class
How many debug iterations should be done? 5
------------------
Initial code generated by ChatGPT:
 class Fibonacci:
    def __init__(self, n):
        self.n = n

    def calculate(self):
        fib_sequence = [0, 1]
        for i in range(2, self.n):
            fib_sequence.append(fib_sequence[i-1] + fib_sequence[i-2])
        return fib_sequence[:self.n]

# Example Usage:
n = 10
fibonacci = Fibonacci(n)
result = fibonacci.calculate()
print(result)
------------------

Iteration 1:
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
Code executed successfully.
Saved to script.py
Final version saved to script.py
```

## Using `catHerder.py`

The `catHerder.py` script is a command-line tool that allows you to generate and debug code using LLM reflections. You can provide a code prompt or modify existing code, specify the code type (e.g., Python, LaTeX, HTML), and set the number of debug iterations.

### Running the Script

```bash
python catHerder.py -p "create a fibonacci class" -i 5
```

### Command-Line Arguments

- `-p`, `--prompt`: The code prompt to generate new code or the path to a file containing the prompt.
- `-m`, `--modify`: The path to the existing code file to modify.
- `-c`, `--code_type`: The type of code (default: python, latex, html, etc.). Default is 'python'.
- `-i`, `--iterations`: Number of debug iterations to perform. Default is 5.

### Example

```bash
python catHerder.py -p "create a fibonacci class" -i 5
```

```bash
python catHerder.py -m existing_code.py -c python -i 3
```

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests to enhance the functionality of CatHerder.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Flow Chart

<img src="./CatHerder_Flow.png" alt="CatHerder Flowchart"  align="left" style="margin-right: 20px;"/>
```

This updated README includes information about the `catHerder.py` script and how to use it from the command line, along with the existing details about the project and examples.
