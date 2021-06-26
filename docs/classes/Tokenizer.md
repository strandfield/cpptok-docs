---
layout: default
title: "Tokenizer class"
parent: "Class reference"
---

# Tokenizer Class

**Brief:** produces token from an input string

## Detailed description

The Tokenizer is a line-based tokenizer. That is, it is able to produce tokens for one line of input at a time and maintains a state to produce the correct output for multi-line constructs (currently that means multi-line comments).

The tokenize() methods provide tokenization for a variety of inputs, but ultimately an array of char* is used.

The output tokens are written in the `output` member of the class.

## Enumerations

### State

**Brief:** describes the state of the tokenizer

- Default
- LongComment

## Members documentation

### void tokenize(const std::string& str)

Parameters:
- a string to tokenize

Warning: do not pass temporary string to this function. The output tokens store the text as a string_view.

### void tokenize(const char* str)

Parameters:
- a string to tokenize

### void tokenize(const char* str, size_t len)

Parameters:
- the string to tokenize
- the length of the string

### void reset()

**Brief:** resets the tokenizer

Puts the tokenizer back in its default state and clears the output vector.

