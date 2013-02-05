*************************
README get_data.py
*************************



*************************
README get_data_dir.py
*************************

To download files from ADCS document repository, simply run the following command line in your terminal:

  python get_data_dir.py

To get help, run this command line:
	
	python get_data_dir.py -h
	or
	python get_data_dir.py --help


Configuration
------------------------------
You have two ways to define which directory to grab the files from, and where to save the files to:

	1: via command line arguments [see section "Command Line Arguments" for more details]
	2: in a conf.json file [see section "CONF FILE" for moredetails]

Note: the specs defined via the command line arguments always have the higher precedents than the conf.json file.  

Things you can specify in both conf.json file and via the command line:

	- username: your adcs edc portal login name
	- password: your adcs edc portal password
	- source url: where to grab the files from ADCS Document Repository. e.g. https://adcs-adni.iadcs.ucsd.edu/docs/data1
	- target directory: where to store the files to on your machine/server
	- recursive: by default this feature is turned off; if specified, files under all subdirectories will also be saved
	
Things you can only specify via the command line:

	-h or --help: brings up this README page
	-v or --verbose: additional processing messages


Command Line Arguments
------------------------------
-u or --username
-p or --password
-s or --sourceurl
-t or --targetdir
-r or --recursive
-v or --verbose
-h or --help

Example:
	python get_data_dir.py -s https://adcs-adni.iadcs.ucsd.edu/docs/data1 -v -r


CONF FILE
------------------------------
File name: conf.json
Location: always under the same directory with get_data_dir.py
	e.g. if get_data_dir.py is located under /Users/xxx/Desktop/data_folder, 
	then the conf.json has to be located under /Users/xxx/Desktop/data_folder

Note: if you are planning to define all the specs using command line arguments, you don't need to create a conf.json file

JSON keywords:
	username
	password
	source_url
	target_directory
	recursive
	
Example:
{
	"username": "userx",
	"password": "ppp",
	"source_url":"https://adcs-adni.iadcs.ucsd.edu/docs/data1",
	"target_directory":"/Users/xxx/Desktop/data_folder",
	"recursive":1        
}

