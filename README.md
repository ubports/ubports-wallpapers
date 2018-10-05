# UBports Wallpapers

This repository contains wallpapers gathered from our community for inclusion into Ubuntu Touch. All of the wallpapers are licensed at least as permissively as CC-BY-SA 3.0, but check out [debian/copyright](debian/copyright) for full copyright information.

## How is this package released?

The package `ubports-wallpapers` is made by this source. `ubports-wallpapers` is made to depend on other `ubports-wallpapers-[date]` packages. For example, for the OTA-5 cycle and beyond (until we have enough wallpapers to warrant another package), `ubports-wallpapers` will depend on `ubports-wallpapers-2018-10`. Once we have enough wallpapers to create a new wallpaper pack, we'll do the following:

1. Create a new folder in the root of this repository with the year and month the folder is created in (`2019-02`, for example).
1. Add the new images to the new folder.
1. Add the copyright of the new images to [debian/copyright](debian/copyright).
1. Create `debian/ubports-wallpapers-2019-02.install` (for example) which installs all of the files from the new folder into `/usr/share/backgrounds`.
1. Add the new package (`ubports-wallpapers-2019-02`, for example) to [debian/control](debian/control),
1. Change `ubports-wallpapers` to depend on the new package in [debian/control](debian/control).
1. Add the old package (`ubports-wallpapers-2018-10`, for example) to the suggested packages for `ubports-wallpapers`.

## Can I use my own wallpapers in Ubuntu Touch?

Yes! Go to Settings > Background, scroll down to Custom, and tap "Add an image..." to select your image.

## How can I submit more wallpapers?

Email us at `contribute at ubports dot com` with your wallpaper submission or submit an issue on this repository. Please include the license which you are sharing the image under (including a link to the license text) in your e-mail. We will upload the image to [our Pending Wallpaper Submissions folder](https://nc.ubports.com/s/oiAHpNGMyryCbXe) along with your name or pseudonym. If you prefer to remain anonymous or pseudonymous, please state that in your submission.

Once we have enough submissions and enough time has passed since the last wallpaper release (4-6 months), we'll make a poll for our community asking which wallpapers they would like to see included in the next update of Ubuntu Touch. Please note that while this poll will be public, the UBports contributors reserve the final say in whether a submission is included or not. We don't expect to use this reservation, but we want to be clear that we make it.

### Submission rules

These rules ensure that submissions are equally usable and shareable by all users of Ubuntu Touch.

We will only accept wallpapers where you, the submitter, are the copyright holder for the image.

Submissions should have at least 4096 pixels in each direction. If that is not possible, at least 1920 pixels in each direction is required. This ensures that your submission will display at full resolution on a majority of Ubuntu Touch devices whether used in landscape or portrait orientation.

Submissions may be `png` or `jpg` images, but please note that they may be recompressed before they are included in a wallpaper package.

Files must be licensed under the Creative Commons-Attribution-ShareAlike 3.0 (CC-BY-SA 3.0) license. A newer version of the CC-BY-SA (such as CC-BY-SA 4.0) license may be used. A more permissive license than CC-BY-SA 3.0 (such as CC0 or CC-BY-4.0) may be used. A less permissive license may not be used.

Do not accent the location of the Ubuntu Touch InfoGraphic (the circle on the lock screen) in your submission. the InfoGraphic's position changes depending on the orientation and physical size of the device screen.

All submissions must follow the [Ubuntu Code of Conduct 2.0](https://www.ubuntu.com/community/code-of-conduct). Additionally, images must not contain any adult or questionable content. Basically, if you would not expect a parent to set your submission on their young child's device, do not submit it.

## Will users who have set a wallpaper lose it if you remove it?

No. Unity8 and System-Settings copy the wallpaper into the user's home folder when it is set. When a wallpaper is removed from the image, it will be shown in the "Custom" section of the Background settings in Ubuntu Touch.

## What the heck is warty-ubuntu-final.png?

In short, `warty-ubuntu-final.png` is a bit of a kludge until we have a better solution.

Due to historical reasons, Ubuntu has included `warty-ubuntu-final.png` in every Ubuntu release since the first, 4.10 in 2004. This allows them to replace the default wallpaper in every release and have the people using that wallpaper see the new one when they upgrade. The Unity System Compositor, unity8, and System Settings all have a path to `warty-ubuntu-final.png` hard-coded into them as the default wallpaper for the system.
