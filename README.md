# PixPack

<div align="center">
  <img src="https://github.com/BitPackTools/pixpack/blob/main/PicPack%20Logo.png?raw=true" alt="PixPack Logo" width=300/>
</div>

# PNG Data Embed/Extract Tool (LabVIEW)

This repository contains a LabVIEW tool for embedding and extracting custom data in PNG files.

## Possible Use Cases

- **Data + Image packaging:** Attach measurement data or analysis results directly to the corresponding image.  
- **Metadata storage:** Add experiment details, configuration parameters, or version info to image files.  
- **Lightweight data transport:** Send both visual and numerical information in a single portable PNG file.  
- **Hidden annotations:** Store notes or instructions inside an image without affecting its appearance.  
- **Scientific experiments:** Bundle experiment setup, raw data, and results visualization into a single file for easier sharing.  
- **Quality control:** Save inspection images together with measurement logs for traceability in manufacturing.  
- **Field work:** Collect photos with embedded sensor readings (temperature, GPS, etc.) for later analysis.  
- **Archiving:** Preserve both visual documentation and related datasets in one file for long-term storage.  
- **Secure communication:** Share images with embedded technical or proprietary information without altering appearance.

## Features

- Embed and extract arbitrary files in PNG images  
- Password-protected payloads using **7-Zip**  
- Native LabVIEW implementation (no external toolkits required)  
- Simple GUI for external file embedding  
- Lightweight and portable

## Requirements

- **LabVIEW 2020 or newer**  
- **7zr.exe** (included in [7-Zip](https://www.7-zip.org/) distributions)  

## Included VIs

- **Encode VI** – Appends data to a PNG file or optionally exports it as XML.  
- **Decode VI** – Reads back the data from a PNG file, including XML if used.

- `PP.PNG.File.Encode.vi` – Embed external files into PNG  
- `PP.PNG.File.Decode.vi` – Extract files from PNG  

## Key Features

- Preserve image appearance while storing hidden data.  
- Optional XML export for structured data.  
- Combine images and related data in a single portable file.  
- Store hidden notes or annotations without affecting the image appearance.

## Changelog
## Version 1.1.1
- Refactored **Decode VI**: replaced temporary PNG file creation with direct bytestream-to-image conversion.  
  - This improves performance and removes the need for intermediate files.  
-  Note: No build is provided for this version, since the built executable cannot return the image data.  
## Version 1.1.0
- **Removed MGI dependencies**  
  Replaced with custom search methods → faster and no external toolkit needed.
  
- **Simplified encryption**  
  Removed LabVIEW Flatten and XML Flatten RC4 encryption.  
  Now only **byte negation** is applied.

- **New external file embedding/extraction**  
  - `PP.PNG.File.Encode.vi`  
  - `PP.PNG.File.Decode.vi`  
  Uses `7zr.exe`, password required.

- **Password-protected payload handling**  
  - `Write.Encrypted.7zPayload.vi`  
  - `Read.Decrypt.7zPayload.vi`

- **New GUI**  
  Added for external file embedding, usable in both LabVIEW IDE and built applications.


## Usage

![Usage](https://github.com/iattila/pixpack/blob/main/src/pixpack/example/Example_1_Snippet.png)

1. Provide the PNG file path.  
2. Specify the output file path (or overwrite the original).  
3. Supply the data to encode.  
4. Decode VI can retrieve the embedded data.

## License

This project is released under the **BSD 3-Clause License**.  

The included hex encode/decode functions are derived from the MGI Utilities (also BSD 3-Clause).  

---

### BSD 3-Clause License

Copyright (c) 2025, BitPack Tools  
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice,
   this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in the
   documentation and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its
   contributors may be used to endorse or promote products derived from
   this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

### 7-Zip License Notice
PixPack uses `7zr.exe` from the **7-Zip project**.  
7-Zip is licensed under the **GNU LGPL** with unRAR restrictions.  
For more information, see the official [7-Zip License page](https://www.7-zip.org/license.txt).



