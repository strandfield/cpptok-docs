---
layout: default
title: "Token class"
parent: "Class reference"
---

# Token Class

**Brief:** represents a token

## Detailed description

Each token has a `type()` and a `text()`.

Note that the token's text is stored as a string_view. This makes tokens cheap to copy but requires that the string that was used to create the token outlives the token.

## Members documentation

### Token()

**Brief:** builds an invalid token

Invalid tokens have `type()` TokenType::Invalid.

### Token(TokenType t, string_view str)

**Brief:** builds a token from a type and a text

Parameters:
- token type
- token text

The text is stored as a string_view. The original string should outlive the token to avoid potential undefined behavior.

### bool isValid() const

**Brief:** returns whether the token is valid

Invalid tokens have `type()` TokenType::Invalid.

### TokenType type() const

**Brief:** returns the token's type

### string_view text() const

**Brief:** returns the token's text

### std::string to_string() const

**Brief:** converts the token to a string

### bool isOperator() const

**Brief:** returns whether the token is an operator

### bool isIdentifier() const

**Brief:** returns whether the token is an identifier

### bool isKeyword() const

**Brief:** returns whether the token is a keyword

### bool isLiteral() const

**Brief:** returns whether the token is a literal

### bool isComment() const

**Brief:** returns whether the token is a comment

