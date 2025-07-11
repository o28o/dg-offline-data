
Instructions for local installation of displays for shs dictionary.

 1.  Go to https://www.sanskrit-lexicon.uni-koeln.de/scans/SHSScan/2020/web/webtc/download.html
       and download shsweb1.zip.
 1a. unzip shsweb1.zip. You need the  'web' folder,  which contains fonts, images, etc. 

 2. Prepare a 'php server' on your computer.
   There are various ways to do this.
   If you you have this already on your computer, you can skip the following.
   For Windows OS,  we recommend installing 'xampp for windows'.
   There is also 'xampp for Linux' and 'xampp for OSX Macintosh'.
   See https://www.apachefriends.org/index.html for download instructions.
   Note: The current displays use only the Apache Server and PHP features
   of xampp. In particular, MySQL, FileZilla, Mercury and Tomcat are not used.

 3. Find the 'home' folder for your server.
   A common location on Windows 10 installation of xampp is 'C:\xampp\htdocs'
   The following instructions use HOME to refer to this directory.
   Create a folder named 'cologne' under HOME.
   Then create a folder named 'shs' under 'cologne'.
   Finally move the 'web' folder of step 1 into 'shs' folder.
   So we now have, in Windows xampp installation, 
     C:\xampp\htdocs\cologne\shs\web
    This completes the installation.
 4. Be sure your server is 'started. The details depend on the server.
    For xampp on Windows 10, type 'xampp' in the 'Type here to search'
    input field at lower left of the Windows desktop. This brings up the
    xampp Control Panel.
    Click the Action 'Start' beside for 'Apache' Module.
 5. Try out your displays. Open your browser, and enter url:
     http://localhost/cologne/shs/web/
     You should see a list of 'Available displays'  (Basic display, etc.)
     for dictionary shs.
     Choose a display and then try a search.

Good luck!

NOTES:
1. For Linux and Macintosh computers, you may need to change permissions
   on the 'cologne directory.  You can do this in a command terminal:
    cd HOME
    chmod -R 755 cologne
2. The above installation of xampp on Windows has been tested for 
   PHP version 7.1.9 and PHP version 8.0.0.


INSTALLATION OF LOCAL SCANNED IMAGES (Optional)

For the displays above, clicking on a link to a page of the scanned
images retrieves the image file from the Cologne server.  However,
you may also install the scanned images locally.


1.  get a copy of the scanned images for shs
 1a.  make a directory named 'scans' as a child of the 'cologne' directory
 1b. cd into cologne/scans
 1c. git clone https://github.com/sanskrit-lexicon-scans/shs.git
     This will download a directory called 'shs' into cologne/scans folder.
     PDFs for individual pages are in the subfolder named 
     'cologne/scans/shs/pdfpages'
     Note: If you don't have git on your computer, you could go to the
      https://github.com/sanskrit-lexicon-scans/shs
      click the 'Code' button, and then 'Download ZIP'

2.  Access a particular page (say page 123) via the browser with this url:
    http://localhost/cologne/shs/web/webtc/servepdf.php?page=123
3.  Also, in your shs displays,  clicking on a page link should now
    show an image from the local installation.

