# Activity Tracker Logic

Windows application usage tracking system that monitors active windows and logs usage data.

## Project Structure

```
activity tracker logic/
├── main.py           # Main entry point
├── tracker.py        # Core AppTracker class
├── data_manager.py   # JSON data persistence
├── utils.py          # Utility functions
├── config.py         # Configuration settings
├── requirements.txt  # Python dependencies
└── README.md         # This file
```

## Setup

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the tracker:
   ```bash
   python main.py
   ```

## Features

- **Real-time tracking**: Monitors active windows every second
- **Smart filtering**: Ignores system processes and short sessions
- **Data persistence**: Saves usage data to JSON file
- **Error handling**: Graceful shutdown and backup data saving
- **Configurable**: Easy to customize settings in `config.py`

## Configuration

Edit `config.py` to customize:
- Minimum session duration
- Check interval
- Apps to ignore
- JSON file path

## Data Format

Saves data to `app_usage.json` with structure:
```json
[
  {
    "timestamp": "2024-01-01 10:00:00",
    "app_name": "chrome.exe",
    "window_title": "Google Chrome",
    "duration": 300.5,
    "session_end_reason": "app_switch"
  }
]
```

## Usage

1. Start the tracker: `python main.py`
2. Use your computer normally
3. Press `Ctrl+C` to stop tracking
4. Data is automatically saved to JSON file 