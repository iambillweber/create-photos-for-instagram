# Create Photos for Instagram

This Mac workflow will resize images to a width of 1080px and then add them to your Photo Library. It uses a slightly modified Applescript shared by [Craig Smith](https://stackoverflow.com/users/4898303/craig-smith) on [Stack Overflow](https://stackoverflow.com/questions/30913245/resize-images-to-specific-width-only-applescript-or-automator).

## How Does This Work

The workflow accepts image files for input. 

1. It takes those image files and copies them to a folder on the Desktop it creates called Instagram.
2. It will then look for the string "FS" in the images' filenames. 
	- If it finds "FS", it will change it to "IG". Otherwise, the file will retain its name.
3. It then uses [Sips](https://www.unix.com/man-page/osx/1/sips/) to resize the images to 1080px while maintaing the images' proportions.
4. It will then add the images to your Photo Library (Photos.app).

### Note

You may wish to disable or alter Steps 2 and 4 depending on your workflow.

# How To Use This
 
1. Open the .workflow file in Automator.
2. Save it as a service ~/Library/Services
3. In Finder, highlight the photos you wish to resize.
4. Right-click on one of the photos and in the menu, go to Services, then Create Photos for IG v2.
