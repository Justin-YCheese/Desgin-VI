# Lab 5 Procedure

I have a Windows and Raspberry Pi setup.

## 1) Install Mosquitto on Windows

[Download Mosquitto on Windows](https://mosquitto.org/download/)

I skipped adding Visual Studio Runtime.  

<img width="386" alt="image" src="https://user-images.githubusercontent.com/70534623/159603686-933331e2-bd0d-4ff0-a7bd-bc3d1cac024a.png">

Then add "C:\Program Files\Mosquitto" to path environment variables 

## 2) Install Mosquitto on Raspberry Pi and test

<img width="265" alt="image" src="https://user-images.githubusercontent.com/70534623/159606019-bed9c67b-1531-46b3-b709-41963b27304e.png">

## 3) Testing Subcription

<img width="910" alt="image" src="https://user-images.githubusercontent.com/70534623/159605942-5e5ea43c-5d14-4695-8b6e-49543f0f4e3b.png">

## 4) Install Paho 

<img width="430" alt="image" src="https://user-images.githubusercontent.com/70534623/159606461-8b701247-c21e-4b1a-b493-7ef57bcfef37.png">

<img width="602" alt="image" src="https://user-images.githubusercontent.com/70534623/159606777-f2b792e8-8e1d-46bc-b5fd-8e111c865f27.png">

I cloned paho.mqtt.python.git into the "iot" directory just so it was more organized

# Run python code

## Single:

<img width="905" alt="image" src="https://user-images.githubusercontent.com/70534623/159607999-cd7886cc-1359-4bb3-823d-e4c979ce8036.png">

I thought that I needed to run "client.py" while subscribing, but you just need "sub.py" and "pub.py"

<img width="617" alt="image" src="https://user-images.githubusercontent.com/70534623/159608531-b437a6a6-2cf5-4b97-bbd5-0b9d3927ee98.png">

## Multiple:

<img width="791" alt="image" src="https://user-images.githubusercontent.com/70534623/159609168-4cf6a447-f613-4a98-adcd-9b00b12fd84d.png">

## CPU:

<img width="647" alt="image" src="https://user-images.githubusercontent.com/70534623/159609700-4760863c-7992-430e-84e0-aa98c6eb8a70.png">

## Interrupts (Custom):

<img width="835" alt="image" src="https://user-images.githubusercontent.com/70534623/159614039-7abf0257-1385-4749-ae95-810876a8a762.png">

I made some edites to the cpu code. I tried to use [psutil](https://psutil.readthedocs.io/en/latest/#) to instead publish number of interrupts since boot.

<img width="574" alt="image" src="https://user-images.githubusercontent.com/70534623/159612401-40adce05-d293-470c-bf0d-53394a50b767.png">

I speed up the publishing rate and changed the data to interrupts. I found that as long as the subscription  
and publishing functions have the same string, then they will listen to each other.  
I also made the mistake of using a tab instead of 8 spaces which with python results in an error.

<img width="722" alt="image" src="https://user-images.githubusercontent.com/70534623/159614186-27adff80-f502-428d-bbfe-67699e12143c.png">

## Temperature and CPU usage:

<img width="872" alt="image" src="https://user-images.githubusercontent.com/70534623/159615662-477af0aa-3d4f-4a55-b369-edffda1da658.png">

I made some edite with what I learned from my first attempt.

<img width="789" alt="image" src="https://user-images.githubusercontent.com/70534623/159615779-19dee77c-02f7-43f0-a4a3-523479966895.png">

Also the extra message worked...

<img width="190" alt="image" src="https://user-images.githubusercontent.com/70534623/159615857-41e74305-d128-4a90-886c-0fd4ac394bac.png">
