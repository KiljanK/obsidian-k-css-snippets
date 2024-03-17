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

## How to selectively display Properties:
It is possible to limit, which properties are shown. To do this, add another list property to the note, called `d-f-show`. Within this list property, add all the property names you want to be shown in the previews/embeds. Pretty self-explanatory.

Please note that this will only take effect, if:
- The property `d-f-show` isn't empty
- The list inside `d-f-show` isn't empty
- The list inside `d-f-show` doesn't contain a `null`

The last two points can be checked by looking at the source view of the YAML Frontmatter. To do this, go into editing mode (`ctrl+E` or `cmd+E`) and toggle on the [source mode](https://notes.nicolevanderhoeven.com/obsidian-playbook/Using+Obsidian/02+Making+Notes+in+Obsidian/Views+in+Obsidian#Source+mode). Then, check the raw text of the `d-f-show` property. It should NOT be an empty list (`[]`). If it has bullet points, none of them should be empty.