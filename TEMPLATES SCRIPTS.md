# Template Scripts
This file compiles templates scripts.<br>
<p align="center">Overview of scripts from the advanced configuration pane - example with centered rendering templates<br>
<img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Scripts%20For%20Templates%20(Centered)%20-%20With%20Screenshot.png" width=120% height=120%></p>
Each one has to be inserted in the three corresponding advanced preference fields in the Zotero desktop interface.
You could easily retrieve these three fields by entering "template" in the preference search bar.
They are: 1) Note title template ; 2) Note template (a.k.a. sticky note or standalone note) ; and 3) Highlight text template.
See screenshots for an overview with examples.</p>
  
<p align="justify">Two main formats options had been considered below: 1) a centered format and 2) a right-left format.<br />
Other options such as left-right formats, left-left format, had been inserted in the sections 3 and 4.<br />
There is also a script to map the highlight colors to any text of your choice (see section 4.3).<br />
		  
Default name for comentator is "Worried seeker" in capital letter (WORRIED SEEKER). You'll have to change it manually or by search and replace.<br />
					       
Use of dashes, spaces and quotations marks in the Sample template section (3) has been labelled as "french convention", that is to open and close dialogs with a quotation mark, a space, and use dashes for speaker switch expect for the first line. This might be arbitrary but has been maintained to illustrate the syntax theme.  
This is the convention I encountered in my highschool education and encountered in some sources. Depending on national and cultural traditions, norms and conventions, editorial choices and personal preferences, you might want to edit the corresponding part of the template yourself if the templates proposed below don't match what you are looking for.
														      
Elements you might want to change in that case are the one that refers to all that syntax wrapped around the speakers of the dialogs, that is, mainly the location of the following characters: ```" "" " ";" ":" ";" "-" ";"``` the spaces in between two blocks of text and the capitalisation of the comentator name.

<p align="justify">A complete choral annotation formatting needs to be continued outside Zotero reader i.e. on a text editor where Zotero pluggin has been correctly installed and require CSL editioning.<br />
		  
Choral styles has been edited for that purpose and are avalaible for download. These are minimal customization of already existing style (APA7 etc), substituting the inline citation format : "(Author,date,page locator)" by : "AUTHOR DATE: ".

The explicit purpose of this is to render it so it feels like a dialog with you and the author, giving to it a screenplay, screenwrighting look.
Value of this is that it lets room for variations, for example to set the publisher, the location, or even a date in the role of the "author" (or "speaker" "actor" "performer" if you wish).<br />

Such variations are in the roadmap so it will be accessible for download in the future, but you could already try it for yourself, starting from the CSL edition documentation and visual editor for example.< br>

Current avaliable Choral Style is adapted from APA7 and should render as AUTHOR DATE, plus use the word and instead of ";" between two references.<br />
 
If any doubt, checking the screenshots is a good option, and you can also do some trials-and-errors to adjust to your specific preferences and need.

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


# 3. Other Templates - with previews
## 3.1 Left-Left, French Conventions
<p align="center"> Preview: <br>
<img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20Left-Left%20French%20Convention.png" width=70% height=70%>
</p>

* Title Note: ```<h1 style="text-align:left;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:left;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />``` <br />

## 3.2 Left-right, French Conventions
<p align="center">Preview: <br /> <img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20Left%20Right%20-%20French%20Convention.png" width=70% height=70%)>

* Title Note: ```<h1 style="text-align:left;">Choral Anotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:center;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:center;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:center;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />```

## 3.3 Centered, French Conventions
<p align="center">Preview: <br /> <img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20-%20Centered%20-%20French%20Convention.png" width=70% height=70%>

* Title Note: ```<h1 style="text-align:center;">Choral Annotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:left;">" WORRIED SEEKER: {{comment}} "</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:center;">{{citation}}:<p style="text-align:left">{{highlight quotes='false'}}{{if comment}}<p style="text-align:center;">WORRIED SEEKER: <p style="text-align:right;">{{comment}}{{endif}}</p><br />``` <br />

# 4. More Templates

## 4.1 Mixted : Centered for names and left-right for speeches (without french convention)
<p align="center"> Preview:<br /><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20Mixted%20-%20No%20French.png" width=70% height=70%></p>

* Title Note: ```<h1 style="text-align:center;">Choral Annotations<br/>{{date}}</h1><br />```
* (Standalone) Note Template: ```<p style="text-align:center;">WORRIED SEEKER:<p style="text-align:right;">{{comment}}</p><br />``` <br />
* Higlight Note Template: ```<p style="text-align:left;">” {{citation}}: {{highlight quotes='false'}}{{if comment}}<p style="text-align:right;">&#8211; WORRIED SEEKER: {{comment}} ”{{endif}}</p><br />```

## 4.2 Didascalia Workaround
It is hardly possible to enter didascalias (precision about the speech "quietly", etc), however, it is possible to get an apromixation editing the (standalone) note template.<br>
<p align="center">Preview: <br /><img src="https://github.com/betamigo98/Choral-Annotations-For-Zotero/blob/main/Screenshots/Pdf%20Left%20Left%20-%20Didascalies%20-%20French%20Convention.png" width=70% height=70%></p>

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

# 5 Troubleshooting, ajustments, customization
Remember that there are two components involved for a full choral rendering: the templates from Zotero and the CSL Styles. The CSL settings only applies for the author side, not to the comentator side ("your" side). So it has to be checked carefully that it does not result in double use of brackets, dashes, spaces, and ":".<br />
Once the template editor in Zotero is opened, it is quite easy to make some trials-and-errors from Zotero Reader switching from one window to the other.
<i> You could keep multiple windows opened in your desktop and tabswitch in between it : the template editor pane, the pdf reder pane, and the word editor open and play from that.</i><br />

CSL edition for yourself (remember [there are APA7 modified for chorale purpose avalaible to download](https://github.com/betamigo98/Choral-Annotations-For-Zotero/tree/main/CSL%20Choral%20Styles) with more to come) might take more time as you will have to look up in macros, variable and value, then save and install the style (quicker of you are confortable enough to edit straight from the console in Zotero corresponding menu).< br />
In any case there is lot of documentation avalaible for CSL edition. You could also open an issue in that repo, or ask help in Zotero forums too.<br />


