# Dark Mode | Anki Cards
## Description

**Advance settings to get Dark Mode on your Anki Cards (Step by step) with imgs**

## Step 1

Go to Tools > Manage Note Types

![](https://i.imgur.com/iovbqn7.png)

After that click on "Add" button to create another Note Type, and just click "Ok"

![](https://i.imgur.com/AUA7iFS.png)

and Choose a name for the new Note Type, in my case, I wrote it like this:

![](https://i.imgur.com/J3uZnaG.png)

And click "Ok"
## Step 2
Now you will have a new option "Pro Dark Mode Cloze", click that one you just created and Click on "Fields"
![](https://i.imgur.com/dvo9xXP.png)

And you'll add 5 Fields named:

Front
Back
Hint
Clue
Category or Pronunciation

**Note: Exactly with Uppecase at the beggining of the word** and click "Close"

![](https://i.imgur.com/21HRS9z.png)


Now, we are ready for the fancy part where we will add the style to the cards, so click on "Cards" button

![](https://i.imgur.com/IJvTa6W.png)

and you'll see 3 boxes in blank, doesn't matter if you are familiar with HTML and CSS, we will just copy 3 parts of code which I share them below:

![](https://i.imgur.com/Gt9AdPW.png)


## Part 1
**Just copy and paste**
```html =
<table class="Question">
   <td class= "Centrado">
      <div style='text-transform: uppercase; font-size: 13px;  font-style: bold;  color: #f0ad4e'> 
         {{Category or Pronunciation}} 
      </div>
      <div style=' text-transform: uppercase;'>{{Front}}</div>
   </td>
</table>

<table class="Content">
   <td>
      <table class="Hidden">
         <div style='font-size: 12px; color:#ECEFF1; text-align: center;padding:5px'>
         <div style='font-size: 13px; color:#8c9ba1; text-align: center;padding:5px; font-style: bold'> 
            {{Hint}}
         </div>
         <td>
         <td class= "Centrado">
            <div style=' font-size: 0px; font-weight=bold; color:#1abc9c;'>
            </div>
            <div style='font-size: 14px;  font-style: bold;  color: #bfcacf'>{{cloze:Back}}</div>
      </table>
      <br>
      <div style='font-size: 11px; color:#b2bec3; text-align: right;padding:5px; font-style: italic;'>
      </div>
      <div style='font-size: 11px; color:#bef306; text-align: right;padding:5px; font-style: italic'>
      {{Tags}}
   </td>
</table>
```
## Part 2

```css =
@import url("https://fonts.googleapis.com/css?family=Nunito+Sans:400,600");
 
.card {
	font-family: 'Nunito Sans', sans-serif;
	font-size: 15px;
	color: #DCDCDC; 
	background-color: #24292e;
}

.clue {
	background: #d9534f;
	padding: .5em 1em;
	font-weight: 600;
	color: #FFF;
	top: -20px;
	left: -15px;
	display: inline-block;
	position: relative;
}

img {
	max-width: auto;
	max-height: 250px;
	/* center image*/
	display: block;
	margin-left: auto;
	margin-right: auto;
	/*Image shadow*/
	padding: 5px;
	box-shadow: 0px 0px 8px #2c3e50;
}
table {
	width: 100%;
	padding: 12px;
}
.Question {
	font-size: 27px;
	color: #FFFAFA;
	background-color: #2f3338;		
	border-radius: 15px 15px 0px 0px;
	opacity: 0.95;
	box-shadow: 0px 0px 10px #16191a;
}
.Content {
	background-color: #343a40;			
	color: #bfcacf opacity: 1;
	color: #FFF;
	height: 100%;
	border-radius: 0px 0px 10px 10px;
	box-shadow: 0px 0px 10px #16191a;
}

td {
	text-align: left;
}
.Centrado {
	padding-top: 5px;
	text-align: center;
	opacity: 1;
}
.CentradoBack {
	font-size: 35px;
	padding-top: 5px;
	text-align: center;
	opacity: 1;
}
.cloze {
	color: #f0ad4e;
}
```

## Part 3

```html =
<table class="Question">
   <td class= "Centrado">
      <div style='text-transform: uppercase; font-size: 13px;  font-style: bold;  color: #f0ad4e'>{{Category or Pronunciation}}</div>
      <div style=' text-transform: uppercase;'>{{Front}}</div>
      <ab =' font-size: 17px;
   </td>
</table>
<table class="Content ">
   <td>
      <div style='font-size: 14px; text-align: center; font-style: bold;  color: #bfcacf'>{{cloze:Back}}</div>
      <br>
      <br>
      <div class="clue" style='color: #fff'>
         Clue: {{Clue}}
      </div>
      <div style='font-size: 11px; color:#bef306; text-align: right;padding:5px; font-style: italic'>
         {{Tags}}
      </div>
   </td>
</table>
```
Now just close the window, it will automatically save it!
And that's pretty much it, we are done! :) 
Now it's time to add a normal note as you have always done it, but you have to be conscious about the information for each field, so I'll add an example:


![](https://i.imgur.com/XwlqHKJ.png)

**Front**: It can be the **word / question**
**Back**: It's the answer/definition of the word/question

Note: Notice that you can add "Cloze deletion" to hide part of the answer by just highlighting the part of the text you want to highlight and just cliking to the [...] icon : 

![](https://i.imgur.com/7VSAnRn.jpg)

**Hint**: It Doesn't need much explanation, it's just a Hint to help you to remember the word.

**Clue**: It's an additional help after showing the answer so you can learn a little bit more, it helps to memorize better.

**Caterogy or Pronunciation**: It's an specification for every question/Word you are studying, it's makes it more professional :)

And finaly you can add some Tags to help you organize it more.

At the end it would look like this on your PC

## Front:
![](https://i.imgur.com/dqaKZ0m.png)
## Back:
![](https://i.imgur.com/ewbXQqN.png)

If you wonder, this is how it looks on a phone :) 

![](https://i.imgur.com/mwY0xRg.jpg)

There is no difference :) 

Let me know if there is any question regarding to this Anki Tutorial.

I hope my help will help you enjoy your study time better!
