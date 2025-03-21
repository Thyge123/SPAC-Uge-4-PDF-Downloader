# PDF-Downloader

A Python utility to download PDF reports, track download status, and upload files to Google Drive.

## Features

- Downloads PDF files from URLs listed in Excel spreadsheets
- Uses multithreading for efficient parallel downloads
- Tracks download status and maintains metadata
- Creates detailed reports of download success/failure
- Automatically uploads downloaded PDFs to Google Drive
- Maintains backward compatibility with existing files

## Requirements

- Python 3.6+
- Required packages:
  - pandas
  - requests
  - pydrive2
  - openpyxl (for Excel file support)

## Setup

1. Clone this repository
2. Install dependencies: `pip install pandas requests pydrive2 openpyxl`
3. Download OAuth credentials from Google Cloud Console and save as `client_secrets.json` in the project directory
4. Prepare your Excel file with report URLs in the expected format (with 'BRnum', 'Pdf_URL', and 'Report Html Address' columns)

## Usage

Simply run the script:
```bash
   python PDF-Downloader.py
```

The program will:
1. Read report URLs from Excel
2. Download PDFs that haven't been downloaded before
3. Create a report of download status
4. Update metadata
5. Upload downloaded PDFs to Google Drive

## Directory Structure

- `Data/` - Main data directory
  - `Downloads/` - Downloaded PDF files
  - `Output/` - Reports and logs
- `client_secrets.json` - Google API credentials
- `credentials.json` - Saved Google authentication tokens