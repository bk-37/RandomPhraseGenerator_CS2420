# Random Phrase Generator (Java)

## 🧠 Overview
This project is a Java-based Random Phrase Generator that uses context-free grammars to recursively construct valid phrases. It can generate random poetic sentences, mathematical expressions, ABC-style sequences, and more — depending on the grammar file provided.

The project demonstrates file parsing, custom stack implementation, and recursive phrase construction using formal grammar rules.

## 🎯 Features
- Parse `.g` grammar files with custom syntax
- Generate recursive and nested phrases from start symbols
- Support for multiple included grammar sets:
  - `abc.g`, `abc_spaces.g`
  - `poetic_sentence.g`
  - `mathematical_expression.g`
  - `assignment_extension_request.g`
- Custom-built `ArrayStack` class (no reliance on Java's built-in stack)
- Interactive command-line usage

## 📂 Project Structure

| File | Description |
|------|-------------|
| `ArrayStack.java` | Custom generic stack implementation used during parsing |
| `GrammarParser.java` | Loads grammar from a `.g` file and organizes rules |
| `PhraseGenerator.java` | Recursively generates phrases from parsed grammar |
| `RandomPhraseGenerator.java` | Main driver — takes file and count as input and prints random phrases |

### 🗂 Example Grammar Files

| File | Description |
|------|-------------|
| `abc.g` / `abc_spaces.g` | Simple rules for generating ABC sequences |
| `poetic_sentence.g` | Grammar for stylistic poetic lines |
| `mathematical_expression.g` | Generates algebra-style expressions |
| `assignment_extension_request.g` | Humorously generates excuses for late work |

## 🚀 How to Run

### Compile:
```bash
javac *.java
```

### Run:
```bash
java RandomPhraseGenerator poetic_sentence.g 5
```

This will generate 5 random poetic sentences using the specified grammar.

## 📌 Notes

- Grammar format:
  ```
  <start>
      the <noun> <verb>
  <noun>
      student
      engineer
      philosopher
  <verb>
      sleeps
      thinks
      codes
  ```

- Non-terminals are wrapped in angle brackets (`< >`)
- You can easily extend the system by writing your own `.g` grammar files

## ✍️ Authors
**Brian Keller and Wyatt Young**  
Biomedical Engineering BS/MS | Computer Science Minor  
University of Utah
