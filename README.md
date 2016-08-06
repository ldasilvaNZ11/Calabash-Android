# Calabash-Android
Work project, setting up Automation for Android mobile devices using Calabash tool

#Steps on how to set up Calabash tool for Mac (OSX)

1- Create a folder in your working documents. 

It will make it easier later for you to organize and know where all of your files are located. eg. I've created a folder called 'CalabashAutomation' under Documents
	
2- Install a text editor 

	 #I use a text editor called Atom, you can get it from here: 
	 
	 https://atom.io/
	
	
3- Make sure the latest JDK (java development kit) and Android SDK are installed in your machine

   If they are not you can either get them from the following links:#################
   Or if you currently use Android Studio, it is easy to get those files installed for you by##################


4- Make sure you have Ruby installed into your machine

  #You need to have Ruby installed. Verify your installation by running in terminal:
  
  $ruby -v in a terminal 
  
  #it should print "ruby 2.0.0" (or higher). We recommend using a managed version of Ruby like rbenv or rvm.


5- Open Android Studio to find out where your library path currently is

   #library path can be found in android studio >tools>android>SDK Manager


6- Do the following actions in the terminal windown

A) In terminal run the following command: 

   $ nano ~/.bash_profile 
   
   #it will open the .bash_profile file

B) Save this command in there: 

   $ export ANDROID_HOME=/Users/ldasilvanz11/Library/Android/sdk 

   #do a control 'o', then hit return, then hit control 'x' to exit out file and head back to terminal's intial stage
	
		
7-	Installing bundler, which is going to take care of all the gems for you from now on. Run this command in the terminal: 

    $ gem install bundler 
    
    #or in case you have permission issues, then use instead the following command:

    $ sudo gem install bundler

   
8- Open your text editor from step 2 and create a file naming it: "GEMFILE" 

   #This file is going to be located in the working directory, more precisely inside your CalabashAutomation folder created during step 1. The Gemfile will contain all your Ruby dependencies.

9- Adding contents to your GEMFILE
   
   #Add the line below to your GEMFILE and save it 
   
   source "https://rubygems.org"
   
    $ gem 'calabash-android'
    $ gem 'cucumber'

11- 

In terminal navigate to the folder 'CalabashAutomation' and run the following command: bundle install
run command calabash-android gen to create calabash file structure
move app.apk file into calabashautomation folder
calabash-android run <apk>
