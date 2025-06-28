# Real-Time-Reminder-Clock

This application provides the following features:

Current Time Display: Shows the current time updating every second.

Add Reminder:

You can enter a custom message.

Choose between "One-Time" or "Interval" reminders.

For "One-Time" reminders, set a specific time (HH:MM). If the time is in the past, it will automatically schedule for the next day.

For "Interval" reminders, set a duration in minutes (e.g., every 60 minutes).

Active Reminders List: Displays all your active reminders, showing their message and next trigger information.

Voice Output: When a reminder triggers, it will speak your message aloud using your browser's Speech Synthesis API.

Visual Alert: A temporary banner will appear at the top to visually notify you when a reminder triggers.

Persistence: Reminders are saved to your browser's Local Storage, so they will persist even if you close and reopen the browser tab.

Delete Reminders: You can individually delete reminders or clear all of them at once.

Key changes include:

Added a hidden div with id="customConfirmModal" to the HTML for the modal structure, including a message paragraph and "Yes"/"No" buttons.

Added CSS rules for .modal-overlay and .modal-content to style the modal, make it responsive, and include a backdrop blur effect.

Implemented showCustomConfirm(message, onConfirmCallback) and hideCustomConfirm() JavaScript functions to control the modal's visibility and behavior.

Modified the clearAllRemindersBtn and individual delete buttons' event listeners to call showCustomConfirm instead of confirm().

Created a clearAllRemindersConfirmed() function to encapsulate the logic that runs after the user confirms clearing all reminders.

How to Use:

Enter your desired reminder message in the "Message" field.

Select "One-Time" or "Interval" from the "Type" dropdown.

Adjust the time or interval as needed.

Click "Add Reminder".

The reminder will appear in the "Active Reminders" list and will trigger at the scheduled time.
