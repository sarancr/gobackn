# Go-Back-N ARQ Implementation

### This project was developed by below team members:
Saranya Chithalandur Rajedran
Keerthana Mahalingam

## Live demo
http://saracr.com/gobackn

## Environment
### Platform: windows 7, Mac, Google Chrome
### Language: Java script, JQuery, HTML, CSS

## Steps to run the simulator
1. Clone the project 
2. The clone project will contain below three files
	 start.html
	 app.js
	 app.css

3. Open the start.html file in a browser (Tested only on Chrome latest update). Please maximize the browser to full window, it may not work correctly in small window.

4. The page will appear with default properties such as "Number of frames, Window size, Timeout(s), Speed". Please feel to change the values of them and the values must be in numeric.

5. The simulation area, the sender's "ready frames" will appear in the top and receiver's "expected frame" slots will appear in the bottom of the simulation area.

6. Sliding window is marked in red color and it covers the frames those are ready to get transmitted from sender.

7. Some of the quick simulation controls are specified below:
	- Perform a mouse click on required "ready info frame"  (frame 0, frame1,....frameN) on sender side to issue damaged "Info Frames"
	- To damage or kill a moving frame or ACK, feel free to click on it. This will make frame to be lost/damaged.
	- Click on "Stop" button any time to completely stop the simulation and get page refreshed.

8. Click on green color "Start" button to start the simulation. This will start generating RR ACK if the below steps are not performed yet.

9. REJ ACK Simulation: In order to simulate damaged info frame, please click on the frame on the sender side before it gets transmitted. As soon as you click on the sender side frame, it will appear in black color and it will send damaged from to receiver.

10. ACK Poll/Final Command Simulation: The ACK Poll frame is issued by sender when RR ACK is not received in a specified time. In order to simulate this case, either click on the moving info frame or RR frame to kill. Then, please wait for specified timeout time to see ACK Poll get issued from sender and wait to see the ACK Final from receiver.

## Assumption:
1. We do not display running timer on screen, however, the timer is running on the specified interval and keeps polling until RR ACK is received for a frame sequence. So, please wait until the timer expires to send the poll request.
2. We assumed that killing a ACK is similar as damaging it.
