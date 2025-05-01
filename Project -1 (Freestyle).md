# FREESTYLE PROJECT 1
## STEPS TO CREATE THE FREESTYLE PROJECT
### 1- On Dashborad select "New Item" --> enter the Item name --> select "Freestyle project" --> click OK
### 2- Configuration tab will open which consist of six sections -
        1- General
                -provide the description for the project
        2- Source Code Management
                -not required in this project
        3- Triggers
                -not required in this project
        4- Environment
                -not required in this project
        5- Build Steps
                -Click 'Add Build Step' --> select your requirement(there are seven options) (example- 'Execute Window Batch Command' or 'Execute Shell')
                -here i am running Jenkins on Windows so i selected 'Execute Window Batch Command' --> box will open 
                -write the required command in the box provided, for example --> echo "hello world"
        6- Post build Actions
                -not required in this project
### 3- Save the Configuration 
### 4- Now, several options will be available to you for that item that you created.-
        1- Status
        2- Changes
        3- Workspace
        4- Build Now
        5- Configure
        6- Delete Project
        7- Rename
### 5- Click on 'Build Now'
### 6- This will run the Project and shows on bottom left corner under the Builds whether it run correctly or showed any error.
### 7- Click the Build you created, this will show the Console output and steps.
