# PixPack

![PicPack Logo](https://github.com/iattila/pixpack/blob/main/PicPack%20Logo.png)

# PNG Data Embed/Extract Tool (LabVIEW)

This repository contains a LabVIEW tool for embedding and extracting custom data in PNG files.

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


