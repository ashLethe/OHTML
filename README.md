# ObsidianToHtmlConverter
I helped make a python script for converting [obsidian](https://obsidian.md/) md-file to static (local) html (recursively adds all link/images)
This script is for when you need to distribute something from your obsidian vault to someone that either does or does not have Obsidian.

The script has 4 optional parameters:
1. **-v**: The vault directory
    - Default is the current directory.
2. **-o**: The output directory
    - Default is the a subdirectory called "html" in the vault directory.
3. **-c**: Export to html or not [**true**/false]
    - **false**: Exports the choosen md-file to a new vault and bring all the images and linked md-files with it (recursively!)
        - Easily opened as a new vault in obsidian and everything just works!
    - **true**: Exactly like above, but also create html-files next to the md-files (with images and working links to other md.html-files in vault)
        - The script puts an index.html-file in the root of the exported vault that is a direct link to your exported file.md.html for easily access
4. **-d**: Download external images to local vault [**true**/false] (if export to html is chosen)
    - **true**: downloads all the images
    - **false**: normal link to external image that downloads when viewed

Run this script from the root of obsidian vault (or anywhere if you specify the vault location)

usage: 
```python exportMdFileToHtml.py <[-v vaultDir] <filename.md> <[-o outputDir]> <[-c true/false] [-d true/false]>```
- "<filename.md>" **no filepath needed** unless you have several files with same name

Only tested on Windows!

