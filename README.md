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
<details>
<summary><b>Extracting the Contour with biggest area</b></summary>
<ol>
  <li>Convert image to Gray scale <i>(cv2.cvtColor)</i></li>
  <li>Blur the image using Gaussian Blur <i>(cv2.GaussianBlur)</i></li>
  <li>Apply adaptive thresholding <i>(cv2.adaptiveThreshold)</i></li>
  <li>Extract the contour with biggest area <i>(cv2.contourArea)</i></i></li>
</ol>
</details>

<p align="center">
  <img src="/Images/frame.png" width="300" height="250" />
</p>

<details>
<summary><b>Extract Sudoku Grid</b></summary>
  Use <i>cv2.warpPerspective</i> to get stable Sudoku Grid
 </details>
 
<p align="center">
  <img src="/Images/prespective.png" width="300" height="300" />
</p>

## 2. Extract and Detect the Digits
<details>
<summary><b>Process the Extracted Grid</b></summary>
  Use <i>cv2.morphologyEx</i> and Invert the image
 </details>
 
 <p align="center">
  <img src="/Images/P-Window.png" width="300" height="300" />
  <img src="/Images/invert.png" width="300" height="300" />
</p>

<details>
<summary><b>Get Individual Cells of the grid and Predict the Digit</b></summary>
  Model used for prediction has been trained on subset of <i>Chars4K Dataset</i> which contains digits only (0-9).
  Model can be viewed <a href="https://github.com/prishitakadam/Real-Time-Sudoku-Solver/blob/master/Digit%20Recognizer%20Model.ipynb">here</a>

 </details>
 <p align="center">
  <img src="/Images/segements.png" width="300" height="250" />
</p>
