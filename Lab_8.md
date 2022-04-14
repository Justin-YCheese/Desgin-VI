# Lab 8 Procedures

## Getting Tenor flow
<img width="416" alt="image" src="https://user-images.githubusercontent.com/70534623/163458830-867e8e45-5b54-4205-aeb3-d94d4be3c5b1.png">

I have a raspberry pi so I tried to do it on that  
you can type "lsb_release -a" to check you Debian version. I have version 11.  
<img width="367" alt="image" src="https://user-images.githubusercontent.com/70534623/163458964-87e9330e-66ca-4005-b5db-87da0aeb0cc2.png">

I still tried to install with the instructions for Desbian 10 but I got an error when trying to install tenorflow  
<img width="359" alt="image" src="https://user-images.githubusercontent.com/70534623/163456637-24744bdf-f5f4-4b56-a31a-2ad27b15bc86.png">

<img width="620" alt="image" src="https://user-images.githubusercontent.com/70534623/163463656-e5755478-2ca6-46bf-8d15-6181a3c7bbd4.png">

I had to follow the [link](https://blog.d-and-j.net/deep-learning/2021/03/24/tensorflow-debian-11.html)

pip install -U --user keras_preprocessing --no-deps

I was struggling with downloading tenorflow, so I asked a friend for some help, but we ended up just trying to do the
rest of the Lab without Tenor Flow and found that we didn't need it.

## Coping data sheet to Pi

I used scp to copy rpidata_sheet to my Raspberry Pi demo directory  
    scp rpidata_*.csv pi@sporky:/home/pi/demo 

## Editing plt_final and plt_cv2

I made sure to change the title and the data sheet name. But when I first ran it, figure 1 was very short, and 
I realized I had to change the xticks parameter as well. Through checking the google sheet document, I added the apporpriate lables.

<img width="701" alt="image" src="https://user-images.githubusercontent.com/70534623/163466815-edb11b3b-e16d-4153-be03-2961e6a95900.png">

<img width="623" alt="image" src="https://user-images.githubusercontent.com/70534623/163462727-0baa9b16-cd87-4b2e-9534-916b231b1f75.png">

## Plt_Final

Figure 1

<img width="497" alt="image" src="https://user-images.githubusercontent.com/70534623/163466542-2419a862-bad1-4817-8af5-02a88cb2a782.png">

Figure 2

<img width="493" alt="image" src="https://user-images.githubusercontent.com/70534623/163463184-6e533579-1f59-4b83-8ef9-112fa4b12aef.png">

Figure 3

<img width="544" alt="image" src="https://user-images.githubusercontent.com/70534623/163463236-abe67edc-e758-4765-8fee-c158871d8e37.png">

Figure 4

<img width="510" alt="image" src="https://user-images.githubusercontent.com/70534623/163463267-403e4adc-516e-48a3-83ef-09ae13f4e02d.png">

Figure 5

<img width="587" alt="image" src="https://user-images.githubusercontent.com/70534623/163463304-be98489c-76ef-4e09-b097-f165e87c226b.png">

Figure 6

<img width="552" alt="image" src="https://user-images.githubusercontent.com/70534623/163463365-4caba5e9-c8ca-4683-9334-2ba513df7391.png">

## Plt_cv2

<img width="936" alt="image" src="https://user-images.githubusercontent.com/70534623/163463810-f0c20119-386e-4667-b5e5-6ece2f3935b2.png">

## Conclusion

Some of the data is messed up even though I had recorded data for 45 minutes. It's mostly because temperature from some reason kept reading as 0 even 
though I was running it on my Pi. But from figure 1 you can tell a story. I started by leaving the Pi, then browsing youtube, then leaving it again, 
and finally just opening the browser and leaving it.  

<img width="497" alt="image" src="https://user-images.githubusercontent.com/70534623/163466557-8df79349-b165-43bb-8357-6fd50bec3bfc.png">


