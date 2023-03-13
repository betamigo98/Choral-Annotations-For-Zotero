This file compile all the templates that has to be insert in the corresponding advanced preference pane in Zotero menu.

They are three classes of template, each corresponding to the three different item and item fields in the preference pane.  
1) highlight template ; 2) standalone note template ; and 3) note tittle tempplate.

Across this classification, the two following options has been considered as the two mains rendered format: 1) centered format and 2) right-left format.
A third option is possible, that is the one a left-left format. Then it can go along with many more as the templates remains totally editable by any user (right-right for example). 
To get a consistent format for one option, the three classes has to be edited. Note though that the note tittle might be of secondary consideration. But preferably it is considered better to have a consistent format for the highlight and the standalone template.

Then come a third layer of modification that comes with all the variations that one could imagine around the syntax of the speakers and of the dialogs, that is mainly the location of "" ; : ; and - .
Depending on national and cultural tradition, convention, and norms (or for specific editorial conventions), you might want to edit the corresponding template part yourself if there are not yet avalaible.
The capitalisation of letter is also to determine.

Important note here for desambiguition is that one could edit csl style to set letters caps, prefix and suffix for inline citation. Such editing has to be carefully watch for consistency with the name (if any) of the comentarist.
A couple of style has been edited and can be downloaded (see corresponding file and section).

The last layer of modification and variations are related to the formatting of the spaces in between two blocks of text in the note file that is displaye in the right-hand pane of the Zotero reader interface.

# Centered formatted templates

## highlight template
### base template
<code><p style="text-align:center;">{{citation}}<br /> {{highlight}}</p>{{if comment}}<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”{{endif}}</p><br /></code>
### tighter
(same as base template above without breaking space at the end)
<code><p style="text-align:center;">{{citation}}<br /> {{highlight}}</p>{{if comment}}<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”{{endif}}</p></code>

## standalone note template
### base template
<code><p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”</p><br /></code>
### tighter 
(same as base template above without breaking space at the end)
<p style="text-align:center;">WORRIED SEEKER<br />”{{comment}}”</p>


Note:Citation will not be linked – because adding the variable {{citation}} would made the author appears. If a csl style could be edited so the inline citation is left blank, it will give a local solution for this, however, it will breaks the highlight template render because the cst style will also apply to the {{citation}}, ending with an empty author thus loosing the intention of putting the comentator in vocal dialog with the author(s).

## note tittle template
<code><h1 style="text-align:center;">{{title}}<br/>({{date}})</h1></code>


# left-right formatted templates
Author on the left ; commentator (“you”) on the right 

Note: Consecutive highlights are not commented would stay on the right (or the left if you prefer and edit as it). Improvement here would be to set a conditional that spot a consecutive element – let it a paragraph on the same side, and if that is the case, change paragraph alignment to the opposite side. I do not see currently how this would be possible. Anyway, it seems to be a minor issue.
## highlight template
### base template
<code><p style="text-align:left;">”{{citation}}<p style=”text-align:left;”{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<p style="text-align:right;">{{comment}}”{{endif}}</p></code>
### tighter breakspaces but space in between too elements
<code><p style="text-align:left;">”{{citation}}<br />{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<br /> {{comment}}”{{endif}}</p><br /></code>
### thightest form
<code><p style="text-align:left;">”{{citation}}<br />{{highlight quotes='false'}}”</p>{{if comment}}<p style="text-align:right;">” WORRIED SEEKER<br /> {{comment}}”{{endif}}</p></code>

## standalone note template
Commentator on the right
### base template
<code><p style="text-align:right;">WORRIED SEEKER<br />”{{comment}}”</p><br /></code>
### thighter
<code><p style="text-align:right;">WORRIED SEEKER<br />”{{comment}}”</p></code> 
