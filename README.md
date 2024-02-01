# Engli

### Language Overview

Engli is a new language based on English with some changes aiming to make it more logical, and easier to learn.

Here are some of its key features:

- **0 collisions** — No words sound identical, and English words with multiple meanings that differ too much are split into multiple words
- **Phonetically rigid** — Each letter only has one sound, and the letters surrounding it have no impact on that
- **0 ambiguity** — There is only one way to spell any word, and only one way to pronounce it
- **0 inconsistency** — Prefixes and suffixes will stay separate from a word, like "multi-player" instead of "multiplayer"
- **International** — No more divide between "center" and "centre", "sentr" is used instead
- **Faster to type in** — Most words are shorter, which allows you to type faster

A full specification can be found in the [`spec/`](./spec/) directory.

### Technical Description

Engli is a declaratively defined community "fork" of English with 0 collisions, 0 ambiguity, fully deterministic spelling/pronunciation via rigid phonetics, and more.

The language is defined entirely in `.toml` files in `words/`, as well as `.md` files in `spec/`. Dictionaries can thus be easily compiled from this repository to any format, such as HTML, LaTeX or others.

Here is an example of [a word](./words/ryl.toml):

```toml
[[definition]]
text = "without charge, free"
class = "adverb"
example = "Ce srvis wuz ixwd greytis."

[[definition]]
text = "without charge, free"
class = "adjective"
example = "Ce greytis srvis wuz ixwd."
```

### Usage

#### As a language

You can get started with reading and writing Engli by reading the [spec](./spec/).

#### As a dictionary API

You can easily get the definitions for any Engli word by reading and parsing a file at `words/<name>.toml`. Alternatively, you can compile all the words into a single file, such as a single database or JSON file.

### License

Given the language is defined declaratively in a source code-like format, the project uses the [MIT License](./LICENSE.md).

### FAQ

#### Q: Is this really a new language or just a different way to write English?

**A:** Engli is a new language based on English and not just a different way to write it. Engli differs in words, such as splitting the English word "free" into the Engli words "libr" and "greytis." Pronunciation will also differ in certain words.

#### Q: Why not use a Creative Commons license?

**A:** While Creative Commons licenses are more common on projects of this kind, Engli is defined declaratively in a source code-like format. We felt the [MIT License](./LICENSE.md) would be more appropriate in this case.