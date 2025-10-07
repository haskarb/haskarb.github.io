---
layout: page
title: CodeOptimiserLLM
description: AI-powered Python to C++ converter with automated performance benchmarking
img: assets/img/code-optimizer.jpg
importance: 1
category: GenAI
tags: [LLM, Code Generation, Performance Optimization, Benchmarking]
github: https://github.com/haskarb/CodeOptimiserLLM
---

## Overview

CodeOptimiserLLM is an intelligent tool that leverages Large Language Models to automatically convert Python code into optimized C++ implementations. The system not only performs the conversion but also benchmarks both versions to quantify performance improvements.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/python-code.jpg" title="Python input" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/llm-processing.jpg" title="LLM conversion" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/cpp-output.jpg" title="C++ output" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The conversion pipeline: Python source code → LLM-powered optimization → Compiled C++ binary
</div>

## Key Features

- **🤖 LLM-Powered Conversion**: Uses OpenAI's GPT models to generate idiomatic, optimized C++ code
- **⚡ Performance Benchmarking**: Automated timing comparison with microsecond precision
- **🔧 Modular Architecture**: Clean separation between optimization logic and utilities
- **📊 Quantitative Analysis**: Statistical benchmarking over 10,000+ iterations

## Technical Architecture

The system consists of three main components:

1. **CodeOptimizer Class**: Manages LLM interactions and orchestrates the conversion workflow
2. **Utility Functions**: Handle compilation, execution, and benchmarking
3. **Benchmarking Engine**: Provides accurate performance measurements for both languages

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/architecture-diagram.jpg" title="System architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    System architecture showing the flow from Python source to benchmarked C++ binary
</div>

## Performance Results

Extensive testing across various algorithms demonstrates significant performance improvements:

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/benchmark-chart.jpg" title="Benchmark results" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/speedup-graph.jpg" title="Speedup comparison" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Performance comparison showing 5-20x speedup for compute-intensive algorithms
</div>

### Benchmark Examples

| Algorithm | Python (μs) | C++ (μs) | Speedup |
|-----------|-------------|----------|---------|
| Matrix Multiply (10×10) | 125.3 | 12.4 | 10.1x |
| Bubble Sort (100 elem) | 89.7 | 4.2 | 21.4x |
| Fibonacci (n=10) | 0.36 | 0.37 | ~1x |

## Technical Implementation

The project demonstrates several advanced software engineering practices:

- **Streaming API Integration**: Real-time LLM response processing
- **Dynamic Code Execution**: Safe Python code evaluation with isolated namespaces
- **Cross-language Compilation**: Automated C++ compilation with optimization flags
- **High-precision Timing**: Microsecond-level performance measurement using `perf_counter`

```python
# Example usage
optimizer = CodeOptimizer()
results = optimizer.optimize_and_benchmark(
    python_code, 
    test_input=[5,2,8,1,9]
)
print(f"Speedup: {results['python_time_us'] / cpp_time:.2f}x")
```

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/terminal-output.jpg" title="Terminal output" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Real-time streaming output during code conversion and benchmarking
</div>

## Technologies Used

- **Python 3.11+**: Core implementation language
- **OpenAI API**: GPT-4 for code generation
- **Clang++**: C++ compilation with -O3 optimization
- **UV**: Modern Python package management
- **dotenv**: Configuration management

## Future Enhancements

1. **Multi-language Support**: Extend beyond Python→C++ to support Rust, Go, etc.
2. **GitHub Integration**: Direct repository analysis and conversion
3. **Batch Processing**: Convert entire codebases automatically
4. **ML Model Training**: Fine-tune models on domain-specific optimizations

---

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        <a href="https://github.com/haskarb/CodeOptimiserLLM" class="btn btn-primary">View on GitHub</a>
        <a href="https://github.com/haskarb/CodeOptimiserLLM#readme" class="btn btn-secondary">Documentation</a>
    </div>
</div>