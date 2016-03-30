# Transmorgify
## Please Note : Currently in development, not working as it should.

## Purpose
The purpose of transmorgify is to accept a file, then transform it into a
different type. This includes altering the file identifier in the hex (magic numbers)
as well as changing the extension of the file to match the magic number.

## What's Included

##### file_sig_util.py
This is where the magic happens. This script appends a new file signature via hex to a specified file, alters the extension to match, then saves it.

##### hex_util.py
This is a custom script I use for any project that requires some interaction with hex code. It's links directly to the python <code>binascii</code> library. It provides a more intutive and streamlined workflow for working with hex.


## What's Required

You need only this folder of scripts, and a version of Python 3. Code is able to run wherever python can be installed.


## Commands

##### Single File
If you only want to change one single file.

- Layout:<br>
<code>
python transmorg.py [filename] [newfiletype]
</code><br>

- Example<br>
<code>
python transmorg.py example.png jpg
</code><br>

##### All Files in a Folder
A command for recursively changing all files in a folder looks like this.

- Layout<br>
<code>
python transmorg.py [folder] [newfiletype]
</code>

- Example<br>
<code>
python transmorg.py pictures jpg
</code>

##### Filtering

If you want to choose what types of files are changed when you point to a folder you use can use the filter argument.

- Layout<br>
<code>
python transmorg.py [folder] [newfiletype] [filter]
</code>

- Example<br>
<code>
python transmorg.py pictures jpg png
</code>

  The above code will transform every file in that folder that is a .png to a .jpg
