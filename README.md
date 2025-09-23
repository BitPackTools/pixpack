# PixPack

![PicPack Logo](https://github.com/iattila/pixpack/blob/main/PicPack%20Logo.png)

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

## Included VIs

- **Encode VI** – Appends data to a PNG file or optionally exports it as XML.  
- **Decode VI** – Reads back the data from a PNG file, including XML if used.

## Key Features

- Preserve image appearance while storing hidden data.  
- Optional XML export for structured data.  
- Combine images and related data in a single portable file.  
- Store hidden notes or annotations without affecting the image appearance.

## Dependencies

This tool uses two VIs from the **MGI Library** (BSD 3-Clause License).  
For simplicity and to avoid external dependencies, these VIs have been extracted from the MGI library and included directly in this repository.

## Usage

1. Provide the PNG file path.  
2. Specify the output file path (or overwrite the original).  
3. Supply the data to encode.  
4. Decode VI can retrieve the embedded data.


