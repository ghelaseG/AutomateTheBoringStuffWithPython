For Chapter 14 - "Working with Google Sheets" from Automate the Boring Stuff with Python(2nd Edition) by Al Sweigart, steps for the practice project:

  * Downloading Google Forms Data
  * Converting Spreadsheets to Other Formats
  * Finding Mistakes in a Spreadsheet

First thing I did was to login on "Google Cloud Platform" to enable two important API - I used this webiste https://console.cloud.google.com, after I've login with my details and created a new project (if you did it, and you want to make a new project -> follow the next images).

<img width="789" alt="Screenshot 2022-04-12 at 21 26 52" src="https://user-images.githubusercontent.com/96828940/163048750-f62a63e3-4e28-40de-bb93-982f228f0e11.png">
<img width="729" alt="Screenshot 2022-04-12 at 21 27 09" src="https://user-images.githubusercontent.com/96828940/163049142-d8ecc5db-626b-41bf-8a2e-6c289ba35216.png">
<img width="518" alt="Screenshot 2022-04-12 at 21 27 36" src="https://user-images.githubusercontent.com/96828940/163049318-948c5931-47fd-488b-91d5-dba91d444ca8.png">


On the search bar I simply wrote Google Sheets API and I pressed Enable, and then I wrote again on the same search bar Google Drive API and I pressed Enable (you can also use the links from the book - https://console.developers.google.com/apis/library/sheets.googleapis.com/ 
                                                 - https://console.developers.google.com/apis/library/sheets.googleapis.com/ )

<img width="802" alt="Screenshot 2022-04-12 at 21 13 38" src="https://user-images.githubusercontent.com/96828940/163046071-3897e354-c996-44de-85c7-b6ade488cffe.png">

<img width="1762" alt="Screenshot 2022-04-12 at 21 14 49" src="https://user-images.githubusercontent.com/96828940/163046182-a138f2c3-a3d1-40d0-b707-1f7a6d1f060c.png">
                                                      
Then I pursue to download the json file. At first I failed so in order for you to don't do it, please follow the next steps.
  After you pressed enable at the last API - Google Drive - it will send you on the page presented in the next image.
  
<img width="965" alt="Screenshot 2022-04-12 at 21 39 01" src="https://user-images.githubusercontent.com/96828940/163050265-5cb545a4-e06e-47a8-a61e-c1ae8c3c2437.png">

Ok, now press on Credentials and go on +Create Credentials - here do not select the first row API key as it will not help you (what I saw its for gspread module)

<img width="887" alt="Screenshot 2022-04-12 at 21 39 46" src="https://user-images.githubusercontent.com/96828940/163050495-b46c08e2-83ef-4b7d-b113-adbde52b9428.png">

Choose Desktop App.

<img width="697" alt="Screenshot 2022-04-12 at 21 39 59" src="https://user-images.githubusercontent.com/96828940/163050592-b833d6fe-5a84-459e-b117-9acb6adb757f.png">

Write any name you wish.

<img width="848" alt="Screenshot 2022-04-12 at 21 40 41" src="https://user-images.githubusercontent.com/96828940/163050685-3ba8dd63-f955-4063-a489-b11244210baf.png">

And finally, after you press Create it will let you download the json file. (please rename it to credentials-sheets.json)

<img width="804" alt="Screenshot 2022-04-12 at 21 41 04" src="https://user-images.githubusercontent.com/96828940/163051175-82131f0f-b64e-429e-9c73-ddcad5ac1db7.png">

Drag that file in the same folder where you created the project( I use PyCharm )

<img width="316" alt="Screenshot 2022-04-12 at 21 50 35" src="https://user-images.githubusercontent.com/96828940/163052316-607e8611-ec75-4080-b14f-44773639d184.png">

And make sure to "Publish the app", same as in next picture.

<img width="1061" alt="Screenshot 2022-04-12 at 21 41 58" src="https://user-images.githubusercontent.com/96828940/163052509-906e16fa-22a2-4c9a-bd57-b246e8e2a97b.png">

In the book it sends you to enable Google Sheets API with this link: https://developers.google.com/sheets/api/quickstart/python/ and then you can download the pickle files, well I haven't got this steps but the website they offer it's working in a total different way. (but it works, that's important)

After you follow the step 1 from the website, it will ask you to create a file quickstart.py and copy the code they provide and then place the python file in the same folder with the credentials-sheets.json. After you press Run it will automatically download this file token.json in the same folder.
  
<img width="1059" alt="Screenshot 2022-04-12 at 22 06 25" src="https://user-images.githubusercontent.com/96828940/163054739-0b1b7452-0f27-4ccf-b750-5ea31462e247.png">
<img width="317" alt="Screenshot 2022-04-12 at 22 07 14" src="https://user-images.githubusercontent.com/96828940/163054795-90350177-f87a-4c7e-aadf-86d7586a0094.png">

Now create a new Python File in the same directory, I chose to name it DownloadingGoogleFormsData.py as that's how it's called my new project. Then inside just write import ezsheets and run it. First time it will send you on the next website (see next image) and download, after you press continue, in the same folder the token-drive.pickle or tocken-sheets.pickle - sorry I can't remember the order, then do the same thing again, run quickstart.py and the Python FIle with import ezsheets again to download the second tocken-xyz.pickle.

<img width="649" alt="Screenshot 2022-04-12 at 22 12 41" src="https://user-images.githubusercontent.com/96828940/163055970-ab504573-e46a-4678-b17c-b0560b01a8a4.png">

Now after you completed all of this, it only remains to write the code I presented here inside the Python File - DownloadingGoogleFormsData.py

To get the unique ID to use next to Spreasheet you'll have to go at https://docs.google.com/forms/ get the link to your new form, complete it with what you want and then go to Responses and create new spreadsheet and copy the unique ID from there. Good luck!

<img width="1332" alt="Screenshot 2022-04-12 at 22 27 51" src="https://user-images.githubusercontent.com/96828940/163058455-b3be3403-1bf6-4145-a16d-a1193115a704.png">

I don't promise that this is the only way to do it, or is the only correct version of it, but I hope it will inspire some of you. Thank you!



 *  Licensed under the MIT License.

