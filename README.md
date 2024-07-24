# OPenai -voice assistant

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Project Structure](#project-structure)
7. [API References](#api-references)
8. [Contributing](#contributing)


## Introduction

Voice Assistant systems have gained remarkable popularity in recent years, transforming the way we interact with technology and making our daily tasks more convenient and accessible. This project introduces "Jarvis A.I," an AI-based voice assistant implemented in Python. This section provides an overview of the project's motivation, objectives, the problem statement, and the challenges encountered.


## Features

- Real-time stock price updates
- Portfolio valuation and performance tracking
- Integration with financial data APIs
- User-friendly interface with interactive charts
- Secure user authentication
- Natural language processing for querying stock information
- Historical data analysis
- Automated portfolio rebalancing suggestions
- News aggregation related to stocks in the portfolio

## Requirements

- Python 3.7 or higher
- MySQL server
- Internet connection for API data fetching

### Python Packages:

- `speech_recognition`
- `webbrowser`
- `openai`
- `os`
- `datetime`
- `random`
- `pyttsx3`
- `mysql-connector-python`
- `flask`
- `flask-login`
- `pandas`
- `matplotlib`

## Installation

### Clone the Repository

```bash
git clone https://github.com/adarshsharma-18/OPENAI-Javis-VoiceAssisstant
cd stock-portfolio-manager
```

### Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

### Install the Required Packages

```bash
pip install -r requirements.txt
```

### Set Up the MySQL Database

Create a database in your MySQL server and run the following SQL command to create the necessary table:

```sql
CREATE DATABASE stock_portfolio_manager;

USE stock_portfolio_manager;

CREATE TABLE voice_assistant (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_command TEXT NOT NULL,
    ai_response TEXT NOT NULL,
    timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### Configuration

Create a `config.py` file in the root directory and add your OpenAI API key:

```python
apikey = 'your_openai_api_key'
```

## Usage

### Starting the Application

Run the main application script:

```bash
python app.py
```

### Using the Voice Assistant

Upon running, the voice assistant will introduce itself as Jarvis and start listening for your commands. You can interact with it using natural language commands such as:

- "Open YouTube"
- "What's the time?"
- "Tell me a joke"
- "Who is Elon Musk?"

The assistant will respond with appropriate actions or information, and it will log the user commands and AI responses to the MySQL database.


## API References

- [OpenAI API](https://beta.openai.com/)


## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.
