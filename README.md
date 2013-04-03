todo-list
=========

### Steps To Create Application
- Based on the TodoMVC App: http://todomvc.com/architecture-examples/knockoutjs/
- Create a new developer org and assign the CEO role to the registered user
- Create the web library dependencies:
	- Download jquery ui: http://jqueryui.com/download/
	- Download knockout: http://knockoutjs.com/downloads/knockout-2.2.1.js
	- Download knockout-mapping: https://raw.github.com/SteveSanderson/knockout.mapping/master/build/output/knockout.mapping-latest.js
	- Download knockout-validation: https://raw.github.com/ericmbarnard/Knockout-Validation/master/Dist/knockout.validation.js
	- Download underscore: http://underscorejs.org/underscore.js
	- Download director: https://raw.github.com/addyosmani/todomvc/gh-pages/architecture-examples/knockoutjs/components/director/build/director.js
	- Download TodoMvc: https://github.com/addyosmani/todomvc/tree/gh-pages/architecture-examples/knockoutjs/components/todomvc-common 
	- Create a zip file from the contents: $ zip -r includes.zip * 
	- Add the zip file as a static resource. Be sure to set the access level to public.
	- Create a new visualforce component that includes all the libaries; call it Includes.component.
- Create a site home page:
	- Create a new visualforce page, call it TodoList.page
	- Be sure to add: showHeader="false" standardStylesheets="false" since we want our own styling
	- Also set docType="html-5.0" language="en"
- Create a new force.com site:
	- App Setup -> Develop -> Site -> New Site
	- Use the SiteLogin.page as the site home page
	- Enable the customer portal: Customize -> Customer Portal -> Settings -> Edit -> Enable -> Continue
	- Edit the customer portal, 
		- Set the Administrator
		- Enable Self-Registration
		- Set New User Form URL to SiteRegister
		- Set the Default New User License and Default New User Profile to High Volume Customer Portal
	- Enable login for the site: App Setup -> Develop -> Site -> Login Settings -> Edit, set My Profile Page to MyProfilePage
- TODO: Modify the SiteSamples/SiteStyles.css static resource to contain bootstrap styles
- Register a new user on the site
	- Create a new account that all the registered site users will belong to. Call it TodoList Account
	- Copy the Id of the account and edit the SiteRegisterController to reference the account.
	- Modify the registerUser method of the SiteRegisterController to pass in the page URL of the TodoList.page to the login() call
- Create a ToDo Component
	- Include the web dependencies in the component
	- Create a js file called app.js and upload it as a static resource. 
	- Add the knockout code for the todo app.
	- Modify the TodoList.page to include the Todo.component and position it using bootstrap fluid rows.