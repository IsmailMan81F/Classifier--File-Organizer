
# Classifier
Organize files in your current directory, by classifying them into folders of music, pdfs, images, etc.

## Installation
```sh
$ pip install classifier
```
#### Compatibility
* Python 2.7 / Python 3.4
* Linux / OSX / Windows


## Usage
* Go to your directory, where you want to classify your files.
* Run the following command in your terminal.
```sh
$ classifier
```
```sh
>> Scanning Files
>> Done!
```

## Example
### Before:
```
Downloads
│   ├── project.docx
│   ├── 21 Guns.mp3
│   ├── Sultans of Swing.mp3
│   ├── report.pdf
│   ├── charts.pdf
│   ├── VacationPic.png
│   ├── CKEditor.zip
│   ├── Cats.jpg
│   └── archive.7z
```

### After:
```
Downloads
│   ├── Music
│   │   ├── 21 Guns.mp3
│   │   └── Sultans of Swing.mp3
|   |
│   ├── Documents
│   │   ├── project.docx
│   │   ├── report.pdf
│   │   └── charts.pdf
|   |
│   ├── Archives
│   │   ├── CKEditor.zip
│   │   └── archive.7z
|   |
│   ├── Pictures
│   │   ├── VacationPic.png
│   │   └── Cats.jpg
```


## Options
`classifier [-dt] [-st SPECIFIC_TYPES [SPECIFIC_TYPES ...]] [-sf SPECIFIC_FOLDER] [-o OUTPUT]`

optional arguments:

	-h --help				show help message and exit
	
	-dt --date				Classify the files by their Creation Date
	-st --specific-types			Move the specific file extensions into the Specific Folder
	-sf --specific-folder			Folder to move files with Specific Type
	
	-d --directory				The directory whose files you want to classify
	-o --output				Main directory to put organized folders
	
	-v --version         			show version
	-t --types           			Show the current list of types and formats
	-et --edittypes      			Edit the list of types and formats (edit the CONFIG)
	
	-rst					Reset the CONFIG file


### Example
###### Classify specific file types
`classifier -st py pyc -sf "Python Files"`

### Before
```
Workspace
│   ├── views.py
│   ├── temp.pyc
│   ├── game.java
│   ├── index.html
│   └── script.py
```


### After
```
Workspace
│   ├── Python Files
│   │   ├── views.py
│   │   ├── temp.pyc
|   |	└── script.py
|   |
|   ├── game.java
|   └── index.html

```

### Example
###### Classify by Date:
`classifier -dt`

### Example
###### Classify files of directory '/home/source' and put them in location '/home/dest':
`classifier -d /home/source -o /home/dest`

`Note: ` If -d (source directory) is given without -o (output) directory, this will classify the files of source directory Eg:<br>
`classifier -d /home/source'`<br>
This classifies the directory /home/source.



### View the CONFIG, how files will be sorted
`classifier -t`

### Edit the CONFIG, to set up manual settings for classification
`classifier -et`

### Reset the CONFIG file
`classifier -rst`
```

```

