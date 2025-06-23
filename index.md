# Voice Assistant with AI

<!---

<span style="background-color:blue">

<!--- You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions: -->

<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Irene L | Stratford Preparatory Blackford | Engineering | Incoming 8th Grader


<!--- **Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.** -->



<!--- ![Headstone Image](logo.svg) -->

![Headshot](2025bluestampheadshotformat.png)


  
# Final Milestone

<!--- 


<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE -->



# Second Milestone

<!---

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone -->

# First Milestone

<!---

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project -->



## Description

My first milestone was to obtain the OpenAI API key and to set up the raspberry pi to use and interface with it as a computer. I chose this project because it was very different from last year--more focused on software than hardware and using raspberry pi instead of Arduino--and because I wanted to learn about interacting with AI. Virtual Network Computing (VNC), Secure Shell (SSH), and Visual Studio Code (VS Code) were used to create a headless setup. I imaged the raspberry pi, renamed the it, created a host name to connect to it, used a rasperry pi camera (or pi camera) to take photos, and downloaded updates and upgrades into the terminals of Visual Studio Code and the raspberry pi.

## Components and Software

For hardware, I used the raspberry pi, a keyboard and mouse, an SD card, and an SD card reader. I downloaded a raspberry pi imager in order to image the SD card of the raspberry pi and create a host name that would later be used in Visual Studio Code to connect to the raspberry pi. For displays, I used OBS, which displays the raspberry pi screen and TigerVNC Viewer, which allows the computer's keyboard and trackpad to be used instead and allows use of the raspberry pi without plugging in the SD card reader to the computer. I downloaded Visual Studio Code to code in python as well as updates and upgrades into the terminal of VS Code. 

### Images

**Raspberry pi images**
![raspberrypiimage](censoredimage.png)
note: I did not have image to show this person's face, so I put a purple square over it.

This is one of the only pictures that I took with the raspberry pi camera that showed up in the raspberry pi's folder.

**Raspberry Pi setup**
![raspberrypissetup](rasppisetup.png)

## Challenges

When I was first imaging the raspberry pi's SD card, I forgot that the imager only imaged the SD card, so I imaged it twice by accident. Halfway through the second time, I remembered that it was only supposed to image the SD card, and the imager seemed to be frozen at 100% in the verify stage. Upon pressing the "cancel" on the screen, I corrupted the SD card, and when I received a new SD card, I almost corrupted that one too because the imager was frozen at 100% verify from the start. After thirteen minutes of waiting, the imager finally finished imaging the second SD card, allowing me to take it out and use it. Visual Studio Code needed updating after I started it up for the second time after a few days, and that prevented me from filming my milestone video sooner. My raspberry pi camera was not working at first even after I plugged it in twice, and I only realized after plugging it in again that I had not plugged it in deep enough and that I had to push it a little more even with the possibility of it breaking.


## Code
---
### Raspberry Pi Imager Code

``` python

from picamera2 import Picamera2, Preview
import time
import cv2
picam2 = Picamera2()
camera_config = picam2.create_still_configuration(main={"size": (1920, 1080)},
lores={"size": (640, 480)}, display="lores")
picam2.configure(camera_config)
#picam2.start_preview(Preview.QTGL) #Comment this out if not using desktop interface
picam2.start()
time.sleep(2)
im = picam2.capture_array()
im = cv2.cvtColor(im, cv2.COLOR_BGR2RGB)
cv2.imwrite('file.png', im)

```

<!--- ```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```
-->

# Starter Project
---
<iframe width="560" height="315" src="https://www.youtube.com/embed/f6nY_RwNvRg?si=etzqtukCnwUdpPpv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Description

I chose my starter project to be a jitterbug, which entailed soldering several parts onto the board because I had done the RGB slider the previous year and thought that this project would be a decent balance between difficulty (e.g. soldering and applications of soldering) and time consumption. The main components were the board, which was shaped like a bug, metal wire as the "legs" of the jitterbug, two red LEDs as the eyes, a switch, and a vibration motor, which causes the entire jitterbug to vibrate, or "jitter". The 5V nickel battery powers the LEDs and the vibration motor when the switch is turned on or flicked to the right.

![jitterbug](smalljitterbugpic.png)

***Fig 1:** an image of the jitterbug*
 
## Challenges

The jitterbug starter kit did not come with paper instructions, and the online instructions were rather unclear, so I looked at the picture and attempted to fit together the pieces how it was shown in the picture. I eventually figured it out by looking at the image more closely and stripping the wires. The vibration motor had two wires that needed to be soldered, but they were too thin to strip properly, and they did not fit properly like shown in the picture. I stripped the first one incorrectly and had to have the vibration motor replaced with another vibration motor that did end up fitting properly on the designated area, and I stripped it correctly and soldered it onto the board. These issues indirectly addressed and solved each other because of how all of the parts of the jitterbug are related to each other and how the placements affect each other.

![annotatedjitterbug](jitterbugpicannotated.png)

***Fig 2:** the yellow circle shows the vibration motor, allows the jitterbug to "jitter", and the red and blue wires are extremely thin--unable to be stripped with a traditional wire stripper*



## Next Steps

After finishing the starter project and reviewing soldering, I will have started my intensive project, and my first milestone is setting up my raspberry pi and obtaining an OpenAI API key. 


<!--- note: add picture of my own project if possible-->



# Bill of Materials
<!--- Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. -->

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
<!--- One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components. -->
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
