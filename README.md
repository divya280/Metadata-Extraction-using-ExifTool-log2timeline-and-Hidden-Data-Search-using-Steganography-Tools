# EX-6 : METADATA EXTRACTION USING EXIFTOOL USING EXIFTOOL LOG2TIMELINE AND HIDDEN DATA SEARCH USING STEGANOGRAPHY TOOLS
#### NAME : V DIVYASHREE
#### R.NO : 212223230051
## AIM :
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.
## REQUIREMENTS :
- **Operating System:** Kali Linux (preferred) or any Linux distro with forensic tools
- **Tools:**
     -  ExifTool – For metadata extraction
     -  plaso/log2timeline – For timeline analysis
- **Steganography tools:** steghide, zsteg, binwalk
- **Test Data:** Image, video, and document files (some with embedded hidden data)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Sample Files - Images, Videos, Documents] --> B[Metadata Extraction with ExifTool]
    B --> C[Event Timeline Creation with log2timeline]
    C --> D[Hidden Data Search with Steganography Tools]
    D --> E[Evidence Analysis and Documentation]
```
## DESIGN STEPS :
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM :
| Step | Action                  | Tool                 | Output                           |
| ---- | ----------------------- | -------------------- | -------------------------------- |
| 1    | Extract file metadata   | ExifTool             | Metadata fields, GPS, timestamps |
| 2    | Generate event timeline | log2timeline / plaso | CSV/HTML timeline                |
| 3    | Search for hidden data  | steghide / binwalk   | Extracted hidden files           |
| 4    | Document findings       | Manual report        | Investigation record             |


## OUTPUT :
### A. Using ExifTool – for file metadata
- **Install:**
```bash
sudo apt update
sudo apt install exiftool -y
```
- **Extract metadata from a file:**
```bash
exiftool image.jpg
```
- **Batch process a folder:**
```bash
exiftool -r /path/to/folder
```
- **Useful flags:**
  
- ```-G: Show metadata group```

- ```-time:all: Show only timestamps```

- ```-GPSLatitude -GPSLongitude: Extract GPS data```

<img width="1920" height="1085" alt="image" src="https://github.com/user-attachments/assets/23f07bad-eda4-4952-a0a8-090d152807db" />



### install log2timeline
```
sudo apt install plaso -y
```

```
sudo apt install steghide -y
```
- **Embed data**
```
steghide embed -cf /home/kali/Downloads/new.jpg -ef /home/kali/Downloads/secret.txt
```
<img width="1920" height="1085" alt="image" src="https://github.com/user-attachments/assets/c865fa4d-a66f-4c5b-8e2a-fc22cc834d09" />


- **Extract hidden data:**
```
steghide extract -sf new.jpg

```
<img width="1920" height="1085" alt="image" src="https://github.com/user-attachments/assets/35e9c765-01ee-412d-b6fe-4fd03ee32a1d" />


### Using binwalk – for file analysis
```bash
sudo apt install binwalk -y
binwalk suspicious.jpg
```
```bash
binwalk /home/kali/Downloads/wallpaper.jpg
```

<img width="1920" height="1085" alt="image" src="https://github.com/user-attachments/assets/3b966427-b682-4c0f-a867-d20c5e923f5f" />

## OUTPUT :

Extracted Metadata, Timeline Events, and Hidden Data Detection Results
<img width="1385" height="964" alt="image" src="https://github.com/user-attachments/assets/6315d6e2-fb41-4416-9f94-76a5eab812bc" />


## RESULT :
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.
