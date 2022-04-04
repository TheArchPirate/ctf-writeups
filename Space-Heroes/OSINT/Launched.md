# Launched
- - -
What is the name of the launch and the payload in this picture. (flag format is shctf{rocket_payload}, spaces are underscores)

author: GlitchArchetype

![[launch.jpg]]

- - -

Reverse image searching didn't bring must of interest, however, this picture contained quite a lot of metadata that was very useful. To extract this data I used exiftool. Here is the output of that:

```
ExifTool Version Number         : 12.40
File Name                       : launch.jpg
Directory                       : .
File Size                       : 1035 KiB
File Modification Date/Time     : 2022:04:01 13:29:22-04:00
File Access Date/Time           : 2022:04:01 13:29:34-04:00
File Inode Change Date/Time     : 2022:04:01 13:29:24-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
Exif Byte Order                 : Big-endian (Motorola, MM)
Make                            : Apple
Camera Model Name               : iPhone 6
Orientation                     : Rotate 90 CW
X Resolution                    : 72
Y Resolution                    : 72
Resolution Unit                 : inches
Software                        : 12.2
Modify Date                     : 2019:04:11 18:36:33
Y Cb Cr Positioning             : Centered
Exposure Time                   : 1/1721
F Number                        : 2.2
Exposure Program                : Program AE
ISO                             : 32
Exif Version                    : 0221
Date/Time Original              : 2019:04:11 18:36:33
Create Date                     : 2019:04:11 18:36:33
Components Configuration        : Y, Cb, Cr, -
Shutter Speed Value             : 1/1721
Aperture Value                  : 2.2
Brightness Value                : 10.46362087
Exposure Compensation           : 0
Metering Mode                   : Multi-segment
Flash                           : Auto, Did not fire
Focal Length                    : 4.2 mm
Subject Area                    : 1632 1219 1794 1079
Run Time Flags                  : Valid
Run Time Value                  : 319531566998333
Run Time Scale                  : 1000000000
Run Time Epoch                  : 0
Acceleration Vector             : 0.02314408868 -0.9397569887 0.3482433259
Sub Sec Time Original           : 352
Sub Sec Time Digitized          : 352
Flashpix Version                : 0100
Color Space                     : sRGB
Exif Image Width                : 3264
Exif Image Height               : 2448
Sensing Method                  : One-chip color area
Scene Type                      : Directly photographed
Exposure Mode                   : Auto
White Balance                   : Auto
Digital Zoom Ratio              : 2.423762376
Focal Length In 35mm Format     : 70 mm
Scene Capture Type              : Standard
Lens Info                       : 4.150000095mm f/2.2
Lens Make                       : Apple
Lens Model                      : iPhone 6 back camera 4.15mm f/2.2
GPS Latitude Ref                : North
GPS Longitude Ref               : West
GPS Date Stamp                  : 2022:03:24
GPS Horizontal Positioning Error: 0 m
Compression                     : JPEG (old-style)
Thumbnail Offset                : 1948
Thumbnail Length                : 5701
Image Width                     : 3264
Image Height                    : 2448
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Run Time Since Power Up         : 3 days 16:45:32
Aperture                        : 2.2
Image Size                      : 3264x2448
Megapixels                      : 8.0
Scale Factor To 35 mm Equivalent: 16.9
Shutter Speed                   : 1/1721
Create Date                     : 2019:04:11 18:36:33.352
Date/Time Original              : 2019:04:11 18:36:33.352
Thumbnail Image                 : (Binary data 5701 bytes, use -b option to extract)
GPS Latitude                    : 28 deg 35' 9.60" N
GPS Longitude                   : 80 deg 39' 2.48" W
Circle Of Confusion             : 0.002 mm
Field Of View                   : 28.8 deg
Focal Length                    : 4.2 mm (35 mm equivalent: 70.0 mm)
GPS Position                    : 28 deg 35' 9.60" N, 80 deg 39' 2.48" W
Hyperfocal Distance             : 4.39 m
Light Value                     : 14.7
Lens ID                         : iPhone 6 back camera 4.15mm f/2.2

```

We see there is a date of 11 April 2019 and there are latitude and longitude values. We can modify the GPS positon to see where this is using Google maps:

```
28°35' 9.60"N 80°39'2.48"W
```

https://www.google.co.uk/maps/place/28%C2%B035'09.6%22N+80%C2%B039'02.5%22W/@28.5868384,-80.6540164,15.54z/data=!4m5!3m4!1s0x0:0x49b5622c695396d0!8m2!3d28.586!4d-80.6506889

This will show us that the locaiton is the Kennedy Space Centre. Now we can look for rockets launched on the 11 April from the Kennedy Space Centre. Wikipedia contains a [list of rockets launched in 2019](https://en.wikipedia.org/wiki/2019_in_spaceflight). In the table there exists an entry for the Falcon Heavy carrying ArabSat-6a.

![[flacon-heavy-2019.png]]

We can now build the flag

- - -

**Flag**
shctf{falconheavy_arabsat-6a}
