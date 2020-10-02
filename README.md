# Cortex Material Design Subtasks
Examples of LivePortal UI Progress options

This project contains some subtasks that create an HTML output that can be used on any LivePortal UI blocks.
Using the Material Design panels a new and fresh look and feel is available for LivePortal UIs.
However, you would need to understand how to create and write those html parts.
These subtasks will make that part a lot easier: simple provide the details and the subtasks return the html.

Items that are part of this project:

### 1. CTX-MDS-covert-table-2-html
This subtask creates the Material Design html from a table variable. You can supply the following inputs:

- table - The Cortex table variable that needs to be converted
- table-id: The table_id for the html generated. Will be set to 'table1' if omitted
- Panel Title: The text that should be displayed as the title of the table.
- Panel Subtitle: The text that should be displayed as the subtitle of the table.
                  It can be used as a short explanation of the table contents.
                  The text will be displayed in smaller font than the table title.
- Panel Title Colour: The background colour of the table header. Pick any of:
                      crtxlblue (default), crtxgreen, crtxindigo, crtxorange
- Columns2skip: A comma separated list of column names to skip from being added to the output html
- Panel width: Supply the bootstrap column width value (from 1 - 12) for the width of the table.
               The table is set to automatically center itself to the area it is placed in.
- Action: Supply the action column details
- Action icon: Supply a Material Design icon to be displayed. If omitted as default the double_arrow will be used.

### 2. CTX-MDS-create-button
This subtask creates the html for a Material Design Styled button. You can supply the following inputs:

- Text: The text that should be displayed on the button
- Icon: Use any Google material design icon. The reference list can be found here: [http://design.google.com/icons/](http://design.google.com/icons/)
- Icon position: Use 'left' or 'right' to position the icon Left or Right from the button text
- Colour: Use crtxorange, crtxblue, danger, red, warning, orange, success,green, info, lightblue, primary,purple, default,regular,grey
- Outlined: Please use 'yes' for outlined colour only. If omitted no outline will be used
- Size: Please use 'small', 'regular' or 'large'. When omitted regular size will be used
- Style: Please use 'default', 'round' or 'simple'. If omitted, 'default' will be used.
- Trigger: Add any trigger text that you want to validate in the next step.
           It will be used to populate a variable for a control called CONTROLLABEL.
           That still needs to be added as a hidden object in the LivePortal block.
           If omitted, only the 'Next' button is triggered and no value is passed.

### 3. CTX-MDS-create-dropdown
This subtask creates the html for a Material Design styled dropdown button. You can supply the following inputs:

- Text: The text that should be displayed on the drop-down button
- Icon: Use any Google material design icon. The reference list can be found here: [http://design.google.com/icons/](http://design.google.com/icons/)
- Icon position: Use 'left' or 'right' to position the icon Left or Right from the button text
- Colour: Use crtxorange, crtxblue, danger, red, warning, orange, success,green, info, lightblue, primary,purple, default,regular,grey
- Outlined: Please use 'yes' for outlined colour only. If omitted no outline will be used
- Size: Please use 'small', 'regular' or 'large'. When omitted regular size will be used
- Style: Please use 'default', 'round' or 'simple'. If omitted, 'default' will be used.
- Width: Enter the width to be used. This should be a value from 1 - 12
- Labels: Supply a LIST variable containing the Labels to be displayed
- Triggers: Supply a LIST variable containing the trigger values to be used.
            These should match the order of the Labels list.
            It will be used to populate a variable for a control called CONTROLLABEL.
            That still needs to be added as a hidden object in the LivePortal block.
            If omitted, only the 'Next' button is triggered and no value is passed.

### 4. CTX-MDS-create-panel-header
This subtask creates the html for a Material Design styled panel. You can supply the following inputs:

- Title: The text that should be used as the Title of the panel or card
- Title_position: Location of the Card Tile text. Use one of the following options:
                    right (default value if omitted), center, left
- Icon: The icon that should be displayed inside the card title box. Use any Google material design icon. The reference list can be found here: [http://design.google.com/icons/](http://design.google.com/icons/)
- Colour: The colour used for the panel header icon box.
            Use crtxorange, crtxblue, danger, red, warning, orange, success, green, info, lightblue, primary, purple, default, regular, grey, gray
- Width: Supply the bootstrap column width value (from 1 - 12) for the width of the panel.
         It will automatically center itself to the area it is placed.
### 5. CTX-MDS-create-tile
This subtask creates the html for a Material Design styled tile. A tile is similar to a panel with the main difference that it can be used in Dashboards to display counters, with action capability (e.g. to create a drill down). You can supply the following inputs:

- Title: The text that should be used as the Title of the card. If the Title list is supplied it will supersede this input parameter.
- Category: Use this (single) category if only 1 category is to be used on the tile. If the Category list is supplied it will supersede this input parameter.
- Icon: The icon that should be displayed inside the card title box. Use any Google material design icon. The reference list can be found here: [http://design.google.com/icons/](http://design.google.com/icons/)
- Colour: The colour used for the panel header icon box.
            Use crtxorange, crtxblue, danger, red, warning, orange, success, green, info, lightblue, primary, purple, default, regular, grey, gray
- Width: Supply the bootstrap column width value (from 1 - 12) for the width of the panel.
         It will automatically center itself to the area it is placed.
- Footer text: The footer text can be optionally supplied to display at the bottom of the tile.
- Category list: If the tile needs to display several values then use this list to supply the value description (e.g. Total Time Saved). Suggest to leave the first record in this list blank (see title list)
    The category text will displayed in a smaller font than its value.
- Title list: If the tile needs to display several values then use this list to supply the values (e.g. "4 Days, 5 Hrs"). The first record in this list will be displayed as the top title.
    A value will displayed in a larger font than the category.
- Action list: A list of actions that should be performed when the user clicks the value.
   This could be used to drill down into a subtask that retrieves the data but lists it in a table.

### 6. CTX-MDS-Progress-Indicator
This subtask creates the html for a Material Design styled Progress Indicator that can be used instead of the Cortex 'Please Wait' spinning indicator.

- Title_text: The main (title) text that is displayed in the Progress Update card
- Description: A description of the current activity/process being executed in the background. Can take more characters than the title text
- Old_value: The old value of the Progress html code. This will be altered (marked as completed) and positioned underneath the new Progress Indicator.
- Cortex_server_connected_to_internet: Supply no if the Cortex server cannot retrieve the Material Design icons from the Google servers. If so, an HTML code for an hourglass and a checkmark will be used. If omitted the default value of yes will be used.

### 7. CTX-MDS-test
This is an example flow that demonstrates the use of all subtasks mentioned above. It is a very simple to follow flow.

# Installation Instructions
You require the material-dashboard-cortex.css file part of this project to be copied to the Cortex application server.
The last part of this video demonstrates how to do that: [https://vimeo.com/458599158/67a838ef39](https://vimeo.com/458599158/67a838ef39)

:thumbsup: Success! :wink:
