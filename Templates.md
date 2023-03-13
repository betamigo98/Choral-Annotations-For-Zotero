# Presentation
This file compile all the templates that has to be inserted in the corresponding advanced preference fields in the Zotero desktop interface.
  
<p>Two formats options had been considered below: 1) centered format and 2) right-left format.
Other options such as left-right formats, left-left format, and any other are of course possible but has not been written yet.</p>

<p>Also, one shall observe that they are three classes of template corresponding to the three different item and item fields in the advanced preference pane in Zotero:
1) highlight template ; 2) standalone note template ; and 3) note title template. To get a consistent format for one option it is recommended to edit all of these three classes. You might try and see for yourself.

Another layer of modification comes with all the variations regarding the syntax of the speakers and of the dialogs, that is, mainly the location of the following characters: "" ; : ; and - .
Depending on national and cultural tradition, convention, and norms (or for specific editorial conventions), you might want to edit the corresponding template part yourself if there are not yet avalaible.
The capitalisation of letter is also to determine.

The last layer of modification and variations are related to the formatting of the spaces in between two blocks of text in the note file that is displaye in the right-hand pane of the Zotero reader interface

<i>A brief remark here for desambiguition is that one could edit csl style to set letters caps, prefix and suffix for inline citation. Such editing has to be carefully watch for consistency with the name (if any) of the comentarist.</i>

A couple of style has been edited and can be downloaded (see corresponding file and section in this repository).

Default name for comentator is: Worried seeker in capital letter. you'll have to change it manually.


# 1 Centered formatted templates
## 1.1 Highlight templates
### 1.1.1 Base Templates
```<p style="text-align:center;">{{citation}}<br /> {{highlight}}</p>{{if comment}}<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”{{endif}}</p><br />```
### 1.1.2 Tighter form
<i>Thighter forms are the same forms as the base template above without breaking space at the end</i><br />
```<p style="text-align:center;">{{citation}}<br /> {{highlight}}</p>{{if comment}}<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”{{endif}}</p>```
## 1.2 Standalone note template
### 1.2.1 Base template
```<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”</p><br />```
### 1.2.2 Tighter form
Same form as the base template above without breaking space at the end <br />
```<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”</p>```<br />
<i>Note: Citation will not be linked – because adding the variable {{citation}} would made the author appears. If a csl style could be edited so the inline citation is left blank, it will give a local solution for this, however, it will breaks the highlight template render because the cst style will also apply to the {{citation}}, ending with an empty author thus loosing the intention of putting the comentator in vocal dialog with the author(s).</i>
## 1.3 Note Title Template
```<h1 style="text-align:center;">{{title}}<br/>({{date}})</h1>```
# 2 Left-right Formatted Templates
Author will appear on the left ; commentator (“you”) on the right of the document where you will export your note and render with csl style.
<i>Note: Consecutive highlights are not commented would stay on the right (or the left if you prefer and edit as it). Improvement here would be to set a conditional that spot a consecutive element – let it a paragraph on the same side, and if that is the case, change paragraph alignment to the opposite side. I do not see currently how this would be possible. Anyway, it seems to be a minor issue.</i>
## 2.1 Highlight template
### 2.1.1 Base template
```<p style="text-align:left;">”{{citation}}<p style=”text-align:left;”{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<p style="text-align:right;">{{comment}}”{{endif}}</p>```
### 2.1.2 Tighter breakspaces form but space in between too elements
```<p style="text-align:left;">”{{citation}}<br />{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<br /> {{comment}}”{{endif}}</p><br />```
### 2.1.3 Thightest form
```<p style="text-align:left;">”{{citation}}<br />{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<br /> {{comment}}”{{endif}}</p>```
## 2.2 Standalone note template
Commentator's comments will be place on the right side of the document
### 2.2.1 Base template
```<p style="text-align:right;">WORRIED SEEKER<br />”{{comment}}”</p><br />```
### 2.2.2 Thighter
```<p style="text-align:right;">WORRIED SEEKER<br />”{{comment}}”</p>```
