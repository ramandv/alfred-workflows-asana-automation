**Setup Instructions:**
1. Create a new access token on Asana and set it on the accessToken env variable [1]

2. Set your user id: writing "asana" and click on "My ID", then press enter to copy the gid and paste it in the "me" env variable

3. Set the workspace: write "asana" and click on "Workspaces", select the workspace you want and paste the gid in the "workspace" env variable

**How to use:**

In order to create a task, use the "task" keyword.
The format of the input should be this: title;description
for e.g. "create a website;check the email from John and create the website according to his instructions"

In order to open the newly created task add ":" followed by a space at the end of your input, for e.g. "create a website :" or "create website;setup wordpress :"

In order to assign a user to a task, you can use the "-a" flag followed by a space at the end of your input, for e.g. "create a website -a"

In order to add project to a task, you can use the "-p" flag followed by a space at the end of your input, for e.g. "create a website -p"

In order to add a task to a section in a project you can use the "-s" flag followed by a space at the end of your input, make sure that the "-p" flag exists

You can also use here the open URL feature by simply add the ":" character at the end (before or after the flags), for e.g. "create a website : -a" or "create logo;use blue and grey colors -a -p :"

In order to resync data like projects, sections or users you can use the "asana" keyword and select the desired function.

**Development:**

To run the script you the following command:

```me=$me workspace=$workspace accessToken=$accessToken node index.js 'task title;task description'```

Set the variables to your vars.

**Optional variables:**
assignee, projectId, sectionId

**References:**

[1] https://asana.com/guide/help/api/api