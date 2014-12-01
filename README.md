Titanium Alloy ACS Login Widget
================
##Overview

A login widget for Titanium Alloy that integrates with Appcelerator Cloud Services.

##Manifest
- version: 1.0 (beta)
- github: https://github.com/bettytran/acsloginwidget
- author: Betty Tran
- platforms: iOS, Android

##Features

- ACS Login
- Forgotten password retrieval 
- New account creation:
	Added parameter confirmation-template: 'new_user_confirmation'
	Use by creating an ACS email-template 'new_user_confirmation' containing the activation link
	<a href="https://cloud.appcelerator.com/users/confirmation?key={{key}}&confirmation_token={{confirmation_token}}">
	Your confirmation message here</a>


##Usage

- Include the widget in your application config.json file as a dependency:

```
"dependencies": {
	"com.appcelerator.acslogin": "1.1"
}
```

- Place the widget folder inside `app/widgets`. Create the `app/widgets` folder if it does not already exist.


###Initialise the widget

__views/index.xml__

```
<Require type="widget" src="com.appcelerator.acslogin" id="acslogin"/>
```

__controller/index.js__

```
$.acslogin.init({callback: function(e){//login success callback}});
```



