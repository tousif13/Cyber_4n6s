# Time Zone Conversion

![image](https://user-images.githubusercontent.com/33444140/234938598-a5cb24f1-19ef-474b-ad43-23c097ecccc7.png)

`UTC = Local Time - (Local Time Offset)`

`Local Time = UTC + (Local Time Offset)`

## Exercise 1

### 1. Convert the following timestamps from their local timezone to UTC

### a. 07/03/2021 15:05:00 EDT

    UTC = 15:05:00 - (-4)

    07/03/2021 19:05:00 UTC
### b. 05/03/2018 19:30:16 PST

    UTC = 19:30:16 - (-8)
    
    05/04/2018 02:30:16 UTC

### c. 11/05/2020 03:45:00 AEST

    UTC = 03:45:00 - (+10)
    
    11/04/2020 17:45:00 UTC
    
### d. 01/23/2019 23:33:02 CST

    UTC = 23:33:02 - (-6)
    
    01/24/2019 05:33:02 UTC
    
### 2. Convert the following timestamps from UTC to Eastern Timezone

### a. 02/25/2016 05:00:03 UTC
    
    Local = 05:00:03 + (-5)
    
    02/25/2016 00:00:03 EST
    
### b. 06/01/2015 04:56:13 UTC

    Local = 04:56:13 + (-4)
    
    06/01/2015 00:56:13 EDT
    
### c. 01/01/2019 15:30:00 UTC

    Local = 15:30:00 + (-5)
    
    01/01/2019 10:30:00 EST
    
### d. 03/01/2000 00:30:45 UTC

    Local = 00:30:45 + (-5)
    
    02/29/2000 19:30:45 EST
    
### 3. Convert the following timestamps from UTC to Pacific Timezone

### a. 04/02/2003 01:23:55 UTC

    Local = 01:23:55 + (-8)
    
    04/01/2003 17:23:55 PST
    
### b. 04/02/2006 02:55:23 UTC

    Local = 02:55:23 + (-8)
    
    04/01/2006 18:55:23 PST
    
### c. 12/05/2019 21:44:24 UTC

    Local = 21:44:24 + (-8)
    
    12/05/2019 13:44:24 PST
    
### d. 10/29/2017 22:00:00 UTC

    Local = 22:00:00 + (-7)
    
    10/29/2017 15:00:00 PDT

### 4. True or False: Local time was reported as February 28, 2020, 20:20:30 EST. Its time in Coordinated Universal Time is February 29, 2020, 01:20:30 UTC.

    True

# File Operations

> Standard Information will record changes and timestamps associated with the raw content of the file.

> Filename attribute will record timestamps associated with the creation of a file's metadata on an individual volume , typically only getting updated upon copying a file or moving it to another volume.

![image](https://user-images.githubusercontent.com/33444140/235131592-d0c7623b-efc3-4584-a9dc-32f7cc88f4c2.png)

![image](https://user-images.githubusercontent.com/33444140/235131672-e287551e-71e0-4320-8232-07081807808a.png)

## Exercise 2

## Task 1 : Inspecting MAC Timestamps

### The following questions should be answered for the files in \Task1\C5W_timestamps.zip. Assume that the host that these files were generated on is in Eastern Timezone

### 1. Was the target host on Eastern Standard Time or Eastern Daylight Time when these files were acquired?

    The target was on the Eastern Daylight Time when these files were acquired as the files were acquired at July, May, November 0f 2020,2021 which falls under Eastern Daylight Time.

### 2. Why are the Modified and Created timestamps on cybersecurity-image.png the same? What may this indicate?

    Modified and Created timestamps are same means that it is created once and no modification is done from the time of creation. This indicates that cybersecurity-image.png is downloaded at Created Timestamp time and didn't got modified.
    
### 3. When was sample_textdoc.txt first saved? What does the Modification time indicate?

    sample_textdoc.txt first saved on 2021-Jul-05 23:23:05. The Modification time indicates that the file is modified later as it's time is 2021-Jul-05 23:29:06.
    
### 4. What are the MAC timestamps for Notes.csv? What is the most likely reason that the Modified date is earlier than the Created date?

    M - Modified - 2020-May-10 18:34:28
    A - Accessed - 2021-Jul-30 07:33:48
    C - Created  - 2021-Jul-04 20:33:48
    
    The reason that the Modified date is earlier than the Created date is that the file is downloaded/moved which is already written/modified at some other place.
    
### 5. Look at anotherdocument.txt's MAC timestamps. What is the most likely reason that the Modified date is earlier than the Created date?

    This file too downloaded/moved which is already written/modified at some other place and it may also be due to the Daylight Savings.
    
### 5.a. Bonus: What are anotherdocument.txt's MAC timestamps in UTC?

    M - Modified - 2020-Nov-01 06:02:02
    A - Accessed - 2021-Jul-30 07:33:48
    C - Created  - 2020-Nov-01 05:59:50
    
## Task 2: File Metadata

### 1.In the Recycle Bin, "$I" files are generated to contain the metadata for a deleted file. Its hex code will detail the original file's size in bytes, deletion time, and path. For more information about Recycle Bin file format, refer to Cyber5w's Recycle Bin course. The information for its deletion time can be found at byte 0x10, and is 8 bytes long. For more information about Endianness, refer to Cyber5w's Computer and Data Representation course. Use DCode to conduct the following:
### a. Open Task2\$Recycle.Bin_backup\$I111B13.jpg in a hex editor and locate its deletion time. Highlight the 8 bytes from byte 0x10 to 0x17, and copy the selection in Hexadecimal, Little Endian

![image](https://user-images.githubusercontent.com/33444140/235157483-b3ceb0e0-f194-4299-8852-db03c952d6e6.png)

### b. How many bits are in 8 bytes?

    64 bits
    
### c. Open DCode and paste the hex  inthe "Value to Decode" field. In the "Decode Format" dropdown menu, select Windows: 64 bit Hex Value -Little Endian", then press "Decode"

![image](https://user-images.githubusercontent.com/33444140/235160572-af065acc-c728-4069-b421-42cd31d4f13e.png)

### d. What is this file's deletion time in UTC?

    2021-06-28 02:51:04
    
### e. Assuming that this file was deleted in Eastern Time originally, what was the local time that the file was deleted?

    02:51:04 + (-4)
    2021-06-27 22:51:04 EDT

### 2.Many archive files, such as ZIP, RAR, 7Z, and Microsoft DOCX use timestamps to identify times that its containing files were created. For ZIP files, this timestamp can be located at bytes 0x0A to 0x0D (11th to 14th bytes) relative to the start of that entry's File Record. However, this 4-byte segment can be interpreted as 2 Little Endian bytes for the File Time (DOStime) and 2 Little Endian bytes for the File Date (DOSdate), which can be manipulated to be interpreted as MS-DOS: 32-bitHex Value in localtime. This is particularly useful for password-encrypted ZIP files that cannot be extracted through normal means.

### a.Open c5w_timestamp-Sample.zip in a hex editor and locate the first entry's creation timestamp (should be at 0xA-0xD). Highlight the 4 bytes at that location in Hexadecimal, Little Endian.

![image](https://user-images.githubusercontent.com/33444140/235220553-27b14c5d-0d20-4f3c-997a-4adb6f539f5d.png)

### b. How many bits are in 4 bytes?
    
    32 bits
    
### c. Open DCode and paste this value into the "Value to Decode" field, applying the "Decode Format:" equal to "MS-DOS: 32-bitHex Value.

![image](https://user-images.githubusercontent.com/33444140/235165428-4311dea5-bd37-44a6-b735-2c9e77a2ec6e.png)

### d. What time was this file created?

    2021-03-23 09:14:42
   
### e. What timezone is stored in archive files?

    Local

### 3.Certain file types will include "ExifData", which is usually metadata about an image and the camera that took it. The most common file type that will include Exif Data is JPG files. Exif data usually includes a lot of information, such as the make and model of the camera that took the picture, the resolution of the picture, the GPS location that the picture was taken at, the camera's lens configuration, exposure, color encoding, flash, field of depth, time the file was taken, and more. This data can be read in Phil Harvey's ExifTool, a hex editor, an Exif Data Viewer online.

### a. Open c5w_exif-pink_rose.jpg in a hex editor andreview its Exif data (look for the word, "Exif"). Most of the Exif data should be in plaintext, making it readable without decoding it.

![image](https://user-images.githubusercontent.com/33444140/235222823-37295ef2-5726-489c-83aa-238568af7ec1.png)

### b.The Exif data will automatically save the time in localtime, the timezone that the file was taken in. Based on parsing the file in a hex editor, what time was the picture taken?

![image](https://user-images.githubusercontent.com/33444140/235221762-a0fa542f-99ca-40ae-a394-b1e62ce5cddd.png)

    2018-06-09 17:32:50
   
### c.Verify the hex timestamp by comparing it to the output of exiftool. Run exiftool(-k).exe against c5w_exif-pink_rose.jpg by issuing the command, "exiftool(-k).exe c5w_exif-pink_rose.jpg". What timestamp does it show that the photo was taken?

![image](https://user-images.githubusercontent.com/33444140/235228269-70af0698-8f3b-453f-8c03-fc44ee4fa6ca.png)

![image](https://user-images.githubusercontent.com/33444140/235228717-99ca18e3-b684-4bd4-a237-1f332a4e88e0.png)

### d.Bonus: What time was the picture taken in UTC? Hint: See what other information is stored in Exif metadata that can help you locate the appropriate timezone.

![image](https://user-images.githubusercontent.com/33444140/235228966-0139c01d-bb8b-462b-a887-5bb0f99a3fd5.png)

    The GPS co-ordinates of this photo is 48 deg 50' 48.73" N, 2 deg 20' 3.31" E which is location of Paris, France. The local timezone of Paris is CEST (Daylight time) which is +2 of UTC offset.
    
    So, 17:32:50 - (+2)
    2018-06-09 15:32:50 UTC
