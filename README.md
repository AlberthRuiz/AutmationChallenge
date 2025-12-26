# Automation Challenge

## Task 1 - UI Automated Test using Selenium WebDriver
Automated tests for user registration on a practice website.

## Task 2 - API Automated Test using Requests
API testing for country data endpoints.

---

## Requirements

- Python 3.8 or later ([Download](https://www.python.org/downloads/))
- Google Chrome browser installed
- ChromeDriver (Selenium 4 can auto-download it via Selenium Manager)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd AutmationChallenge
```

2. Create and activate a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
# or
venv\Scripts\activate  # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Project Structure

```
AutmationChallenge/
├── random_data.py      # Generates fake customer data for testing
├── selenium_layer.py   # Selenium WebDriver abstraction layer
├── task_1.py           # UI automation: user registration
├── task_2.py           # API automation: country data endpoints
├── util.py             # Utility functions (logging, file operations)
├── requirements.txt    # Python dependencies
├── input/              # Input files (auto-created)
├── output/             # Output files (auto-created)
└── log/                # Log files (auto-created)
```

## Usage

### Generate Test Data
Before running Task 1, generate mock customer data:
```bash
python random_data.py
```
This creates `input/mockup.xlsx` with test customer data.

### Run Task 1 - UI Automation
```bash
python task_1.py
```

### Run Task 2 - API Testing
```bash
python task_2.py
```

## API Endpoints (Task 2)

- `https://api.countrylayer.com/v2/all` - Get all countries
- `https://api.countrylayer.com/v2/alpha/{code}` - Get country by code

## Notes

- Selenium 4 uses Selenium Manager to automatically download the correct ChromeDriver
- For headless execution, uncomment the headless option in `selenium_layer.py`
- Logs are saved in the `log/` directory with timestamps
