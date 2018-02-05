
# TEAM SPECIFICS

## About team contributions

* 	Please, add yourself as a contributor to the repo by going to **Settings->collaborators** ( using the team account ). Add your personal github account so that we can know who made which changes.Commits should be done using your own account, not this one.

*	For your own contributions, feel free to push your changes to the contrib/{youraccount} folder. If there is no folder yet, just create one and add all your code there. As we are working with different tools and with different OSs, our raw contributions are not mergeable. If we end up using a shared api, all the changes related to that common api will be sent to the [**api** ](./api) folder.

*	The [**res**](./res) folder will have all the file assets we will be working with, like images, txt files, useful links, pdfs, etc. . Please, don't try to commit video files, as most of them are really big. Instead, try updating the appropiate scripts to get the files from dropbox, e.g. the [**get_calibration_files.sh**](./res/get_calibration_files.sh) file.

```sh
#!/bin/bash

echo "GETTING CALIBRATION FILES FROM DROPBOX"

FILES=( "https://www.dropbox.com/s/yjip8kscakq257l/calibration_mslifecam.avi"  
		"https://www.dropbox.com/s/so7qjmpusrpmurr/calibration_ps3eyecam.avi" )

## get the files from dropbox
for _file in "${FILES[@]}"
do

	echo "downloading: ${_file}"
	wget "${_file}"

done


echo "DONE"

```

	In the email sent to the members, you should have received the related dropbox account. Just add your videos there and make a link to share the file. Then add this link to the **FILES** array in the script file.

*	Also, please update the .gitignore files according to the files you are working with and are not supposed to be commited ( like .project files from some IDEs, or other file formats for videos, etc. ).