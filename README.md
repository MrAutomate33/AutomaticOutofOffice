# Microsoft Outlook - Automatic Out of Office
Turns your out of office on and off at the right time.

## General
This Power Automate flow will activate your out of office automatically.
Depending on which version you have chosen the flow will check on Outlook events with the `category` `Out of Office` or with the `Show As` status `Out of Office`.
The flow will set your out of office for the duration of that Outlook event.

The out of office message contains by default the message that you are currently not available but will be again at \<end of Outlook event\>.
If the event duration of the out of office is 5 days or longer, the message will add 2 days in the message.
This way you can prevent a busy start of your day after a long week off.
The out of office will always turn itself off at the end of the event, despite it may add 2 days in the message.
  
The flow will notify you if it has activated your out of office. You will receive the notification through the [Power Automate app](https://emea.flow.microsoft.com/en-us/mobile/download/?src=banner).
  
_Out of Office message supports HTML._

### Out of Office by Category
The flow checks your agenda by default 6 hours ahead if there is an Outlook event with the `category` `Out of Office`.
You will have to create this category by yourself in Outlook.
<br/>Download: [AutomaticOutofOffice-Category.zip](/../../raw/main/AutomaticOutofOffice-Category.zip)

### Out of Office by Show As
The flow checks your agenda by default 5 min ahead if there is an Outlook event with the `Show As` status `Out of Office`.
<br/>Download: [AutomaticOutofOffice-ShowAs.zip](/../../raw/main/AutomaticOutofOffice-ShowAs.zip)

## Connections in use
* Notifications
* Office 365 Outlook

## Setup
1. Please download the desired flow. [Out of Office by Category](/../../#out-of-office-by-category) or [Out of Office by Show As](/../../#out-of-office-by-show-as).
2. Go to https://emea.flow.microsoft.com/manage/flows/import.
3. Upload and import the `AutomaticOutofOffice.zip` file. [Extra help for importing Power Automate projects](/../../../MrAutomate33/blob/main/files/CreateConnectionsInImport.md).
4. Open the Power Automate flow and change the calendar id to the desired calendar (needs to be done in 1 location).
5. Set the your desired date/time formatting and timezone in the action `Convert time zone - Set date and time format`. By default the formatting is: `dd-MM-yyyy HH:mm`.
6. Set your internal and external out of office messages in the action `Set up automatic replies (V2)`.
7. Save.
8. Don't forget to turn on the Power Automate flow.
9. Label your Outlook events correctly with the Show As status or category.
