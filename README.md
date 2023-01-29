<b>PROJECT SUMMARY</b><br>
<b>CalcTalk</b> is a native android calculator application that is controlled by voice. This would assist user in solving with every day mathematical problems.
CalcTalk is developed using Android Studio (Java) and is designed for mobiles phones using Android version 4.4 and above. Google assistance feature is used to give voice input to the calculator. Currently, functionality of
basic calculator is being offered that is four basic operations (+, -, ×, ÷) could be performed by voice input.<br>
In future, more features could be introduced with the application like unit conversions, date calculations etc.<br><br>

<b>CODE EXPLANATION</b><br>
Following are the functions created for the project along with their purpose:
<br><br>
<b>setNumericOnClickListener()</b><br>
This function is used to find and set a generalized functionality of OnClickListener to numeric buttons (0, 1, 2…9). Then using for loop this function is applied to each numeric button using built in function findViewById. 
<br><br>
<b>setOperatorOnClickListener()</b><br>
This function is used to find and set OnClickListener to operator buttons, equal button, clear button, speak button and decimal point button. Here using built in function findViewById, each button other than numeric buttons is assigned its unique functionality. 
<br>Example, <br>
a clr button has a functionality to clear output display, <br>
(=) button will trigger function onEqual() or <br>
microphone icon button will trigger function promptSpeechInput().<br>
Also, a common OnClickListener for operators is created then using for loop this function is applied to each operator button using built in function findViewById. 
<br><br>
<b>onEqual()</b><br>
This function has the logic to calculate the solution of the entered expression. It checks first if the input is valid then forms it into an expression to calculate it otherwise displays error message and prompt the user to try again.
<br><br>
<b>promptSpeechInput()</b><br>
This function displays google assistant speech input dialog box for user to voice input mathematical expression.
<br><br>
<b>onActivityResult(int requestCode, int resultCode, Intent data)</b><br>
This function first receives voice input through google assistant then using switch...case of requestCode where through REQ_CODE_SPEECH_INPUT variable which stores phrases that will be considered as eligible for speech input it validates for the eligible speech input.
<br>Example, phrases like equal(s) to, equal(s) all map to the equal (=) operator. Similarly, divide, divide by, upon all map to (÷) operator.
<br><br>
<b>Screenshots</b><br>
 ![Screenshot CalcTalk](https://user-images.githubusercontent.com/56563643/215346784-79cb5f74-e657-4714-b529-17abb72c1532.png)
<br>
**_Figure 1:_** CalcTalk Main Screen<br>
**_Figure 2:_** Expression voice input for multiply operator<br>
**_Figure 3:_** Input display for multiply operator<br>
**_Figure 4:_** Output display for multiply operator<br>
<br><br>
Same procedure is followed to solve expressions for other three operators [+, -, ÷].
