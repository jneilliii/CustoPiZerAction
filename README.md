# 🤖 CustoPiZerAction

Thsi is just a simple example of using [CustoPiZer](https://github.com/OctoPrint/CustoPiZer) to create a custom OctoPi image using a manual build action. Base image input is a URL to a downloadable zip file that contains an img file inside. 

## How does this work?

A simple update script is run via [CustoPiZer](https://github.com/OctoPrint/CustoPiZer) action.
All that is done is running the equivalent of `sudo apt update && sudo apt upgrade` from the single file stored in the scripts folder. The resultant output.img file will be zipped, and then attached as an artifact to the action run. Due to the way GitHub Actions handle artifacts the file will be double zipped on download.  