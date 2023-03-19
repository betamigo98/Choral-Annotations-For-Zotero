<div align="center">
  <center><h1>Template Scripts</h1></center>
</div>
<br>
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
	
<img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Scripts%20-%20Templates%20(Centered).png" width=95% height=120%></p>
<p align="center"><i>Example of a full template script once edited in the advanced configuration pane - example with centered rendering templates</i><br>
</p>
<br>
<br>

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
<br>
<br>

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
<br>
<br>

# 3. Other Templates - with previews
Use of dashes, spaces and quotations marks in the Sample template section (3) has been labelled as <i>"french convention"</i> where dialogs are opened and closed with a quotation mark, a space, and use dashes for speaker switch expect for the first line.

This might be arbitrary but has been maintained to illustrate the syntax theme. This is the convention I encountered in my highschool education and encountered in [some other sources](https://www.google.com/search?q=convention+typographie+dialogue+theatre&oq=convention+typographie+dialogue+theatre&aqs=edge..69i57j69i64.7856j0j4&sourceid=chrome&ie=UTF-8).

Depending on national and cultural traditions, norms and conventions, editorial choices and personal preferences, you might want to edit the corresponding part of the template yourself if the templates proposed below don't match what you are looking for.
	
## 3.1 Left-Left, French Convention
<p align="center">
<img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Left-Left%20-%20French%20Convention.png" width=65% height=70%>
</p>

* Title Note: ```<h1 style="text-align:left;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:left;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />

## 3.2 Left-Right - French Convention
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Left-Right%20-%20French%20Convention.png" width=65% height=70%)>

* Title Note: ```<h1 style="text-align:left;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:center;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:center;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:center;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />```

## 3.3 Centered - French Convention
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Centered%20-%20French%20Convention.png" width=65% height=70%>

* Title Note: ```<h1 style="text-align:center;">Choral Annotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:center;">{{citation}}:<p style="text-align:left">{{highlight quotes='false'}}{{if comment}}<p style="text-align:center;">WORRIED SEEKER: <p style="text-align:right;">{{comment}}{{endif}}</p><br />``` <br />

# 4. More Templates

## 4.1 Mixted : Centered for names and left-right for speeches (without french convention)
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Mixted%20-%20No%20French%20Convention.png" width=65% height=70%></p>

* Title Note: ```<h1 style="text-align:center;">Choral Annotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:center;">WORRIED SEEKER:<p style="text-align:right;">{{comment}}</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:right;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />```

## 4.2 Didascalia Workaround
### with notes (sticky notes)
It is hardly possible to enter didascalias (precision about the speech "quietly", etc), however, it is possible to get an apromixation editing the (standalone) note template.<br>
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Left-Left%20-%20Didascalies%20-%20French%20Convention.png" width=65% height=70%></p>

Limitations: if you insert your own personal comment on a sticky note, your name or the one you choose will not appear anymore (and you will also loose the possibility to use the note for your own monolog, comment, etc).
If that is somehow interesting for you, it has been done with the following templates:<br />
* Title Note: ```<h1 style="text-align:center;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">{{comment}}:</p>``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:left;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />

### with tags
You could use tag to write didascalias and stage directions. However, it will not be possible to diferentiate between you and the author(s). You could place it either before the authors speech or your speech.It is a similar problem as described above with notes.<br>
* Case for tags are didasclaia for the authors: ```<p>WORRIED SEEKER <i>({{tags}}):</i><br />{{comment}} {{highlight}} {{citation}}</p>```
* For the comentator (just switch variables positions): ```<p>{{tags}} {{citation}} {{highlight}} WORRIED SEEKER {{comment}} </p>```

### with tags and colors
Now tags could be only place at one place in the template, so you could only make didascalia for one side of the speakers.<br>
But if you use highlight colors to make it correspond to a set of didascalia of your choice (quietly, loud, etc), you could work your way.<br>
Continuing the above example: 
* Let blue the color for "quietly"
* Highlight for author didascalias ; tags for comentator - you didascalias
* Will render every tag as didasclaia so better use it before starting to read and use a set of tag specific for that case (do not mix it with "normal" usecase).
```
{{if color =='#2ea8e5'}}
       <p>{{citation}} <i>(quiet):</i><br /> {{highlight}}<br />{{if tags}}WORRIED SEEKER<i>({{tags}}):</i><br />{{comment}}{{endif}}</p>	   
{{else}}
       <p>{{tags}} {{citation}} {{highlight}} WORRIED SEEKER {{comment}} </p>
{{endif}}
```
<br>
<br>

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

<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Zotero%20-%20Rename%20Highlight%20Colors.png"
width=72% height=113%>

<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Zotero%20-%20Rename%20Highlight%20Colors%20-%20Showed.png" width=72% height=113%><br />
<p align="center"><i>When "show color highlights" is ticked on the note pane"</i>
<br>
<br>

# 5. Additional Notes And Help
* You should easily retrieve the three templates fields by entering "template" in the advanced configuration search bar.
They are: 1) Note title template ; 2) Note template (a.k.a. sticky note or standalone note) ; and 3) Highlight text template.<br>
* A complete choral annotation formatting needs to be continued outside Zotero reader i.e. on a text editor where Zotero pluggin has been correctly installed. You have to add the Choral Style from Zotero before being able to use it in the text editor.
* Current avalaible CSV Choral Style is adapted from APA7 and should render in your text editor "AUTHOR DATE" with the word "and" instead of ";" between two references. Observe that the colon is edited from the template in that scenario. It is a minimal change substituting the inline citation format : "(Author,date,page locator)" by : "AUTHOR DATE: " (AUTHOR1 and AUTHOR2 and AUTHOR3 when multiple authors). For more than three author, it goes back to "et al." (could be edited for extension in the future).
* At this moment it has been decided to do it from the template so that the APA7 choral in this repo should only render AUTHOR DATE for in-line citation in your word document. See additional notes in the section belo for more details about this.
* Double brackets, dashes and spaces for the so called "French convention" in the section above is also managed from the template syntax (it could have been and it is still possible to manage that from the CSL style instead of the template).
* Try to variate authorship: set the publisher, the location, or even a date or any ohter metada in the role of the "author" (or "speaker" "actor" "performer" if you wish).
* See [screenshots](https://github.com/betamigo98/Choral-Annotations-For-Zotero/tree/main/Screenshots) and [sample documents](https://github.com/betamigo98/Choral-Annotations-For-Zotero/tree/main/Choral%20Rendering%20-%20Samples) if you want to see more.
<br>
<br>

# 6. Troubleshooting, Ajustments, Customization
Remember that there are two components involved for a full choral rendering: the templates from Zotero and the CSL Styles. The CSL settings only applies for the author side, not to the comentator side ("your" side). So it has to be checked carefully that it does not result in double use of brackets, dashes, spaces, and ":".<br />
Once the template editor in Zotero is opened, it is quite easy to make some trials-and-errors from Zotero Reader switching from one window to the other.
<i> You could keep multiple windows opened in your desktop and tabswitch in between it : the template editor pane, the pdf reder pane, and the word editor open and play from that.</i><br />

CSL edition for yourself (remember [there are APA7 modified for chorale purpose avalaible to download](https://github.com/betamigo98/Choral-Annotations-For-Zotero/tree/main/CSL%20Choral%20Styles) with more to come) might take more time as you will have to look up in macros, variable and value, then save and install the style (quicker of you are confortable enough to edit straight from the console in Zotero corresponding menu).<br />
In any case there is lot of documentation avalaible for CSL edition. You could also open an issue in that repo, or ask help in Zotero forums too.<br />
<br>
<br>

<div align="center">
  <center><h1>Bonus: Template for tag rendering in Obsidian</h1></center>


<div align="center">
  <center><h2>A. Template That Insert The Tags You Added To Your Highlights</h1></center>
</div>
<p align="center">Highlight your text, create note, add to tags to each of these items, then create a note formatted as "#hgh/<yourtag>" so Obsidian can render it as nested!

<p align="center">Tagging Highlights look like this in Zotero:<br>
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Bonus%20-%20Zotero%20Highlight.png" width=72% height=60%>
	
<p align="center">See how it renders in Obsidian:<br>
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Bonus%20-%20Obsidian%20Tagged-Highlight.png" width=72% height=89%>

<p align="center">Get the Template:<br>

```{{if comment}}<p>{{comment}}{{endif}}<blockquote><i>{{highlight}}</i></blockquote>{{citation}}{{if tags}}<br/>#hgh/{{tags : tags join=' #hgh/'}}{{endif}}```

## B. Templates That Insert The Tags You Added To Your Notes
	
<p align="center">Tagging your (sticky) notes look like this in Zotero:<br>
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Bonus%20-%20Zotero%20Note.png" width=72% height=60%>

<p align="center">See how it render in Obsidian: <br>
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Bonus%20-%20Obsidian%20-%20Tagged%20Note.png" width=72% height=100%>

<p align="center">Note that the other tags you did on your Obsidian appear diferently:<br>
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Bonus%20-%20Obsidian%20-%20Other%20Tags%20.png" width=72% height=89%><br>

<p align="center">Get the template:<br>
	
```<p><i>Note:{{comment}}</i>{{if tags}}<br/>#note/{{tags : tags join=' #note/'}}{{endif}}<br/>{{citation}}</p>```<br>

<i>Note: same pattern as described above but for Notes (a.k.a. sticky notes).</i>

## C. Wrap up and Outlook
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Bonus%20-%20Zotero%20Full%20Preview.png"width=72% height=66%><br>
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Bonus%20-%20Obsidian%20-%20Full%20Preview.png" width=72% height=118%>
	
	
<p align="center"><a href="https://forums.zotero.org/discussion/99170/from-zotero-to-obsidian-a-tag-based-workflow-in-pictures#latest"> See also the original post in Zotero forum</a href>.<br>
<i>Note: you could add conditionals on colors so you got "#hgltY/<yourtag>" for yellow highlight for example. That template might come in the future.</i>
	<br>
<br>
# More Bonus with Obsidian
## Make tags match a color and give you the option to nest by starting highlight comment with "/"
1. Use of '#' for color conditionnal will render clickable tags in Obsidian as normally expected
2. Start a comment by "/" and nest as much as it makes sense to you (and as much as obsdian allow it)

Take this example: 
1. all yellow highlights means "Method"
2. you might or not narrow it down to qualitative metod and quantitative method
3. quantiative method narrows down to linear regression and no-linear regression

with such template: 
```
{{if color =='#ffd400'}}
	<p>{{tags}}#METHOD{{comment}} {{highlight quotes='false'}} {{citation}}</p>
{{else}}       
	<p> {{highlight}} {{citation}} {{comment}}</p> 
{{endif}}
```

See that every highlight will sort out with "#Method" as a prefix. So typing /quantitative/nolinear will sort our #method/quantitative/nolinear.

### why use it?
Depending on each one's profile and preference
* could reduce some click 
* nested tag could bring more precise information
* give it a unix-terminal feel starting your comment by the sign "/"
* you can add anything after the nest (of course you don't need to nest everytime)

	
# More Bonus : visual creativity with OneNote
	
<p align="center"><h3>Do you think you could use your annotations to mimick Stephane Mallarmé 's work <i>"Un coup de dé jamais n'abolira le hasard?"</h3><br>
<br>
<p align="center"><img src="https://cdn.essentiels.bnf.fr/media/images/cache/cache/rc/uPCv9QQz/uploads/media/image/20220111152909000000_p111.jpg" width=52% height=54%><br><i>© Bibliothèque nationale de France taken from <a href="https://essentiels.bnf.fr/fr/image/4cf885ab-033d-4ab5-923e-555fc91ce1ee-un-coup-des-jamais-nabolira-hasard-3)">French National Library website</ a href></i>.
	<br>
	<br>

<p align="center">...well, sort of. With Microsoft OneNote you can reach that kind of results:<br>
<p align="center"><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Visual%20Creativity%20And%20Annotations%20(OneNote).gif">
</div>
