# Dataview Frontmatter CSS Snippet and Template

## What is this?
This is a CSS snippet and Obsidian Template that enables a nice view of a file's YAML Frontmatter in the following places:
- Files embedded into a Canvas
- File Previews from "Folder Gallery View" 
- File Previews from when the cursor hovers over a link

## Prerequisites:
- [Dataview Plugin](https://obsidian.md/plugins?id=dataview) (third party)
- Templates Plugin (by obsidian)

## Preparations:
1. Move the CSS Snippet into your Snippets Folder
	- Enable it under Appearance > CSS Snippets
1. Enable the Dataview Plugin
	-  Enable JavaScript Queries in the Plugin Settings
2. Enable the Templates Plugin
	- Specify a Templates Folder in the Plugin Settings 
	- Move the Template into the specified Templates Folder

## How to use it:
When you want a file's YAML Frontmatter to be seen in the previously mentioned places, then
1. Go into the file's edit mode (`ctrl+E` or `cmd+E`)
2. Move into one of the first lines right below the Frontmatter
3. Insert the Template (`ctrl+P` or `cmd+P`, then type _"insert template"_ and select the Template)

If you want to enable this across all files, you can probably use an editor such as [Visual Studio Code](https://code.visualstudio.com) in order to regex through all your files and insert the Template's text right below each Frontmatter section.