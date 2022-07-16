## Refactoring python engineer’s note taking app
---
In this project I refactored a project done by youtuber and programmer [python engineer](https://github.com/python-engineer/python-fun) incorporating python best practices and improving overall performance by updating and adding more functionality to the app. 

### Code explanation

**Before**

The app had two files namely, 

- **main.py** - main file which is executed in order to run the app.
- **notion.py** - handles notion api calls and connections

```python
import speech_recognition as sr
import gtts
from playsound import playsound
import os
from datetime import datetime
from notion import NotionClient

r = sr.Recognizer()

token = "YOUR NOTION TOKEN HERE"
database_id = "YOUR NOTION DATABASE_ID HERE"

client = NotionClient(token, database_id)

ACTIVATION_COMMAND = "hey sam"

def get_audio(): # helper function to get audio input from microphone
	... # returns an mp3 file

def audio_to_text(audio): # helper function that converts audio to text
	... # returns a string

def play_sound(text): # helper function that plays a sound 
	... # returns none

if __name__ == "__main__":
```

```python
import json
import requests

class NotionClient:

    def __init__(self, token, database_id) -> None: # initializer
				...
# read, update
    def create_page(self, description, date, status): # Function that creates a page in a notion database
			... # returns the result
```

### Refactoring

**Application architecture**