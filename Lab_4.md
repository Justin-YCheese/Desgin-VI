#Lab 4 Progress
Setting up a server.

## 1) Installed Django and Django REST  
<img width="243" alt="image" src="https://user-images.githubusercontent.com/70534623/159195000-cfb35f9f-fd84-4a50-890d-d6abc9e77ea0.png">

## 2) Install MariaDB server and client  
<img width="278" alt="image" src="https://user-images.githubusercontent.com/70534623/159195141-f43ae6ed-46d4-4d37-8dd0-d53d969a2ae1.png">

## 3) Start a Django project  
<img width="296" alt="image" src="https://user-images.githubusercontent.com/70534623/159195607-57dfa6e5-4dff-43eb-8154-3da33a9096f4.png">

## 4) Start Django App  
<img width="335" alt="image" src="https://user-images.githubusercontent.com/70534623/159195727-26c3c609-e0f0-4dc9-9f78-8cdbf96a02f9.png">  
I had a small problem where I didn't realize I just had to type "python 3 manage.py startapp myapp" because the picture wasn't color coded

## 5) Create MySQL database
<img width="379" alt="image" src="https://user-images.githubusercontent.com/70534623/159196126-43a47c4d-2e9a-484f-bc72-d3a76d239012.png">  
I found that if you don't include the semicolon at the end, then you can't finish the command except for certain commands like "quit"

## 6) Edit settings.py in ~/stevens/stevens
<img width="370" alt="image" src="https://user-images.githubusercontent.com/70534623/159196602-504c5090-cbf2-4f97-babc-05a1846beee4.png">

[Instruction Link](https://github.com/kevinwlu/iot/blob/master/lesson4/stevens/settings.txt)  

I didn't know what "change PASSWORD for MySQL user pi" meant so 

## 7) Copy urls.py to ~/stevens/stevens
<img width="391" alt="image" src="https://user-images.githubusercontent.com/70534623/159196990-274e05da-5c8a-4484-b8aa-10a6756954f4.png">

## 8) opy admin.py, models.py, and views.py to ~/stevens/myapp
<img width="414" alt="image" src="https://user-images.githubusercontent.com/70534623/159197017-c7ceb131-0b80-44be-8ee5-433688633808.png">

## 9) Copy index.html
<img width="486" alt="image" src="https://user-images.githubusercontent.com/70534623/159197126-3c9193b8-dcb3-4cc5-aa7f-715ec162dad3.png">

## 10) Created API Key  

[Google API Instructions](https://developers.google.com/maps/documentation/javascript/get-api-key)   

I didn't setup a free trial. I just used my personal gmail account to generate an API key. I specifically skipped the "Before you begin" part.
But I did restrict the API key to work only for HTTP referrers

## 11) Edit index.html to add the Google Maps API key
<img width="454" alt="image" src="https://user-images.githubusercontent.com/70534623/159197887-17f5a9db-eb1d-422a-b5b7-e2a9cfd60d6d.png">

## 12) Copy static files
<img width="434" alt="image" src="https://user-images.githubusercontent.com/70534623/159197904-f422a36b-4c47-4c0e-8b3d-ba00f807b141.png">

## 13) Manage
<img width="368" alt="image" src="https://user-images.githubusercontent.com/70534623/159198199-a3d339cc-28d8-42fe-9ab4-25c3321f9846.png">

## 14) Run Django server
<img width="358" alt="image" src="https://user-images.githubusercontent.com/70534623/159198617-4f4da703-011b-42c5-a285-68f16bdfc6c5.png">
I saw a way to customize the ip in Mitchell Reiff's github so I gave my server a custom ip. But I found that many of the 'ip's I tried didn't work, like 2.0.0.0:8000 or 128.0.0.2:8000. I'm not sure way and I didn't find a solid answer online.

## 15) Connect with VNC
<img width="369" alt="image" src="https://user-images.githubusercontent.com/70534623/159198922-82e3450d-d186-4035-a9c2-61797e8516fc.png">
I kept getting this error even with the default ip address. But then I realized that I'm not supposed to connect to the website with VNC on my laptop, but just open a webbrowser in the Raspberry Pi with that URL.
I made the Super user "SporkyUper" and kept my password the same.
<img width="838" alt="image" src="https://user-images.githubusercontent.com/70534623/159199172-1d25aca9-3796-4b14-8be1-ec24c6274746.png">

## 16) Temperature
<img width="431" alt="image" src="https://user-images.githubusercontent.com/70534623/159199494-67840e90-0387-4b0c-8e6c-b46dc27a24b5.png">
<img width="323" alt="image" src="https://user-images.githubusercontent.com/70534623/159199288-6459a93e-3387-4528-ab5a-e4bcad3ece56.png">
I couldn't type out "Fahrenheit" in temperature so I just put "F"

Then I realized that what I put in was wrong but It works for the example. And hey, the Map works!. I didn't need that free trial.
Also the Raspberry Pi's web browsing was very slow. With alot of latency.

This is me doing Website Stuff (It's fairly slow)

https://user-images.githubusercontent.com/70534623/159201755-e281c8fa-588e-4b6a-b74c-5238962310d4.mp4

This is me messing around with the map (Also slow)

https://user-images.githubusercontent.com/70534623/159201233-d30976d0-29dc-4d38-ab3f-4adfc117c6da.mp4

17) Try on your computer
<img width="751" alt="image" src="https://user-images.githubusercontent.com/70534623/159199739-3edc6300-0184-4ff4-a03e-509a6d4e5de1.png">
<img width="794" alt="image" src="https://user-images.githubusercontent.com/70534623/159199704-8754d9d9-c4a4-4046-8aba-bd38dde2bd73.png">


