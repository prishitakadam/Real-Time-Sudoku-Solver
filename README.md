# Real Time Sudoku Solver

<p align="center">
  <img src="/Images/SudokuSolver.gif" width="500" height="350" />
</p>


## Overview
Sudoku is one of the most popular puzzle of all time.The goal of Sudoku is to fill 9x9 grid such that each row,each column and 3x3 grid contains all of the digits between 1 to 9. In this project we aim to create a real time Sudoku solver which recognise the elements of Sudoku puzzle and providing a digital solution using Computer vision. 

## Steps
1. Grab the Sudoko Grid from the Webcam Image
2. Extract and Detect the Digits
2. Solve the puzzel and Print the Solution

## 1. Grab the Sudoko Grid from the Webcam Image
- ### Extracting the Contour with biggest area
1. Convert image to Gray scale *(cv2.cvtColor)*
2. Blur the image using Gaussian Blur *(cv2.GaussianBlur)*
3. Apply adaptive thresholding *(cv2.adaptiveThreshold)*
4. Extract the contour with biggest area *(cv2.contourArea)*
<p align="center">
  <img src="/Images/frame.png" width="300" height="250" />
</p>

- ### Extract Sudoku Grid
Use *cv2.warpPerspective* to get stable Sudoku Grid
<p align="center">
  <img src="/Images/prespective.png" width="300" height="250" />
</p>
