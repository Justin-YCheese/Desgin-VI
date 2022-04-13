# Lab 6 Procedure
  I have a pi and laptop setup

## Install Node-RED

I ran the command below to instal Node-RED on the pi

<img width="650" alt="image" src="https://user-images.githubusercontent.com/70534623/160293559-3267a5e9-c996-4175-9b20-a1966fd5f9fc.png">

Then I checked the versions

<img width="611" alt="image" src="https://user-images.githubusercontent.com/70534623/160293655-ff4781a0-8c65-4a8b-a8c2-0def2d9d713d.png">

## Run hello.js

When you run "node hello.js" you run a server that you can connect to

<img width="539" alt="image" src="https://user-images.githubusercontent.com/70534623/160293769-4f287f51-03d0-4d30-a7b2-d3062f697035.png">

Hello-world.js does the same thing

<img width="343" alt="image" src="https://user-images.githubusercontent.com/70534623/160293859-d6b15080-9559-431d-b355-9c026f3856e3.png">

## run http.js

But I had troubles running "http.js" I didn't do anything after waiting for a while and I couldn't figure out how to connect to it.  
So I started looking through the code.

hello-world.js

<img width="469" alt="image" src="https://user-images.githubusercontent.com/70534623/160294176-5a32fd28-e279-467c-93ad-75d2dba44a07.png">

hello.js

<img width="568" alt="image" src="https://user-images.githubusercontent.com/70534623/160294143-b156bb5c-841d-4f74-b814-1313a8bba286.png">

http.js

<img width="591" alt="image" src="https://user-images.githubusercontent.com/70534623/160294209-6286dac4-86a1-4fea-b8ad-38b8c9fa2f06.png">

After some testing, and figuring out that http.js listens to "8080".  
When I connect to 127.0.0.1:8080" on my pi the program will print 0 but then crash

<img width="850" alt="image" src="https://user-images.githubusercontent.com/70534623/160296060-3ec361da-b2f7-427a-8a50-dc50aa6bde10.png">

I tried changing the code so that data is always a string, but the same error still occured...

<img width="814" alt="image" src="https://user-images.githubusercontent.com/70534623/160296664-7ef9e670-4642-4c51-955f-1f68033456fc.png">

Even if I changed "test.txt" to something that must be a string it still gave me the same error...

<img width="513" alt="image" src="https://user-images.githubusercontent.com/70534623/160296804-ebea8800-9824-444b-a3c9-29658f85b03e.png">

So I have no idea why it's saying that data has to be a string or an "[instance of Buffer](https://nodejs.org/api/buffer.html#buffer)", the latter of which are  
<img width="718" alt="image" src="https://user-images.githubusercontent.com/70534623/160296929-6f13e507-ac9d-468d-868d-b1c93de7ee24.png">

## Pystache

Execute example commands

<img width="163" alt="image" src="https://user-images.githubusercontent.com/70534623/160297061-59389969-b4d0-44d7-a8d0-f327dd2d0c36.png">

<img width="736" alt="image" src="https://user-images.githubusercontent.com/70534623/160297128-bd4ab3b1-8158-48cb-aa2b-2a944ec29e19.png">

I edited the code a bit and printed some custom messages.

<img width="547" alt="image" src="https://user-images.githubusercontent.com/70534623/160297742-b7c83de4-3d43-469d-af1c-921ace071feb.png">

<img width="911" alt="image" src="https://user-images.githubusercontent.com/70534623/160297754-a4912be7-6149-4df0-b53d-d8805a688b56.png">

What I don't understand is why one would use renders to preparse strings when you could just use variables?  
Perhaps to compress the strings, and for increased readability.

## Update:  
So I recently talked with my dad about coding for internaltionalization, or I18N, and he told me how this can be used in combination with somekind of gettext() function and a resource file to prepare programs for localization. A resource file is a file of all the strings in a program that would have to be translated.



