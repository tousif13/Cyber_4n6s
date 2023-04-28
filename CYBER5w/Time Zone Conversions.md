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

    The target was on the Eastern Daylight Time when these files were acquired as the files were acquired at Aug 10 2021 which falls under Eastern Daylight Time.

### 2. Why are the Modified and Created timestamps on cybersecurity-image.png the same? What may this indicate?

    It means that it is created once and no modification is done from the time of creation.
    
### 3. When was sample_textdoc.txt first saved? What does the Modification time indicate?

    sample_textdoc.txt first saved on 2021-Jul-05 23:23:05. The Modification time indicates that the file is modified later as it's time is 2021-Jul-05 23:29:06.
    
### 4. What are the MAC timestamps for Notes.csv? What is the most likely reason that the Modified date is earlier than the Created date?

    M - Modified - 2020-May-10 18:34:28
    A - Accessed - 2021-Jul-30 07:33:48
    C - Created  - 2021-Jul-04 20:33:48
