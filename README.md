# 🎲 digital-frame game plan:
> 1. take an old iPad
> 2. make it continously display your own website
> 3. put it on the wall
> 4. enjoy the pictures e-mailed by your loved ones scrolling by    

## STEP 1. 📧 e-mail server setup
> the ability to recieve pictures

requirements: 
 - secure auth
 - filtering e-mail for
   - sender (only for spam filtering for now)
   - having attachment
 - ability to extract the attachement

todos:
 - [ ] try existing e-mail services with `api`-s, such as `Gmail API` & `Outlook` if their sulition works for this. I feel it should.
 - [ ] if existing e-mail services will not work for this usecase, investigate hosting an e-mail sever using `Postfix`, `Dovecot`, `Exim` or other.

## STEP 2. 📎 attachment processing and storage
> the ability to handle images

requirements:
 - export images to the web-server
 - secure storage of images on the server
 - handling unfit images
   - too large   --> size can be ignored for now
   - extentions  --> unsopported file extentions can be ignored for now

todos:
 - [ ] how to securely upload images online?
   - [ ] does the host (leaning towards [Notlify](https://www.netlify.com/) atm) support secure image storage?
   - [ ] alternative solutions include: AWS, Google Cloud, Azure Blob

## STEP 3 🖼️ display application
> the ability to view the images

requirements:
 - securely display images in a series 

nice to haves:
 - randomization of next image, possibly with extra weight on recently added ones
 - costumazion of scroll speed
 - night mode
 - notificaiton of new images
 - manually step to next / previous images, preferalbly in a touch-screen-first approach
 - GUI management of the image libtrary (possibly on a per-image basis first)

todo:
 - [ ] build an applicaion that displays images
 - [ ] add auth

## STEP 4 🛳️ deploy application
> the ability to use the digital frame

requirements:
 - deploy this code
 - have storage for the pictures
 - have integration with the selected e-mail solution

again, the best platform might be [Notlify](https://www.netlify.com/)
