# Template Scripts
Below are all the templates scripts that has been edited so far: <br>
1. centered format with couple of variations on spacement. See [section 1](https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Template%20Scripts.md#1-centered-formatted-templates)
2. right-left format with also variations on spacement. See [section 2](https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Template%20Scripts.md#2-left-right-formatted-templates)
3. left-right formats, left-left format, had been inserted in [section 3](https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Template%20Scripts.md#3-other-templates---with-previews) and [section 4](https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Template%20Scripts.md#4-more-templates) gives some extra templates
4. highlight colors mapping to any text of your choice is in [section 4.3](https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Template%20Scripts.md#43-using-highlight-colors)
5. there is also an attempt to integrate didascalias in [section 4.2](https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Template%20Scripts.md#42-didascalia-workaround)

* Default name for comentator is "WORRIED SEEKER". You'll have to change it manually or by search and replace.<br />
* Special characters wrapping the dialogs ```" "" " ";" ":" ";" "-" ";"``` and letter capitalization could be edited both from within the template syntax and the CSV style editor.
* Each script has to be inserted in the three corresponding advanced preference fields in the Zotero desktop interface.
* If in doubt, checking the screenshots is a good option, and you can also do some trials-and-errors to adjust to your specific preferences and need. There are also some [additional comments](https://github.com/betamigo98/Choral-Annotations-For-Zotero/edit/main/TEMPLATES%20SCRIPTS.md#5-additional-notes-and-help) and a [help section](https://github.com/betamigo98/Choral-Annotations-For-Zotero/edit/main/TEMPLATES%20SCRIPTS.md#6-troubleshooting-ajustments-customization) ath the bottom of this page.

<img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Scripts%20-%20Templates%20(Centered).png" width=120% height=120%></p>
<p align="center"><i>Example of a full template script once edited in the advanced configuration pane - example with centered rendering templates</i><br>
</p>

# 1. Centered Formatted Templates
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


# 2. Left-Right Formatted Templates
Author will appear on the left ; commentator (“you”) on the right of the document where you will export your note and render with csl style.

<i>Note: Consecutive highlights that are not commented would stay on the right (or the left if you prefer and edit as it). Improvement here would be to set a conditional that spot two consecutive elements – let it a paragraph on the same side, and if that is the case, change the paragraph alignment to the opposite side. I do not see currently how this would be possible. Anyway, this is a minor issue.</i>
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

# 3. Other Templates - with previews
Use of dashes, spaces and quotations marks in the Sample template section (3) has been labelled as <i>"french convention"</i> where dialogs are opened and closed with a quotation mark, a space, and use dashes for speaker switch expect for the first line.

This might be arbitrary but has been maintained to illustrate the syntax theme. This is the convention I encountered in my highschool education and encountered in [some other sources](https://www.google.com/search?q=convention+typographie+dialogue+theatre&oq=convention+typographie+dialogue+theatre&aqs=edge..69i57j69i64.7856j0j4&sourceid=chrome&ie=UTF-8).

Depending on national and cultural traditions, norms and conventions, editorial choices and personal preferences, you might want to edit the corresponding part of the template yourself if the templates proposed below don't match what you are looking for.
	
## 3.1 Left-Left, French Convention
<p align="center"> Preview: <br>
<img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Left-Left%20-%20French%20Convention.png" width=70% height=70%>
</p>

* Title Note: ```<h1 style="text-align:left;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:left;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />

## 3.2 Left-Right - French Convention
<p align="center">Preview: <br /> <img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Left-Right%20-%20French%20Convention.png" width=70% height=70%)>

* Title Note: ```<h1 style="text-align:left;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:center;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:center;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:center;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />```

## 3.3 Centered - French Convention
<p align="center">Preview: <br /> <img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Centered%20-%20French%20Convention.png" width=70% height=70%>

* Title Note: ```<h1 style="text-align:center;">Choral Annotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:center;">{{citation}}:<p style="text-align:left">{{highlight quotes='false'}}{{if comment}}<p style="text-align:center;">WORRIED SEEKER: <p style="text-align:right;">{{comment}}{{endif}}</p><br />``` <br />

# 4. More Templates

## 4.1 Mixted : Centered for names and left-right for speeches (without french convention)
<p align="center"> Preview:<br /><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Mixted%20-%20No%20French%20Convention.png" width=70% height=70%></p>

* Title Note: ```<h1 style="text-align:center;">Choral Annotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:center;">WORRIED SEEKER:<p style="text-align:right;">{{comment}}</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:right;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />```

## 4.2 Didascalia Workaround
It is hardly possible to enter didascalias (precision about the speech "quietly", etc), however, it is possible to get an apromixation editing the (standalone) note template.<br>
<p align="center">Preview: <br /><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Left-Left%20-%20Didascalies%20-%20French%20Convention.png" width=70% height=70%></p>

Limitations: if you insert your own personal comment on a sticky note, your name or the one you choose will not appear anymore.
If that is somehow interesting for you, it has been done with the following templates:<br />
* Title Note: ```<h1 style="text-align:center;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">{{comment}}:</p>``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:left;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />

## 4.3 Using highlight colors
Systematic users profile might have a very welled organized color system management that they manage to maintain all along their workflow.
The following template propose to make each color correspond to a piece of text.
Change the text pattern below for any text you want i.e. example, method argument, or importance1 importance2 for example.
If you just need to edit some of the colors, delete the correpsonding sections and keep the {{else}} part at the end of the script for closing.
* yellow: "yellow highlight: "
* red: "red highlight: "
* green: "green highlight: "
* blue: "blue highlight: "
* purple: "purple highlight: "
* magenta: "magenta highlight: " 
* orange: "orange highlight: "
* gray: "gray highlight: "

```
{{if color =='#ffd400'}}
       <p> yellow highlight: {{highlight}} {{citation}} {{comment}}</p>
{{elseif color == '#ff6666'}}
       <p> red highlight: {{highlight}} {{citation}} {{comment}}</p>
{{elseif color == '#5fb236'}}
       <p> green highlight {{highlight}} {{citation}} {{comment}}</p>
{{elseif color == '#2ea8e5'}}
       <p> blue highlight: {{highlight}} {{citation}} {{comment}}</p>
{{elseif color == '#a28ae5'}}
       <p> purple highlight: {{highlight}} {{citation}} {{comment}}</p>
{{elseif color == '#e56eee'}}
       <p> magenta highlight: {{highlight}} {{citation}} {{comment}}</p>
{{elseif color == '#f19837'}}
       <p> orange highlight: {{highlight}} {{citation}} {{comment}}</p>	   
{{elseif color == '#aaaaaa'}}
       <p> gray highlight: {{highlight}} {{citation}} {{comment}}</p>	   
{{else}}
       <p> {{highlight}} {{citation}} {{comment}}</p>
{{endif}}
```

# 5. Additional Notes And Help
* You should easily retrieve the three templates fields by entering "template" in the advanced configuration search bar.
They are: 1) Note title template ; 2) Note template (a.k.a. sticky note or standalone note) ; and 3) Highlight text template.<br>
* A complete choral annotation formatting needs to be continued outside Zotero reader i.e. on a text editor where Zotero pluggin has been correctly installed. You have to add the Choral Style from Zotero before being able to use it in the text editor.
* Current avalaible CSV Choral Style is adapted from APA7 and should render in your text editor "AUTHOR DATE" with the word "and" instead of ";" between two references. Observe that the colon is edited from the template in that scenario. It is a minimal change substituting the inline citation format : "(Author,date,page locator)" by : "AUTHOR DATE: " (AUTHOR1 and AUTHOR2 and AUTHOR3 when multiple authors). For more than three author, it goes back to "et al." (could be edited for extension in the future).
* At this moment it has been decided to do it from the template so that the APA7 choral in this repo should only render AUTHOR DATE for in-line citation in your word document. See additional notes in the section belo for more details about this.
* Double brackets, dashes and spaces for the so called "French convention" in the section above is also managed from the template syntax (it could have been and it is still possible to manage that from the CSL style instead of the template).
* Try to variate authorship: set the publisher, the location, or even a date or any ohter metada in the role of the "author" (or "speaker" "actor" "performer" if you wish).
* See [screenshots](https://github.com/betamigo98/Choral-Annotations-For-Zotero/tree/main/Screenshots) and [sample documents](https://github.com/betamigo98/Choral-Annotations-For-Zotero/tree/main/Choral%20Rendering%20-%20Samples) if you want to see more.

# 6. Troubleshooting, Ajustments, Customization
Remember that there are two components involved for a full choral rendering: the templates from Zotero and the CSL Styles. The CSL settings only applies for the author side, not to the comentator side ("your" side). So it has to be checked carefully that it does not result in double use of brackets, dashes, spaces, and ":".<br />
Once the template editor in Zotero is opened, it is quite easy to make some trials-and-errors from Zotero Reader switching from one window to the other.
<i> You could keep multiple windows opened in your desktop and tabswitch in between it : the template editor pane, the pdf reder pane, and the word editor open and play from that.</i><br />

CSL edition for yourself (remember [there are APA7 modified for chorale purpose avalaible to download](https://github.com/betamigo98/Choral-Annotations-For-Zotero/tree/main/CSL%20Choral%20Styles) with more to come) might take more time as you will have to look up in macros, variable and value, then save and install the style (quicker of you are confortable enough to edit straight from the console in Zotero corresponding menu).<br />
In any case there is lot of documentation avalaible for CSL edition. You could also open an issue in that repo, or ask help in Zotero forums too.<br />

# Bonus: Template for tag rendering in Obsidian
I also wrote a template that make use of tags in Zotero and nested tags in Obsidian.<br>
## Template To Add The Tags You Add For Each Of Your Highlights
* Highlight and tag, then create a note formatted as "#hglt/<yourtag>" so Obsidian can render it as nested!
* Of course you could add conditional so you got "#hgltY/<yourtag>" (if you set Y for yeloow in that example). Adjust to your needs!
[img src](https://drive.google.com/file/d/1-V4DvYrpXnCaCYH-UY-rTUGyTSUF4tLV/view)
	
<img src="https://drive.google.com/file/d/1jj2WYz-17_SGwVJp22q7OXZF5lg2cfre/view">
	

''' 
{{if comment}}<p>{{comment}}{{endif}}<blockquote><i>{{highlight}}</i></blockquote>{{citation}}{{if tags}}<br/>#hgh/{{tags : tags join=' #hgh/'}}{{endif}}
'''

## Template To Add The Tags You Add For Each Of Your Notes
* Same pattern as described above for Notes
<img src="https://drive.google.com/file/d/1xNQNz-XoSzWSRyMMUdQFXkQQ0CjzRTIN/view">
<img src="https://drive.google.com/file/d/12x5CN5PTBD6uQPg6UcK11SJroGhuQlbn/view">

'''<p><i>Note:{{comment}}</i>{{if tags}}<br/>#note/{{tags : tags join=' #note/'}}{{endif}}<br/>{{citation}}</p>
'''

See scripts and screenshots from the [original post in Zotero forum](https://forums.zotero.org/discussion/99170/from-zotero-to-obsidian-a-tag-based-workflow-in-pictures#latest).
	
# More Bonus : visual creativity with OneNote
Do you think you could mimick Stephane Mallarmé 's work "un coup de dé jamais n'abolira le hasard?"<br>
![](https://cdn.essentiels.bnf.fr/media/images/cache/cache/rc/uPCv9QQz/uploads/media/image/20220111152909000000_p111.jpg)<br>
© Bibliothèque nationale de France Reproduced from [French National Library websote](https://essentiels.bnf.fr/fr/image/4cf885ab-033d-4ab5-923e-555fc91ce1ee-un-coup-des-jamais-nabolira-hasard-3)<br>

Well, sort of. with Microsoft OneNote that would be posible. See the video below and judge by yourself.
Note: Currently you cannot rotate text from within OneNote.
