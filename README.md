# Piano Tiles Bot

## SHORT INTRODUCTION

We hope you and your family are keeping safe. In this tutorial, we are developing a short and fun project Piano Tiles Bot using OpenCV. The question may arise in our mind, “What type of game is piano tiles”, so, the piano tiles game is simply we should tap the black tiles very fast without losing any of them or hitting a white tile.

The concept used here is, we first by selecting a region to track for black tiles. Then within that region, if the pixel value of any column goes below the threshold (let’s say 100, then it is black). Then we simply simulate a mouse click over that region. The game consists of 4 vertical lanes so the bot checks only one column per lane and if it finds a pixel with black color it clicks the mouse at its position and then starts to search for the new tile to hit.

_**Additional Project: Do checkout our previous projects on**_ “A computer vision based vehicle detection and counting system“

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

<code> 
>>> import random <br>
>>> import time <br>
>>> import cv2 <br>
>>> import imutils <br>
>>> import keyboard <br>
>>> import numpy as np <br>
>>> import pyautogui <br>
>>> import pytesseract <br>
>>> import win32api <br>
>>> import win32con </code>

## PIANO TILES BOT SETUP

<code>
>>> positions = list(range(start, end, jump)) <br>
>>> while True: <br>
>>>     if keyboard.is_pressed('esc'): <br>
>>>         break <br>
>>>     elif keyboard.is_pressed('s'): <br>
>>>         print("Started") <br>
>>>         prev = -1 <br>
>>>         while keyboard.is_pressed('q') == False and keyboard.is_pressed('Q') == False: <br>
>>>             for pos, col in enumerate(positions): <br>
>>>                 if prev != pos and pyautogui.pixel(col, row - delay)[0] < 50: <br>
>>>                     actionClick(col, row) <br>
>>>                     prev = pos <br>
>>>                     break <br>
>>> print("Finished") <br>
<code>
