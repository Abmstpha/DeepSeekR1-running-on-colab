
# DeepSeek R1 Distill Qwen 1.5B: Harnessing the Power of Transformers

This repository hosts the implementation of the **DeepSeek R1 Distill Qwen 1.5B** model, showcasing its capabilities in natural language generation and efficient task execution using the **Transformers** library.

## Overview

The notebook demonstrates:
- Loading the **DeepSeek R1 Distill Qwen 1.5B** model from Hugging Face.
- Prompt-based AI generation using Transformer models.
- Generating a Python function to compute the Fibonacci sequence efficiently with O(n) time complexity.

## Key Features

- **Model**: DeepSeek R1 Distill Qwen 1.5B, an optimized Transformer model for causal language modeling.
- **Usage**: Tokenization and generation of user-defined prompts.
- **Efficiency**: Generates responses with context-based logic and code examples.

## Installation and Setup

1. **Clone this repository**:
   ```bash
   git clone git@github.com:Abmstpha/DeepSeekR1-running-on-colab.git
   ```

2. **Enter the folder and run the notebook** 
   ```bash
   cd deepseek_r1_distill_qwen1_5B_transformers
   ```

## **Install dependencies: Ensure you have Python and transformers installed.**

   ```bash
   pip install transformers 
   ```


## **Run the notebook: Open the notebook in your preferred environment and execute the cells sequentially.**

Model and Tokenizer
The model and tokenizer are fetched from Hugging Face:

Model: DeepSeek-R1-Distill-Qwen-1.5B
Device: Optimized for GPU execution.

Example Prompt
prompt = "Create a Python function to calculate Fibonacci sequence with O(n) time complexity"

The AI processes this prompt and generates an optimized solution leveraging efficient algorithms.

## **Here startes the Response of Model**
 
</think>

To calculate the nth Fibonacci number efficiently with O(n) time complexity, we can use an iterative approach. This method ensures that each Fibonacci number is computed in sequence, leading to a linear time complexity relative to the input size.

### Approach
The Fibonacci sequence is defined such that each number is the sum of the two preceding ones, starting from 0 and 1. The iterative approach avoids the inefficiencies of recursion by using a loop to build up the sequence step by step.

1. **Base Cases**: Handle the simplest cases where `n` is 0 or 1 directly.
2. **Iterative Calculation**: For `n` greater than 1, initialize the first two Fibonacci numbers. Then, iterate from 2 to `n`, updating the current values in each iteration to compute the next Fibonacci number.

This approach ensures that each Fibonacci number is computed in constant time, leading to an overall time complexity of O(n).



### Solution Code
```python
def fib(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    a, b = 0, 1
    for i in range(2, n + 1):
        c = a + b
        a = b
        b = c
    return b
```

### Explanation
- **Base Cases**: The function immediately returns 0 for `n = 0` and 1 for `n = 1`.
- **Initialization**: Variables `a` and `b` are initialized to 0 and 1, representing the first two Fibonacci numbers.
- **Iteration**: For each number from 2 to `n`, compute the next Fibonacci number as the sum of the previous two (`a + b`). Update `a` to the old `b` and `b` to the newly computed Fibonacci number.
- **Return Result**: After completing the loop, `b` holds the nth Fibonacci number, which is returned as the result.

This method efficiently computes the Fibonacci sequence in linear time, making it suitable for reasonably large values of `n`.



''


