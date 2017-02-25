# KeiMainMenu

This class defines a side menu controller with hide animation (with pan or with touch outside its bounds).

#SETUP

- add the KeiMainMenu.swift file to the project
- create a ViewController swift file (ex. MainMenu) of your menu and inherit the KeiMainMenu as so
`class MainMenu: KeiMainMenu {}`
- then create the ViewController in sotryboard and set its class to "MainMenu" and its storyboard ID - ex. the same "MainMenu"
- to make your menu animated you have to define its instance via singleton, I recommend to do so in appDelegates didFinishLaunchingWithOptions function
`MainMenu.shared.MainMenuCtrl = UIStoryboard(name: "Main", bundle: nil).instantiateViewController(withIdentifier: "MainMenu")`
- now you can show you menu with calling a function like so
`MainMenu.shared.show(parentCtrl: your_parent_ctrl, menuWidth: nil)`
where "your_parent_ctrl" is the viewController on which the menu should show up
