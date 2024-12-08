# Sorting Algorithm Detective: Identifying Algorithms Through Execution Analysis

## Overview
This project is a part of a homework assignment focused on analyzing the runtime behavior of five sorting algorithms implemented in the provided `cmpe242-sort01.jar` package. The task involves running experiments, collecting timing data, and making educated guesses about which sorting algorithm corresponds to each of the provided methods. The results are documented in a report with justifications based on time complexity and experimental observations.

## Objectives
- Gain hands-on experience with algorithm runtime analysis.
- Understand Big-O complexities by observing sorting behaviors.
- Use Java's `System.currentTimeMillis()` for time measurements.
- Perform experiments with ascending, descending, and random inputs.
- Visualize and interpret data using tools like Excel or R.

## Requirements
- Use the `cmpe242-sort01.jar` package.
- Identify which sorting algorithm corresponds to each method in the `SortingAlgorithm` class by analyzing runtime data.
- Create a comprehensive report, including visualizations, explaining your experimental setup and findings.

## Provided Jar File
The `cmpe242-sort01.jar` file contains the following:
- **Class**: `SortingAlgorithm`
- **Methods**:
  - `sort1(int[] ar, long studentID)`
  - `sort2(int[] ar, long studentID)`
  - `sort3(int[] ar, long studentID)`
  - `sort4(int[] ar, long studentID)`
  - `sort5(int[] ar, long studentID)`
  - `printArray(int[] ar)`

## Steps to Complete
### Step 1: Setup
1. Download the `cmpe242-sort01.jar` file from the course LMS.
2. Set up the JAR file in your Java project:
   - **In Eclipse**: Right-click on the project → Build Path → Configure Build Path → Add Jars.
   - **In Terminal**: Place the JAR file in the same directory as your `.java` files, and compile/run using:
     ```bash
     javac -cp cmpe242-sort01.jar SortingAlgorithmTester.java
     java -cp cmpe242-sort01.jar SortingAlgorithmTester
     ```

### Step 2: Write the Tester Class
- Create a `SortingAlgorithmTester` class with a `main` method.
- Generate input arrays of:
  - Ascending integers
  - Descending integers
  - Random integers (use `java.util.Random`).
- Sort these arrays using all five sorting methods.

### Step 3: Measure Execution Time
- Use `System.currentTimeMillis()` to measure runtime for each sorting method.
- Perform multiple runs for each array and take the median runtime.
- Record results in a table for each input type and array size.

### Step 4: Analyze Results
- Compare runtimes and deduce which sorting algorithm corresponds to each method based on:
  - Time complexity growth rates (`O(n²)`, `O(n log n)`, etc.).
  - Observed behaviors with ascending, descending, and random inputs.
- Address stack overflow errors for large inputs and document observations.

### Step 5: Visualization and Report
- Visualize your results using tables, plots, or graphs (e.g., in MS Excel or R).
- Prepare a 2-3 page PDF report including:
  - Experimental setup and procedure.
  - Collected data and observations.
  - Justifications for your algorithm guesses.
  - Discussion on runtime complexities and edge cases.

### Example Method Call
```java
int[] array = {1, 2, 3, 4, 5};
SortingAlgorithm.sort1(array, 1234567801L);
SortingAlgorithm.printArray(array);
