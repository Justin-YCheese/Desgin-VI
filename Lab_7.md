# ThingSpeak  
I logged in using my Stevens Account on my laptop.
## Create new channel cpu_loop with field1 cpu_pc and field2 mem_avail_mb  
<img width="856" alt="image" src="https://user-images.githubusercontent.com/70534623/163013517-32e6f6a3-83da-493a-9f4a-cc874662304d.png">

## Get Write API Keys  
<img width="869" alt="image" src="https://user-images.githubusercontent.com/70534623/163017334-470aa4a9-0c96-4f31-aff4-fd95c8a17143.png">

## On Pi: Run code and use API Keys  
<img width="331" alt="image" src="https://user-images.githubusercontent.com/70534623/163017505-f5fefed1-b823-450b-a352-eaa3b6a8a9d9.png">

## Results  
<img width="529" alt="image" src="https://user-images.githubusercontent.com/70534623/163018813-1a2bdb29-20ec-4802-90f1-1c596af9c0ea.png">

<img width="826" alt="image" src="https://user-images.githubusercontent.com/70534623/163018596-d2039fc4-875b-4c8c-ac43-4d0ec7c6dfe0.png">

## New code
But I want to try and record some extra data and name the graphs so I try to edit the code.  
If you don't have system_info in the directory, then copy it "cp ~/iot/lesson3/system_info.py ."  
I added "from system_info import get_temperature" to get the temperature  
thingspeak_cpu_loop  
<img width="691" alt="image" src="https://user-images.githubusercontent.com/70534623/163021342-f5ad2136-3fb1-4ee6-9fdc-570a30b205d4.png">

thingspeak_feed  
<img width="686" alt="image" src="https://user-images.githubusercontent.com/70534623/163022512-e38fdfbe-704b-47c3-943e-2b6989fc851b.png">

I also added code to print the extra data but it's mostly unimportant.

When I first ran the code, Thingspeak didn't update because the Write API key had changed.
But because I had previously said to save the API key when first running thinkspeak_feed.py I had to run "rm API_KEY.pickle"
to remove the saved API key. I ran thinkspeak_feed.py again and it promts me to add a Key so I use the new API key.

## New code Results

<img width="616" alt="image" src="https://user-images.githubusercontent.com/70534623/163034083-606c20a9-199e-435f-854c-d04b67f828d2.png">

First, the pi was left alone. The memory available easily shows when I did certain things. The first drop is when I tried to run youtube and load a video,
but the video couldn't load. Then I let the pi rest, then just opened the web browser, which aparently took about half of the memory. After that I closed it
and left the pi alone again.

<img width="960" alt="image" src="https://user-images.githubusercontent.com/70534623/163027937-6b88d707-48d2-46bb-964e-d8203b3402e7.png">

Whenever the pi was busy, the number of interrupts raised faster, and the cpu percentage usage spiked. But it seems that the temperature didn't work as it
was stuck at 0 for the whole time.

If you want the code, check the [lab_material](https://github.com/Justin-YCheese/Design-VI/tree/main/lab_material) folder.

# Google Sheets
## Sign up for json file
Sign up and log in the Google Cloud Platform Identity and enable Google Drive and Google Sheets API  
Create a Service Account with any infomration, then a json key. You will download a json file.  

I downloaded it on my laptop, so to put it on my pi I opened command promt, changed directory to my downloads folder, and ran:     
"scp rpidata-*.json pi@sporky:/home/pi/demo"  
Becayse I had previously changed my pi name.  

## Install Gspread and Oauth
sudo pip3 install -U gspread oauth2client

## Get rpi_spreadsheet.py to ~/demo  
I already have system_info.py so I don't need to copy it.  
I wanted to use the new rpi_spreadsheet file so I just made my own rpi_spreadsheet.py file with nano,
and pasted the new rpi file from the github.  

## Edit rpi_spreadsheet.py  
Set GDOCS_OAUTH_JSON to json file. (I renamed mine to rpidata-data.json)
and Set GDOCS_SPREADSHEET_NAME to google sheet name (Mine was named rpidata_sheet)

<img width="509" alt="image" src="https://user-images.githubusercontent.com/70534623/163046575-6357f3ac-cce7-40c0-a162-c2db7c9b83a7.png">

## Run rpi_spreadsheet.py  
python3 rpi_spreadsheet.py

<img width="504" alt="image" src="https://user-images.githubusercontent.com/70534623/163049891-95285086-5b1d-48c1-ac04-324876978402.png">

<img width="482" alt="image" src="https://user-images.githubusercontent.com/70534623/163049934-f1feb3fb-924f-48bc-8f5f-c44dce2980c0.png">

[Resulting Google Sheets](https://github.com/Justin-YCheese/Design-VI/blob/main/lab_material/rpidata_sheet%20-%20Sheet1.csv) (converted to csv)

