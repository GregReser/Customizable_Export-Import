# Metadata Export-Import Plugin for Adobe Bridge
Javascript plugin for Adobe Bridge CS5 and higher that allows the user to export and import embedded XMP metadata from media files.

Supported file types: ai, avi, bmp, dng, flv, gif, indd, indt, jpg, mp2, mp3, mp4, mov, pdf, png, psd, swf, tiff, wav, wma, wmv

This plugin is written in Adobe ScriptUI and utilizes the Adobe Bridge JavaScript object model

## Main features
 - Export-import from select file(s) or from an entire folder (with option to include all subfolders)
 - Export-import metadata in tab-delimited text files
 - User can define which feilds to export-import.
   - Estabished schemas (IPTC, Dublin Core, VRA) are available to build a custom field list.
   - Field name for export-import can be changed (allows synchronization with local field names)
   - Custom schemas and namespaces can be used


Backup your files first	
IT IS HIGHLY RECOMMENDED THAT YOU BACKUP YOUR IMAGE FILES BEFORE USING THIS OR ANY XMP INFO PANEL INFO PANEL.	
THERE ARE NO WARRANTIES FOR LOSS OR UNINTENDED MODIFICATION OF DATA.*	

## Installation
 1. Start Adobe Bridge
 2. Go to Bridge Preferences
 
    Windows
      - Go to Edit --> Preferences --> Startup Scripts
    
    Mac:
      - Go to Adobe Bridge --> Preferences --> Startup Scripts
 3. Click "Reveal My Startup Scripts".  This will open the correct folder
 4. In this folder, copy the the downloaded file "user_customizable_export_import.jsx"
 5. Close the folder
 6. Quit Bridge
 7. Start Bridge
 8. When prompted, confirm the installation of "user_customizable_export_import"

## Open the plugin in Adobe Bridge
<<<<<<< HEAD
  1. Locate the menu "Custom Metadata at the top of the Bridge window (to the right of "Help")
  2. Click "Metadata Export-Import" on the dropdown
	
=======
  1. Locate the menu "VRA Core Metadata at the top of the Bridge window (to the right of "Help")
  2. Click "Metadata Export-Import" on the dropdown
	
## Export Instructions
From selected files only 
  1. Select file(s) in Adobe Bridge
  2. Under ‘Images’, choose 'Selected thumbnails in Bridge'
  3. Select desired export options (see below) 
  4. Click ‘Export’ 
  5. Choose name and location for your export file (.txt format)
  6. Save
			
From all image files in a folder
  1. Select 'Entire folder'
  2. Use ‘browse’  to select folder you wish to use
  3. If you want to export images in all subfolders check the box 'include subfolders'
  4. Select desired export options (see below) 
  5. Click 'Export’
  6. Choose name and location for your export file (.txt format)
  7. Save

After export is complete
  1. Open your .txt file in a spreadsheet using tab delimiters and UTF-8 character encoding.
  2. Under "File" menu
    i. Select file and click "Open"
    ii. Confirm settings:
      a)  Tab-delimited (Excel) (*.txt) if you will be using Excel
          Tab-delimited (Not Excel) (*.csv) if you will be using OpenOffice or LibreOffice
      b) Delimited/Separated by = Tab
    iii. Click "OK"
  3. The first row will contain the field names

### Export Options 
Option 1:  prepend Image dates with '_'

   * This is useful if you will be importing the metadata to Excel.
   * XMP Date values must use the YYYY/MM/DD format.  Adding a '_' character at the beginning of the Date will prevent Excel from automatically changing it to a format XMP cannot understand. (if your system is set up for another format, that will be reflected in the way Excel displays dates). 
   * The '_' character will be removed when you import the data back into the image file(s).

Option 2:  Remove line breaks	  
   * This is useful if you will be importing the metadata to Excel.
   * When selected, line breaks (line feed and carriage return) will be replaced by a semi-colon and a space ('; ').
   * When not selected, line breaks will be retained but converted to plain text place holders ('LF'), ('CR') so that they are not changed by Excel.  When the data is imported back to an image, the codes will be changed to the proper XMP encoding.

## Import Instructions
This script imports data from a tab delimited text file into image files with matching filenames.
If you have already exported metadata and edited it in Excel and want to import it back in:
  1. Select the folder containing the target images
    a. If you have nested folders, check 'include subfolders'
  2. Select the text file to be imported
     a. Click 'Import' and cross your fingers
  If you are starting with external metadata (from a database, etc.)
  1. First, you need a properly formatted template. Click the help (?) button on the panel under ‘Import’. 
    This template lists all available IPTC fields and you can import data  into any IPTC field. 

Look for this new file on your desktop
  1. Open the text file in Excel
  2. Add data to the appropriate columns
  3. Save as a tab-delimited text file

To import data into image files:
  1. Select the folder containing the target images
  2. If you have nested folders, check 'include subfolders'
  3. Select the text file to be imported
  4. Click 'Import' and cross your fingers

Import Options 
Option 1: Ignore file extensions
  When selected, metadata will be imported to all matching media with matching file names regardless of the file extension.
  This allows you to import matching metadata to all versions of the same media file, e.g., .tif, .jpg. .png.

Option 2: Create Title (IPTC Core)
  When selected, the Headline will be filled with the data values from:
  VRA Work Title, VRA Image Title

Option 3: Create Description/Caption (IPTC)
  When selected, the Description/Caption (dc:description) will be filled with the data values:
  Work Agent; VRA Work Title;_iTitle; VRA Work Date; VRA Work Type; VRA Work Material; VRA Work Measurements; VRA Work Location; VRA Work Id; VRA Work Rights

Option 4: Create Keywords (IPTC)
  When selected, Keywords (dc:subject) will be filled with the data values from VRA Work fields:
  VRA Work WorkType; VRA Work Technique; VRA Work Style/Period; VRA Work Culture; VRA Work Subject

Option 5: Set Thumbnail Label
  When selected, each image that has metadata successfully imported will have its label set to:
  'VRA metadata imported' and the label color will be changed to white.
  Warning: Existing labels will be lost
>>>>>>> eea2312f69a1c5ac2771fa329322bf7a9ba1bd2d

/////////////////////////////////////////
// Terms and Conditions //
/////////////////////////////////////////

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details. http://www.gnu.org/licenses/

Disclaimer of Warranty
"THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW. EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES PROVIDE THE PROGRAM “AS IS” WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION."

Limitation of Liability
"IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MODIFIES AND/OR CONVEYS THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES."