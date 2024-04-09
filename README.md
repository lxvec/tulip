# tulip - a widget with thematic scenery to cheer you up throughout the day

## What

1. I was creating a new wallpaper on my iPad and went to set a dynamic wallpaper. I found they were boring, for something to be dynamic I expected more than a basic repetetive animation. I thought about the [iGoogle Tea House theme](https://wp.jiinjoo.com/?p=481) that existed back in the late 00s and how much joy it brought me to log on to google and see the zen fox doing a new activity I hadn't seen before. It's a shame these cute temporal themes haven't caught on. They're lightweight, not much more difficult that uploading a static image.

2. Wallpapers are cute, but widgets are cuter and customizable in size and position. Widgets have been available on android devices since 2008 and Apple was painstakingly slow to follow suit. We finally got widgets on ios14 in 2020 and they have improved since then, with more apps developping widget components for their users home screens.

With the above in mind, my current POC is to build an application where you can create a widget, select a theme, position it onto your lock or home screen and then have a cute penpal that goes about his life, just like you. The widget should not always shuffle through the same images, this would get boring once we've seen the penpal iterate through all it's activites at least once. It should be possible for the developer to push a new photo for a specified time slot. This way, we can have easter eggs for special events and holidays. Maybe even a birthday easter egg.

## Why

It's cute. It's like a tamagotchi for iphone but you don't need to worry about killing it because it lives in it's own universe. With the rise of lock and home screen customizations on Apple devices, users making their apps aesthetically pleasing, I think a natural next step is to give users something dynamic. Right now, we can make our screens as pretty as we want, they are still quite static. 

## When

I'm a java, python and ex Javascript/PHP developer. As of this moment, I don't know how to develop for Apple products which I imagine to be a massive headache. This project will be slow, slow, slow. :) 

## How to

For the time being, I wante to enjoy a dynamic wallpaper, share it with friends and have control over disting new images at any time without my friends needing to pull new 'updates'.

Here are the steps:

1. Download all the theme images onto Photos app
2. There are 12 photos, adjust the time to the respective time you want that photo to be set as the wallpaper. For example if you want a photo to be your wallpaper at 5am, set the time this photo was taken to 5am. This is an important step that needs to be done before adding the photos since you can't change metadata from within a shared album.
3. Once this is done for all 12 photos, add them all to a new Shared Album. This preserves the metadata you just created. Share this shared album with your friends who want to have this wallpaper too. 
5. Create the following shortcut in Shortcuts app. Here is a screenshot with details. Again, share this shortcut with any of your friends.
6. Create 12 automations for each time you want to transition the wallpaper background. Select the shortcut created in step 5 for each automation. The shortcut takes the current time in which it is executed, so if it automation executes the shortcut at 5am, it will retrieve the image with metadata at 5am. This is the only step that needs to be manually done on each device as automations cannot be shared between people.
7. Enjoy your dynamic wallpaper :-)

To make changes to the images:
1. The shared album as 12 images, one for each time. If you want your wallpaper to do something different than usual at 5am, delete the 5am photo from the shared album and reupload a new one with the 5am metadata. The automation and shortcut is not aware of the contents of the shared album, it just runs at time X, picks out the photo that was taken at time X from the shared album and sets it as the wallpaper.
