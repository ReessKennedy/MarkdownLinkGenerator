[Remote Link](https://github.com/ReessKennedy/MarkdownLinkGenerator)

## What ⚡
Convert publicly-shared cloud links on GDrive to markdown format for quick inclusion in markdown compatible editors like Notion, Obsidian, Logseq, Joplin, etc. 

## Why 🤷‍♂️
Sometimes it's nice to keep your images and pdfs in a digital asset manager and your text in a markdown. This allows you to merge them and not created duplicates by dragging around your already-cloud-hosted files. 

## How 📋
Super easy. 
Just download this repo and open the HTML file. 
Copy the full public link for your file into the form and it will parse it, grab the id and create a markdown version. Alternative, just enter the id and it will put it in the right place. 
There is an optional control for the width of the outputted element that will only work in some markdown editors, like Obsidian. 

## Issues ⚠️
Didn't want to use API to keep it fast and simple but this means it's difficult to identify the file type which means it's also hard to create a proper switch between image html embed previews and pdf. CORS policy issues made it difficult to even tell if the file existed or not. In a hosted setting possibly CORS issue could be solved. Could also, in a hosted environment, not use pure JS which might allow better load verification, though there may be a speed hit if using a server side language like python or php. 

## Todo ☑️ 🤔
- [ ] JS added to automatically copy and past the markdown link without need select and copy
- [ ] Check on which apps support the size changes
- [ ] Add cookies to persist the width part next time you use it ... this can be "your width setting"
- [ ] Launch this on cloud flare for a free hosted version people can use
- [ ] Put it into a chrome extension
- [ ] Make sure it works for links copied from cloud version as well as desktop
- [ ] Create illustrative GIFS to make it easy to understand
- [ ] Maybe add a checkbox toggle to turn on or off the image preview
- [ ] Encourage better method to handle checks for file types -- pdf loading is imperfect
- [ ] Idea: Possibly width element should be aligned to the right so takes up less horizontal space
