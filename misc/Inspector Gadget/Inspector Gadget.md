# Inspector Gadget

Opening the file reveals some random numbers in cells. Zooming out reveals a QR code albeit stretched. Using an online tool such as [Pixilart](https://www.pixilart.com/draw), recreate the QR code.

![QR Code](https://github.com/N-2-O/MACS-CTFd/blob/main/misc/Inspector%20Gadget/inspector_gadget.png?raw=true)

The QR code will take you to [https://robf101.bitbucket.io/mypage1.html](https://robf101.bitbucket.io/mypage1.html). Inspecting the page source, there is a comment `Hehe, you're on the right track :)`, so the clue is somewhere in the source code. Viewing the source code, notice that there are 4 images in the list for the slideshow, but only 3 show up when viewing the slideshow. Viewing each of the 4 images individually, the image that doesn't appear in the slideshow is the fourth one. [https://robf101.bitbucket.io/assets/BACScreen4.jpg](https://robf101.bitbucket.io/assets/BACScreen4.jpg). 

Again, inspecting element and under the "Sources" tab, the flag is `MACS{heR3uG0}`

