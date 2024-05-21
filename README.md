<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PPE Detection using YOLOv5 and OpenCV</title>
</head>
<body>

<h1>PPE Detection using YOLOv5 and OpenCV</h1>

<h2>Table of Contents</h2>
<ul>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#license">License</a></li>
</ul>

<h2 id="installation">Installation</h2>
<ol>
    <li>Install the required libraries:</li>
    <pre><code>!pip install ultralytics
!pip install cvzone</code></pre>
    <li>Import the necessary modules:</li>
    <pre><code>from ultralytics import YOLO
import cv2
import cvzone
import math</code></pre>
    <li>Download the YOLOv5 model weights (`ppe.pt`) and place it in your project directory.</li>
</ol>

<h2 id="usage">Usage</h2>
<ol>
    <li>Open the `ppe.mp4` video file:</li>
    <pre><code>cap = cv2.VideoCapture("ppe.mp4")</code></pre>
    <li>Initialize the YOLOv5 model:</li>
    <pre><code>model = YOLO("ppe.pt")</code></pre>
    <li>Define class names and set colors for bounding boxes.</li>
    <li>Process each frame of the video:
        <ul>
            <li>Detect objects using YOLOv5.</li>
            <li>Draw bounding boxes around detected objects.</li>
            <li>Write the processed frame to the output video.</li>
        </ul>
    </li>
    <li>Save the processed video:</li>
    <pre><code>writer = cv2.VideoWriter('Output.mp4', cv2.VideoWriter_fourcc(*'DIVX'), 25, (width, height))</code></pre>
    <li>Display the processed video:</li>
    <pre><code>cv2.imshow("PPE Detection", img)</code></pre>
    <li>Press 'q' to exit the video.</li>
</ol>

<h2 id="authors">Authors</h2>
<p>This project was created by Matangee Sparshananda. For any questions or issues, please contact matangee.ai@gmail.com.</p>

<h2 id="license">License</h2>
<p>This project is licensed under the MIT License - see the LICENSE file for details.</p>

</body>
</html>
