# Piano Tiles Bot

## SHORT INTRODUCTION
![piano-tiles-bot](https://user-images.githubusercontent.com/40186859/123657461-87aa4b80-d850-11eb-92e2-8ff066586a71.png)

We hope you and your family are keeping safe. In this tutorial, we are developing a short and fun project Piano Tiles Bot using OpenCV. The question may arise in our mind, “What type of game is piano tiles”, so, the piano tiles game is simply we should tap the black tiles very fast without losing any of them or hitting a white tile.

The concept used here is, we first by selecting a region to track for black tiles. Then within that region, if the pixel value of any column goes below the threshold (let’s say 100, then it is black). Then we simply simulate a mouse click over that region. The game consists of 4 vertical lanes so the bot checks only one column per lane and if it finds a pixel with black color it clicks the mouse at its position and then starts to search for the new tile to hit.

_**Additional Project: Do checkout our previous projects on**_ [A computer vision based vehicle detection and counting system“](https://graspcoding.com/a-computer-vision-based-vehicle-detection-and-counting-system-ai-project/)

## REQUIRED LIBRARY 

1. OpenCV <br>
<code> >>> pip install opencv-contrib-python </code>
2. Imutils <br>
<code> >>> pip install imutils </code> 
3. Keyboard <br>
<code> >>> pip install keyboard </code>  
5. Numpy <br>
<code> >>> pip install numpy </code>
6. Pyautogui <br>
<code> >>> pip install Pyautogui </code>
7. Pytesseract <br>
<code> >>> pip install pytesseract </code>
8. Win32api <br>
<code> >>> pip install win32api </code>
9. Win32con <br>
<code> >>> pip install win32con </code>

## IMPORT NECESSARY LIBRARIES

```python
>>> import random 
>>> import time 
>>> import cv2 
>>> import imutils 
>>> import keyboard 
>>> import numpy as np 
>>> import pyautogui 
>>> import pytesseract 
>>> import win32api 
>>> import win32con 
```

## PIANO TILES BOT SETUP

```python
>>> positions = list(range(start, end, jump)) 
>>> while True: 
>>>     if keyboard.is_pressed('esc'): 
>>>         break 
>>>     elif keyboard.is_pressed('s'): 
>>>         print("Started") <br>
>>>         prev = -1 
>>>         while keyboard.is_pressed('q') == False and keyboard.is_pressed('Q') == False:
>>>             for pos, col in enumerate(positions): 
>>>                 if prev != pos and pyautogui.pixel(col, row - delay)[0] < 50: 
>>>                     actionClick(col, row) 
>>>                     prev = pos 
>>>                     break 
>>> print("Finished") 
```
## RESULT

https://user-images.githubusercontent.com/40186859/123657009-23878780-d850-11eb-9a4a-a4de78791625.mp4

## ☺ Thanks for your time ☺

What do you think of this “Piano Tiles Bot using OpenCV“? Let us know by leaving a comment below. (Appreciation, Suggestions, and Questions are highly appreciated).
