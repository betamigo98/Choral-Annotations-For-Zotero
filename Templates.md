# Presentation
This file compile all the templates that has to be inserted in the corresponding advanced preference fields in the Zotero desktop interface.
  
<p>Two formats options had been considered below: 1) a centered format and 2) a right-left format.
Other options such as left-right formats, left-left format, and others settings are of course possible but has not been written yet.</p>

## Precautionary notes
<p>One shall observe that they are three classes of template corresponding to the three different item and item fields in the advanced preference pane in Zotero:
1) highlight template ; 2) standalone note template ; and 3) note title template. To get a consistent format for one option it is recommended to edit all of these three classes. You might try and see for yourself.

A last layer of customisation is related to the syntax wrapped around the speakers of the dialogs, that is, mainly the location of the following characters: "" ; : ; and - . It also include the capitalisation of the comentator name and the spaces in between two blocks of text in the note file that is displaye in the right-hand pane of the Zotero reader interface. Depending on national and cultural traditions, norms and conventions, editorial choices and personal preferences, you might want to edit the corresponding part of the template yourself if the templates proposed below don't match what you are looking for.

<i>A brief remark here is that one could edit csl style to set such formatting (see inline citation fields for letters caps, prefix and suffix in the csl editor). Such editing has to be carefully watch for consistency with the name (if any) of the comentaror, because the csl settings will not applies for the latter.</i>

A couple of csl style has been edited and can be downloaded (see corresponding file and section in this repository).

Default name for comentator is "Worried seeker" in capital letter (WORRIED SEEKER). You'll have to change it manually or by search and replace.

# 1.Centered Formatted Templates
## 1.1 Highlight Templates
### 1.1.1 Base Templates
```<p style="text-align:center;">{{citation}}<br /> {{highlight}}</p>{{if comment}}<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”{{endif}}</p><br />```
### 1.1.2 Tighter Form
<i>Thighter forms are the same forms as the base template above without breaking space at the end</i><br />
```<p style="text-align:center;">{{citation}}<br /> {{highlight}}</p>{{if comment}}<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”{{endif}}</p>```
## 1.2 Standalone Note Template
### 1.2.1 Base Template
```<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”</p><br />```
### 1.2.2 Tighter Form
Same form as the base template above without breaking space at the end <br />
```<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”</p>```<br />
<i>Note: Citation will not be linked – because adding the variable {{citation}} would made the author appears. If a csl style could be edited so the inline citation is left blank, it will give a local solution for this, however, it will breaks the highlight template render because the cst style will also apply to the {{citation}}, ending with an empty author thus loosing the intention of putting the comentator in vocal dialog with the author(s).</i>
## 1.3 Note Title Template
```<h1 style="text-align:center;">{{title}}<br/>({{date}})</h1>```
# 2.Left-Right Formatted Templates
Author will appear on the left ; commentator (“you”) on the right of the document where you will export your note and render with csl style.
<i>Note: Consecutive highlights that are not commented would stay on the right (or the left if you prefer and edit as it). Improvement here would be to set a conditional that spot two consecutive elements – let it a paragraph on the same side, and if that is the case, change the paragraph alignment to the opposite side. I do not see currently how this would be possible. Anyway, it seems to be a minor issue.</i>
## 2.1 Highlight Templates
### 2.1.1 Base Template
```<p style="text-align:left;">”{{citation}}<p style=”text-align:left;”{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<p style="text-align:right;">{{comment}}”{{endif}}</p>```
### 2.1.2 Tighter Breakspaces Form But With Space In Between Two Elements
```<p style="text-align:left;">”{{citation}}<br />{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<br /> {{comment}}”{{endif}}</p><br />```
### 2.1.3 Thightest Form
```<p style="text-align:left;">”{{citation}}<br />{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<br /> {{comment}}”{{endif}}</p>```

## 2.2 Standalone note templates
Commentator's comments will be place on the right side of the document
### 2.2.1 Base Template
```<p style="text-align:right;">WORRIED SEEKER<br />”{{comment}}”</p><br />```
### 2.2.2 Thighter
```<p style="text-align:right;">WORRIED SEEKER<br />”{{comment}}”</p>```

# 3.Samples
## Left-Left, French Conventions
(picture from zotero reader below)
* Title Note: ```<h1 style="text-align:left;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:left;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />

## Left-right, French Conventions
* Title Note: ```<h1 style="text-align:left;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:center;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:center;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:center;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />

## Centered, French Conventions
* Title Note: ```<h1 style="text-align:center;">Choral Annotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:right;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />

# 4.More Templates

## 4.1 Didascalia Workaround
It is hardly possible to enter didascalias (precision about the speech "quietly", etc), however, it is possible to get an apromixation editing the (standalone) note template. See picture below to grasp the idea.
Didascalias rendered fro the reader insert link TK.

Limitations: if you insert your own personal comment on a sticky note, your name or the one you choose will not appear anymore.
If that is somehow interesting for you, it has been done with the following templates:<br />
* (Standalone) Note Template: ```<p style="text-align:left;">{{comment}}:</p>``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:left;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />
* Title Note: ```<h1 style="text-align:center;">Choral Anotations<br/>{{date}}</h1><br />```






