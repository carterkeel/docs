# 📷 ExifTool Commands Cheat Sheet

## 📄 Basic Info

`exiftool <file>             # View all metadata  exiftool *.jpg              # View metadata for all JPGs in folder`  

## 📝 Writing Metadata

`exiftool -Artist="Your Name" <file>   exiftool -Copyright="(c) 2025 You" <file>   exiftool -Title="My Photo" <file>`  

## 🗃️ Batch Processing

`exiftool -Title="My Photo" *.jpg   exiftool -overwrite_original -Author="Your Name" *.jpg`  

## 🕒 Date & Time

`exiftool -DateTimeOriginal="2025:01:01 12:00:00" <file>   exiftool "-DateTimeOriginal+=0:0:0 1:30:0" <file>`  

## 📤 Export & Save Metadata

`exiftool -j <file> > metadata.json   exiftool -xml <file> > metadata.xml`  

## 📥 Import Metadata

`exiftool -TagsFromFile source.jpg target.jpg`  

## 🧹 Removing Metadata

`exiftool -all= <file>   exiftool -overwrite_original -all= <file>`  

## 🎯 Specific Tags

`exiftool -Model -FocalLength <file>   exiftool -gps:all <file>`  

## 🧭 GPS & Location

`exiftool -GPSLatitude="40.7484" -GPSLatitudeRef=N -GPSLongitude="73.9857" -GPSLongitudeRef=W <file>`  

## 🗂 Rename Files Using Metadata

`exiftool '-FileName<CreateDate' -d %Y%m%d_%H%M%S.jpg <file>`  

## 📦 Misc

`exiftool -list                   # List all tags  exiftool -listw                 # List writable tags  exiftool -h <file>              # HTML output`  

> ✅ Always use `-overwrite_original` to avoid creating backup files (`_original`).