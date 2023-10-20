
[mdlinks.reess.org](https//mdlinks.reess.org) for deployed version
## What ⚡
Quickly convert Google Drive image file links into markdown-formatted links for quick for quick inclusion in markdown compatible editors like Notion, Obsidian, Logseq, Joplin, etc. 

Could probably be expanded to support OneDrive and Dropbox and others but I use GDrive and works for my use case now. I used it multiple times per day. 
## Why 🤷‍♂️
GoogleDrive is great for image storage and sync but the product makes it a little tricky to deliver an image link that can be publicly embedded inside html or markdown to share with the world. 

As a result, though billions use GoogleDrive many people will use additional image hosting services like [imugrr](https://imgur.com/) to host images they share online or embed inside various documents. This solution allows you to stop doing this and centralize all your shared images in one place. 

Advantages of this method: 
- Lightweight git repositories: Adding a bunch of image files to a git repository to support your image adds lots of storage size to your git repo that could be offloaded. 
- Cost: Free solution with unlimited bandwidth to your images
- Organization: Centralize all your shared images into one folder, if you wish, so you can see and remember everything you shared. 
- Editing after sharing: Images can be edited after sharing from this central location. 
- Public and Private: Obfuscate origins of your images using public links that live on a Google domain to remove any associations to you if you don't want any public associations
- Prevent duplicate files: If you already use GDrive and keep some assets there but then have to you another service for shared image this creates dups and this helps avoid that. 

Disadvantages: 
- Potential that you delete a file on GoogleDrive by accident or something happens to your account then you could lose links to an image library possibly powering a large number of public docs
- Similar issue if you replace these images from backup because Google will treat these as new images and create new IDs which will break all your old links

## How 📋
You could sust download this repo and open the HTML file but you can also use the hosted version deployed via Cloudflare pages and I use this version every day: 


Visit: https://mdlinks.reess.org/

### 2)
Share an entire folder of images as public OR just publicly share individual files and copy the link create
![|400](https://drive.google.com/uc?id=1ZKalQWov637vCimiRkShBXiZeXfoaq32&usp=drive_fs)

### 3)
Paste the link created into mdlinks.reess.org (or you can also just paste the file ID) to get the markdown link and paste that into your doc: 
![|400](https://drive.google.com/uc?id=1Z_UxZpVTKoD8mc4dPGuT8MfBJOXTa8wW&usp=drive_fs)

Width control: 
There is an optional control for the width of the outputted element that will only work in some markdown editors, like Obsidian. 

## Features
### Auto copy to clipboard
When the markdown link is created it's automatically copied to your clipboard so you needn't actually do anything else even though it shows you a text area for the markdown ... so **one less step!**
### Image width set + persist
Allows you set the width you prefer for your outputted markdown images and your setting should persist during your usage, and next usage ... you can reset to full width by just deleting width setting. 
https://forum.obsidian.md/t/resize-image/6517
### Image preview
Shows you a preview of your image. 
## Issues ⚠️
Didn't want to use the Google API to keep it fast and simple but this means it's difficult to identify the file type which means it's also hard to create a proper switch between image html embed previews and pdf. CORS policy issues made it difficult to even tell if the file existed or not. In a hosted setting possibly CORS issue could be solved. Could also, in a hosted environment, not use pure JS which might allow better load verification, though there may be a speed hit if using a server side language like python or php. 

## Todo ☑️ 🤔
- [x] JS added to automatically copy and past the markdown link without need select and copy ... actually have it so it automatically gets copied. 
- [x] Add cookies to persist the width part next time you use it ... this can be "your width setting" (this now happens via local storage)
- [x] Launch this on cloud flare for a free hosted version people can use
- [x] Create illustrative GIFS to make it easy to understand
- [ ] Put it into a chrome extension?
- [ ] Might be cool to show a log of recently generated images? 
- [ ] Perhaps should add outputs for the thumbnail version of the image as well for lighter embeds
- [ ] Check on which apps support the size changes
- [ ] Make sure it works for links copied from cloud version as well as desktop
- [ ] Maybe add a checkbox toggle to turn on or off the image preview
- [ ] Encourage better method to handle checks for file types -- pdf loading is imperfect
- [ ] Idea: Possibly width element should be aligned to the right so takes up less horizontal space

### Don't do
- [ ] Perhaps should reposition to put the width on top ... Update: No. Tried this and didn't like
