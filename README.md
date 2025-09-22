# Notes

related urls:
- relevant bdr item: <https://repository.library.brown.edu/studio/item/bdr:247087/>
- relevant bdr mirador viewer: <https://repository.library.brown.edu/viewers/mirador/bdr:247087/>

---


files in the dev-server dir:
- `h_current.html` -- (the `h_` indicates html) the current html for our mirador viewer that you'd see if you did a view-source on the viewer url, above. 
- `h_more_accessible.html` -- chatgpt-suggested html that loads more-accessible manifest-json. Note that (like `current.html`) viewing this file doesn't show much image information -- the js needs to be loaded. See `full_more_accessible_generated_html` below, or right-click and inspect the generated html from a browser. 
- `dummy_manifest.json` -- chatgpt example minimal version-2 manifest-json loaded-manually by `more_accessible.html`.
- `full_current_generated_html.txt` -- the html produced by javascript executing when loading `current.html` in a browser.
- `full_more_accessible_generated_html.txt` -- the html produced by javascript executing when loading `more_accessible.html` in a browser. 

---


chatGPT image-accessibility exchange:
<https://chatgpt.com/share/68d17932-7c10-8006-b51e-1518829d8eaa>

Summary...
- I asked it to analyze info from <https://repository.library.brown.edu/studio/item/bdr:247087/> for image-accessibility. It had a bunch of good suggestions we can implement, like adding aria-labels to buttons and toolbar-icons, just as one example.
- It mentioned "Provide meaningful alternative text and long description", for that item-page -- which made me wonder how the image-viewer itself would fare.
- I shared the html from the stand-alone mirador-viewer at <https://repository.library.brown.edu/viewers/mirador/bdr:247087/> and asked for an analysis.
- It noted improvments and output suggested updated html (`more_accessible.html`).
- I was interested in this piece because it noted that the source-data should come from the manifest.json file, which the page's js would cause to be converted into more accessible html.
- It showed a sample v3 manifest.json file (with this image's data) -- but our viewer's older, so I had it make a v2 version.
- It mentioned a workflow of data coming from MODS to populate the manifest.json.
- Curious about that, I asked it where image-description data should go in the MODS. It recommended mods:abstract and mods:note, with a few additional attributes -- primarily `@type="image-description"` and `@type="image-description-long"` -- to distinguish between abstract/note entries that do and don't have useful image-description info. It also offered other MODS suggestions.


---


Next steps...

I have some thoughts; will update this more tomorrow.

---
---
