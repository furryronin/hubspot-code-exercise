# Submission Notes

These notes will be read by HubSpot developers. Drop us a line!

## Given more time, what would you have done differently?

Exercise 1 was pretty straight forward, I popped the image into a combination of Figma and Affinity to get the colours, it had a few compression artifacts on the broad colour spaces s hopefully I’ve managed to match them.
I’d like to have finished Exercise 2, I did the best I had with the time available but between handover for my previous job and illness, I haven’t spent nearly as much time on it as I would have liked.

I didn’t get as far as styling up the filter controls or adding search but that along with adding in fuse.js for fuzzy search should have only taken about a day.

I used a pre-existing module I had written for the filters. It has an auto-generate function for the filter selections built in but can currently only generate 1 filter list. If I had more time, I would have updated that to allow the generation of multiple filter options based on derived arrays. - I'll be off to update that repo next week, it's a good idea!

Also the deep linking doesn’t work after webpack has had it’s way with it, something to check and resolve, it’s always a nice feature for users. Lastly I hate a user getting a 'Sorry, we can't find anything that matches that.' from set filters because they have selected a search pattern that doesn't find anything, I'd like to rework the filter controls to make them dynamic, only presenting controls for available items.

While finishing up I have just noticed a potential bug where the 'Sorry, we can't find anything that matches that.' sometimes displays at the end of the list of items, I'll be looking at that as well.
 
I put together a new webpack build process (updated an old one), It’s a little rough, I’d like to refine it given more time. Again, something to do with my gardening leave.
Webpack build process. Includes linting and handlebars support -> ttps://github.com/furryronin/Well-Meaning-Webpack-Workflowhttps://github.com/furryronin/Well-Meaning-Webpack-Workflow
Re-useable filtering system, it's based on a project that was specifically designed to support old browsers in B2B institutions -> https://github.com/furryronin/filter.js

## How did you deviate from the directions, if at all, and why?

Exercise 1 – Although it wasn’t specified, I added a small hover state interaction to the button for some user feedback. I couldn’t get a clean cut of the quote mark icon from the image so encoded a svg from the icon fonts library.

Exercise 2 – Well, I would have liked to finish it but ran out of time. It’s functional, just not completely styled.

## Is there anything else you'd like to let us know?

Thankyou for your patience and understanding in what has been a uniquely trying week.

I hope that the file structure, layout and sparse comments give you some insight into my capabilities and methods, and I welcome any feedback (good or bad) on what I’ve presented.

Both exercises were fun and had plenty of nice little gotchas in them, I hope I got them all.

Many thanks
Gareth

