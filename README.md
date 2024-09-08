# ScreenPy

ScreenPy is a Python script for analyzing and parsing screenplay text using natural language processing techniques.

## Requirements

- Python 3.x
- sense2vec (version 0.6.0 or later)
- pyparsing
- python-dateutil
- numpy
- spacy

## Setup

1. Clone the repository:
   ```
   git clone <repository-url>
   cd ScreenPy
   ```

2. Install the required packages:
   ```
   pip3 install sense2vec pyparsing python-dateutil numpy spacy
   ```

3. Download the Sense2Vec model:
   ```
   mkdir s2v_old
   wget https://github.com/explosion/sense2vec/releases/download/v1.0.0/s2v_reddit_2015_md.tar.gz
   tar -xvzf s2v_reddit_2015_md.tar.gz -C s2v_old
   ```

## Usage

Run the script using Python 3:

```
python3 screenpy.py
```

## Features

- Loads and utilizes a Sense2Vec model for semantic similarity comparisons
- Parses screenplay elements such as scene headings, shot descriptions, and time-of-day indicators
- Provides functions for identifying time expressions and dates in text

## Notes

- The script requires a Sense2Vec model to be present in the `s2v_old` directory.
- Some functions (like `loadSpacy()`) are defined but not used in the main execution.
- The `DO_TEST` variable can be set to `True` to run built-in tests.
- The script includes extensive parsing rules for various screenplay elements.

## Troubleshooting

- If you encounter a "Log is not defined" error, replace all instances of `Log()` with `print()` in the script.
- Ensure you're using a compatible version of Sense2Vec. The script was tested with version 0.6.0.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
