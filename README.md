# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report
<img width="1919" height="1078" alt="Screenshot 2025-09-20 144515" src="https://github.com/user-attachments/assets/94223c5a-42fa-4595-b701-262c9719d986" />

<img width="1694" height="945" alt="Screenshot 2025-09-20 144642" src="https://github.com/user-attachments/assets/fcc534ac-4370-4ed7-82b5-fd3a64c67cc2" />

<img width="1682" height="906" alt="Screenshot 2025-09-20 144700" src="https://github.com/user-attachments/assets/b270080b-abf7-4fe2-9ade-1c350a26e67a" />

<img width="1063" height="668" alt="Screenshot 2025-09-20 144813" src="https://github.com/user-attachments/assets/6a5580da-7e58-4617-aed6-13847235ccf1" />

<img width="1688" height="953" alt="Screenshot 2025-09-20 144909" src="https://github.com/user-attachments/assets/e53cd657-bf55-4d30-af4c-efe8804dc5bd" />

<img width="1919" height="970" alt="Screenshot 2025-09-20 145039" src="https://github.com/user-attachments/assets/82d467d6-ae73-4925-9a17-a75cf6901212" />



## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

