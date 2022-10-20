# Cascade Build

This is the steps you will need to take to build a capricorn cascade module from scratch. This is not a common practice, however the steps will still be helpful when building from a copied module. These steps will start with building in the cascade development environment before being built in production in order to be properly tested.

# Building from Scratch

In STTHOMAS DEV 

```

_shared-capricorn

|__ formats
    |__ modules
        |__ campaign
        |__ feed
        |__ image-and-text
        |__ specialized
        |__ text
        |__ web-apps

```

The most commonly used module format file is 'specialized'. It seems to be used as a sort of catch all. This will likely change with the new template builds in the future but as of now, this is most likely the one you will know.

1) After navigating to 'specialized' in 'shared_capricorn', click 'Add Content' located on the top page tool bar next to the site navigation dropdown. 
   - click 'Default' file icon
    - format < >
     - type: 'Velocity'
     - Velocity format file name needs to be kebab-case.
    Example file has been created named 'training test' for reference on formatting new file.

 
# Build from copied file

This is pretty straight forward and usually makes the most sense to do in regards to building.

1) In desired module file ( ex: STTHOMAS DEV/_shared-capricorn/formats/modules/specialized), click to highlight the box next to the file you wish to copy.
2) An icon tool bar will appear after clicking the side box. Select the copy icon. A drawer will pop out for you to confirm by clicking the blue 'copy' button in the corner.
3) Click Confirm Copy on Copy assets pop up.
4) Locate created copy. It should have the same name as the original with an additional '1' after the name.
5) Right click the copy name.
6) Click 'More' from the pop up menu. 
7) Click 'Rename' to rename the copied file.
8) You have now created a "new" file to for with. You may go in an clean up the formatting. 

# Data Definitions 
 Once the module is built you will have to link the module to data definitions in order to integrate the use of variables and props.

1) Locate and click 'Manage Site' on the tool bar on the top of the page.
2) scroll to locate the 'data Definitions'  block and click ' Go to Data Definitions'.
3) Scroll down on the next page and click on 'Universal'.
4) In the 'Universal' file, click edit ( pencil icon) in top right corner. This will open up all of the data definitions.
5) Scroll down to the block labeled 'Content Row'. This is where all the main components live.
6) Click the pencil (edit) icon next to the 'Specialized Type'.
7) Scroll all the way to the bottom of the dropdown to find and click on the button 'Add Item' to add your recently created module. 
8) The new item requires the Value ( the kabob-case name of the file, i.e. training-test). The Label Can be formatted as regular Capitalized text ( Training Test ).
9) Next you will add the necessary fields from the 'Show Fields' drop down.
    example: if the cascade module has a `$heading` variable, that will be 'Content Row/Heading'.
    This allows you to use the heading props and the user can add whatever they want.
10) When done adding variables (?) you will select the save button on the bottom of the data field drop down you are currently in. Do not save at this time using the Submit button on the top. It will not save the work you just did.
11) Once Saved and back on the main data definitions page you may click 'Submit' at the top of the page.
12) You can now test build with your new module in a beta file.
   

 