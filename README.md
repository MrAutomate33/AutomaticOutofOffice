# Automatic Out of Office
Turns your out of office on and off at the right time.

## General
This Power Automate flow will activate your out of office automatically.
The flow checks your agenda 6 hours ahead if there is an Outlook event with the category 'Out of Office'.
If so, the flow will set your out of office for the duration of that Outlook event.

The out of office message contains by default the message that you are currently not available but will be again at <end of Outlook event>.
If the event duration of the out of office is 5 days or longer, the message will add 2 days in the message.
This way you can prevent a busy start of your day after a long week off.
The out of office will always turn itself off at the end of the event, despite it may add 2 days in the message.
  
The flow will notify you if it has activated your out of office. You will receive the notification through the [Power Automate app](https://emea.flow.microsoft.com/en-us/mobile/download/?src=banner).
  
_Out of office message supports HTML_

## Connections in use
* Notifications
* Office 365 Outlook

## Setup
1. Please download the [AutomaticOutofOffice.zip](https://github.com/MrAutomate33/AutomaticOutofOffice/raw/main/AutomaticOutofOffice.zip).
2. Go to https://emea.flow.microsoft.com/manage/flows/import.
3. Upload and import the AutomaticOutofOffice.zip file.
4. Open the Power Automate flow and change the calendar id to the desired calendar (needs to be done in 1 locations).
5. Set your internal and external out of office messages in the action 'Set up automatic replies (V2)'.
6. Save.
7. Don't forget to turn the solution on.
8. Create the category 'Out of Office' in your Outlook.
9. Label your events with the category 'Out of Office'.
