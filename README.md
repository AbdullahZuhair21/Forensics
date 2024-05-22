# Forensics

# Pictures
use the following:

1. Hexeditor file.jpg
![image](https://github.com/AbdullahZuhair21/Forensics/assets/154827329/c6e9ca2a-8f1a-4b5a-a359-3ceacd46ab8b)

2. exiftool (information reader)
3. strings 
4. binwalk (analysis tool)
5. zsteg (detect hiding data in PNG & BMP)
6. steghide (extract the text from a pic) `steghide extract -sf picture3.png`
# PCAP file
check `Statistics` tab > focus on Data > right click and apply filter > follow TCP/UDP packet

# wav file
you need to convert it to image/audio then get the flag

# encypted file using hexdecimal 
the value of the file after using hexeditor is `E2 80 83` for all. this means the file is encypted. [convert Hex to Binary => Binary to ASCII]

![image](https://github.com/AbdullahZuhair21/Forensics/assets/154827329/a5ec5911-5a5a-40f6-abb3-f32d13e29a23)

1. to decrypt the file replace `E2 80 83` with zeros `30` 

![image](https://github.com/AbdullahZuhair21/Forensics/assets/154827329/618f1d0f-c354-4bf0-be44-e5aef34447b0)

2. now replace the spaces `20` with ones `31`

![image](https://github.com/AbdullahZuhair21/Forensics/assets/154827329/fb2ab7bf-02c0-4c5b-ac41-be3b2f2dbe00)

3. decode binary to ascii

![image](https://github.com/AbdullahZuhair21/Forensics/assets/154827329/f8fce585-fe71-45c3-a485-b51c5f956927)

# hex format for files
![image](https://github.com/AbdullahZuhair21/Forensics/assets/154827329/1aa159a2-5aa0-48b5-87e4-79261c3a6db7)

if you got a corrupted file check it's close to which format then you can edit it using a hexeditor 

for example, the following file is corrupted and it's close to PNG format. PNG format starts with `89 50 4E 47 0D 0A 1A 0A`

![image](https://github.com/AbdullahZuhair21/Forensics/assets/154827329/f0ebe76d-cae7-4c19-81f5-fc3cf935ccae)

# Log file 
if you get a log file use Registry Viewer to check the Running application. don't forget to remove the null bytes in the case of copying a based64

Software => Microsoft => Windows => Current Version => Run

# photo's forensics
Hex is represented in hex-editor as little indian not big Indian. you can check the hex value of a number using python then `hex(150)`. use exiftool to get some of the values like image width and height
