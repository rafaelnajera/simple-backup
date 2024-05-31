# simple-backup
A no-fuss, practical tool to back up files from one folder to another.

Usage:
```
simple-backup [--options] folder1-src folder1-dest [folder2-src folder2-dest...]

--ignore-mac-stuff:  ignores .DS_Store and .Trash
--ignore some_file_or_folder_name: ignores the given sub-folder or file

--silent: only major errors will cause output
--no-fancy-output: no fancy terminal animations
```

For every folder source/destination pair, the tool synchronizes the files in the
source to the files in the destination. The tool creates first a list of source files
with the current source folder files removing all ignored files and folders. 

Updated and new files in this list are copied to the destination folder and 
files in the destination not present in the list are deleted. 

