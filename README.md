# cPanel-yml

File for cPanel git deployment

Please remove all # Comments or the file will not work

## Instructions

1.Place the file in the root of your project  
2.The file must be in the repo before you clone it with cPanel  
3.Be sure to edit the file to leave only the lines you need and don't leave all the commands active  
4.There must be no unmerged pull requests or the deploy button will be deactivated  
5.There must be no errors in the file or the deploy button will be deactivated.

````
---
deployment:
     tasks:
       - export DEPLOYPATH=/home/<username>/public_html  # Add /<app_folder> if required
       - /bin/cp <file_name> $DEPLOYPATH                 #Copy specific file to destination from root
       - /bin/cp /<sub_folder>/<file_name> $DEPLOYPATH   #copy specific file from source sub folder
       - /bin cp * $DEPLOYPATH                           #copy all from root
       - /bin cp /<sub_folder>/* $DEPLOYPATH             #copy all from sub folder root
       - /bin/cp -r * $DEPLOYPATH                        #copy all recursively to $DEPLOYPATH```
````
