# YouTube Archiver (PowerShell)

This PowerShell script automates downloading videos from specified YouTube channels while tracking previously downloaded videos using an archive file. It efficiently manages downloads by avoiding duplicates through archive checks.

### Features
- **Prefix-aware Archive Loading:** Loads video IDs from an archive file, stripping any prefixes for accurate matching.
- **Channel Management:** Reads YouTube channel URLs from a file and processes each channel individually.
- **Directory Structure:** Creates directories per channel to organize downloaded videos.
- **Video Filtering:** Skips videos already listed in the archive to prevent re-downloads.
- **Metadata Handling:** Downloads video metadata including descriptions, thumbnails, and subtitles along with videos.
- **Error Handling:** Ignores errors during downloads to allow continuous script execution.

### Usage

#### Prepare Files
- Create a `channels.txt` file listing the YouTube channel URLs you want to download from.
- Ensure an archive file named `downloaded_archive.txt` exists to track downloaded videos.
- (Optional) Provide a `cookies.txt` file if authentication is required for any channels.

#### Run the Script
- Execute the PowerShell script in Windows PowerShell.

#### Output
- Videos will be saved inside a `yt-dlp` directory, organized by channel name.

### Requirements
- Install [yt-dlp](https://github.com/yt-dlp/yt-dlp)  
  You will need Python installed. You can install yt-dlp using:  
  ```powershell
  pip install yt-dlp
  ```
  or download the standalone binary for your platform.

### Notes
- The script displays progress and summary in the console, including numbers of videos found, skipped, and downloaded per channel.
- At the end, the script prompts to exit.