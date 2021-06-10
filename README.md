# Artillery - Performance Testing - Challenge 3
The subject under test will be the Todoist API, more specifically the tasks endpoints section
https://developer.squareup.com/reference/square/payments-api

The purpose of this repository is to test the scenarios described on the following challenge:
https://docs.google.com/document/d/18LB5rSbMGS-rViZcdDCKct-vVG8CKmPTs4LfDvvk7n8/edit?usp=sharing

-   Get active task
-   Create a new task
-   Get an active task
-   Update a task
-   Change a task status to ‘complete’
-   Reopen a task
-   Delete a task

## Project Structure

An NPM project that has a very simple structure:

**scripts**: this folder should all the yml files with the artillery scripts.
**package.json**: contains NPM's project main information such as descripction, version, scripts that can be executed and more.
```
 performance_challenge3
  |
  ├ scripts
  |  ├ AllFlows.yml
  |  ├ ChangeTaskStatusToComplete.yml
  |  ├ CreateTask.yml
  |  ├ DeleteTask.yml
  |  ├ GetActiveTask.yml
  |  ├ GetAllTasks.yml
  |  ├ ReopenATask.yml
  |  └ UpdateTask.yml
  |
  ├ package.json
  └ README.md
```

## Pre-requisites

1. Install Node.js + npm [https://nodejs.org/en/](https://nodejs.org/en/)  
[You can follow this guide: [https://wsvincent.com/install-node-js-npm-windows/](https://wsvincent.com/install-node-js-npm-windows/)]  

2. [Installing Artillery](https://artillery.io/docs/guides/getting-started/installing-artillery.html)
3. [Install Git](https://git-scm.com/downloads)
4. [OPTIONAL] Integrated Development Environment:  
	   (Only if you wish to explore the code more confortable)
	- Visual Studio Code: [https://code.visualstudio.com/](https://code.visualstudio.com/)  
	- Atom: [https://ide.atom.io/](https://ide.atom.io/) 
5. [OPTIONAL] [Postman](https://www.postman.com/downloads/) 

## How to run 

1. Generate an authentication token by [signing up](https://todoist.com/prefs/integrations) on Todoist API's webpage and once you login go to [Settings/Integrations](https://todoist.com/prefs/integrations) section. Once there you will find a generated API token.
(example: f6dFF8g146d7c245b07852feed922e5f354c85f297)

2. Open git bash
3. Clone github repository: 

		 git clone https://github.com/efraimpc89/performance_challenge3.git

4. Navigate to *performance_challenge3* folder.
5.  Set a process environment variable so the project can read your auth token.
		
		export token=<api_token>

	example:
		
		 export token=f6dFF8g146d7c245b07852feed922e5f354c85f297

	You can still verify this command worked by executing:

		echo $token
		 
7. Execute one of following commands:
	
	**-To run all scenarios:**

		 npm run all-flows-task
	
	**-To run 'Create Tasks' scenario**:

		 npm run create-tasks
		 
	**-To run 'Get all Tasks' scenario**:

		 npm run get-all-tasks
		 
	**-To run 'Get active task' scenario**:

		 npm run get-active-task

	**-To run 'Update task' scenario**:

		 npm run update-task

	**-To run 'Complete task' scenario**:

		 npm run complete-task

	**-To run 'Reopen task' scenario**:

		 npm run reopen-task

	**-To run 'Delete task' scenario**:

		 npm run delete-task

*NOTE: The results of the tests will be displayed on console.

## Contact

If you have any questions, feel free to send me an email:
efraimpc89@gmail.com

```