# K18-CCW1067A-walkthrough-chatbot-creation-deployment
Walkthrough Creating and deploying a chatbot usecase

            <!\-\- /\* Font Definitions */ @font-face {font-family:"Cambria Math"; panose-1:2 4 5 3 5 4 6 3 2 4; mso-font-charset:0; mso-generic-font-family:roman; mso-font-pitch:variable; mso-font-signature:-536870145 1107305727 0 0 415 0;} @font-face {font-family:Calibri; panose-1:2 15 5 2 2 2 4 3 2 4; mso-font-charset:0; mso-generic-font-family:swiss; mso-font-pitch:variable; mso-font-signature:-536870145 1073786111 1 0 415 0;} /* Style Definitions */ p.MsoNormal, li.MsoNormal, div.MsoNormal {mso-style-unhide:no; mso-style-qformat:yes; mso-style-parent:""; margin:0in; margin-bottom:.0001pt; mso-pagination:widow-orphan; font-size:12.0pt; font-family:"Calibri",sans-serif; mso-ascii-font-family:Calibri; mso-ascii-theme-font:minor-latin; mso-fareast-font-family:Calibri; mso-fareast-theme-font:minor-latin; mso-hansi-font-family:Calibri; mso-hansi-theme-font:minor-latin; mso-bidi-font-family:"Times New Roman"; mso-bidi-theme-font:minor-bidi;} a:link, span.MsoHyperlink {mso-style-priority:99; color:#0563C1; mso-themecolor:hyperlink; text-decoration:underline; text-underline:single;} a:visited, span.MsoHyperlinkFollowed {mso-style-noshow:yes; mso-style-priority:99; color:#954F72; mso-themecolor:followedhyperlink; text-decoration:underline; text-underline:single;} p.MsoListParagraph, li.MsoListParagraph, div.MsoListParagraph {mso-style-priority:34; mso-style-unhide:no; mso-style-qformat:yes; margin-top:0in; margin-right:0in; margin-bottom:0in; margin-left:.5in; margin-bottom:.0001pt; mso-add-space:auto; mso-pagination:widow-orphan; font-size:12.0pt; font-family:"Calibri",sans-serif; mso-ascii-font-family:Calibri; mso-ascii-theme-font:minor-latin; mso-fareast-font-family:Calibri; mso-fareast-theme-font:minor-latin; mso-hansi-font-family:Calibri; mso-hansi-theme-font:minor-latin; mso-bidi-font-family:"Times New Roman"; mso-bidi-theme-font:minor-bidi;} p.MsoListParagraphCxSpFirst, li.MsoListParagraphCxSpFirst, div.MsoListParagraphCxSpFirst {mso-style-priority:34; mso-style-unhide:no; mso-style-qformat:yes; mso-style-type:export-only; margin-top:0in; margin-right:0in; margin-bottom:0in; margin-left:.5in; margin-bottom:.0001pt; mso-add-space:auto; mso-pagination:widow-orphan; font-size:12.0pt; font-family:"Calibri",sans-serif; mso-ascii-font-family:Calibri; mso-ascii-theme-font:minor-latin; mso-fareast-font-family:Calibri; mso-fareast-theme-font:minor-latin; mso-hansi-font-family:Calibri; mso-hansi-theme-font:minor-latin; mso-bidi-font-family:"Times New Roman"; mso-bidi-theme-font:minor-bidi;} p.MsoListParagraphCxSpMiddle, li.MsoListParagraphCxSpMiddle, div.MsoListParagraphCxSpMiddle {mso-style-priority:34; mso-style-unhide:no; mso-style-qformat:yes; mso-style-type:export-only; margin-top:0in; margin-right:0in; margin-bottom:0in; margin-left:.5in; margin-bottom:.0001pt; mso-add-space:auto; mso-pagination:widow-orphan; font-size:12.0pt; font-family:"Calibri",sans-serif; mso-ascii-font-family:Calibri; mso-ascii-theme-font:minor-latin; mso-fareast-font-family:Calibri; mso-fareast-theme-font:minor-latin; mso-hansi-font-family:Calibri; mso-hansi-theme-font:minor-latin; mso-bidi-font-family:"Times New Roman"; mso-bidi-theme-font:minor-bidi;} p.MsoListParagraphCxSpLast, li.MsoListParagraphCxSpLast, div.MsoListParagraphCxSpLast {mso-style-priority:34; mso-style-unhide:no; mso-style-qformat:yes; mso-style-type:export-only; margin-top:0in; margin-right:0in; margin-bottom:0in; margin-left:.5in; margin-bottom:.0001pt; mso-add-space:auto; mso-pagination:widow-orphan; font-size:12.0pt; font-family:"Calibri",sans-serif; mso-ascii-font-family:Calibri; mso-ascii-theme-font:minor-latin; mso-fareast-font-family:Calibri; mso-fareast-theme-font:minor-latin; mso-hansi-font-family:Calibri; mso-hansi-theme-font:minor-latin; mso-bidi-font-family:"Times New Roman"; mso-bidi-theme-font:minor-bidi;} span.SpellE {mso-style-name:""; mso-spl-e:yes;} span.GramE {mso-style-name:""; mso-gram-e:yes;} .MsoChpDefault {mso-style-type:export-only; mso-default-props:yes; font-family:"Calibri",sans-serif; mso-ascii-font-family:Calibri; mso-ascii-theme-font:minor-latin; mso-fareast-font-family:Calibri; mso-fareast-theme-font:minor-latin; mso-hansi-font-family:Calibri; mso-hansi-theme-font:minor-latin; mso-bidi-font-family:"Times New Roman"; mso-bidi-theme-font:minor-bidi;} @page WordSection1 {size:8.5in 11.0in; margin:1.0in 1.0in 1.0in 1.0in; mso-header-margin:.5in; mso-footer-margin:.5in; mso-paper-source:0;} div.WordSection1 {page:WordSection1;} /* List Definitions */ @list l0 {mso-list-id:554049684; mso-list-type:hybrid; mso-list-template-ids:-1849627302 67698703 67698713 67698715 67698703 67698713 67698715 67698703 67698713 67698715;} @list l0:level1 {mso-level-tab-stop:none; mso-level-number-position:left; text-indent:-.25in;} @list l0:level2 {mso-level-number-format:alpha-lower; mso-level-tab-stop:none; mso-level-number-position:left; text-indent:-.25in;} @list l0:level3 {mso-level-number-format:roman-lower; mso-level-tab-stop:none; mso-level-number-position:right; text-indent:-9.0pt;} @list l0:level4 {mso-level-tab-stop:none; mso-level-number-position:left; text-indent:-.25in;} @list l0:level5 {mso-level-number-format:alpha-lower; mso-level-tab-stop:none; mso-level-number-position:left; text-indent:-.25in;} @list l0:level6 {mso-level-number-format:roman-lower; mso-level-tab-stop:none; mso-level-number-position:right; text-indent:-9.0pt;} @list l0:level7 {mso-level-tab-stop:none; mso-level-number-position:left; text-indent:-.25in;} @list l0:level8 {mso-level-number-format:alpha-lower; mso-level-tab-stop:none; mso-level-number-position:left; text-indent:-.25in;} @list l0:level9 {mso-level-number-format:roman-lower; mso-level-tab-stop:none; mso-level-number-position:right; text-indent:-9.0pt;} ol {margin-bottom:0in;} ul {margin-bottom:0in;} -->  

**Adding the client to a custom page.**

1. First lets create a custom **UI Page** in your instance. On the left hand navigation side bar, search for **UI Pages.** Click the link.

![](https://github.com/csjain/K18-CCW1067A-walkthrough-chatbot-creation-deployment/blob/master/image001.png)

2. Click the blue **New** button at the top left.

![](https://github.com/csjain/K18-CCW1067A-walkthrough-chatbot-creation-deployment/blob/master/image002.png)

3. In the **Name** field add the name **$custom\_virtual\_agent_chat** and also check the **direct** checkbox.

![](https://github.com/csjain/K18-CCW1067A-walkthrough-chatbot-creation-deployment/blob/master/image004.png)

4. In the **HTML** section you will see some HTML that looks like this:

<?xml version="1.0" encoding="utf-8" ?>

<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">

</j:jelly>

5. In the white space between the <j:jelly\> tags, add an iframe which links to the virtual agent, and has a set height and width, using the following code snippet:

<iframe height="800" width="400" src="/$sn-va-web-client-app.do"></iframe>

This will embed the widget on your page.

![](https://github.com/csjain/K18-CCW1067A-walkthrough-chatbot-creation-deployment/blob/master/image006.png)

6. Click the blue **Submit** button at the top right of the page.

![](https://github.com/csjain/K18-CCW1067A-walkthrough-chatbot-creation-deployment/blob/master/image007.png)

7. Now navigate to your custom page by going to **https://<your-instance>/$custom\_virtual\_agent_chat**

You should see the chat widget you placed on the page. You can embed the widget with this method on any page you need!

![](https://github.com/csjain/K18-CCW1067A-walkthrough-chatbot-creation-deployment/blob/master/image009.png)
