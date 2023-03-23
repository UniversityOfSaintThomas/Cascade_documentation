# Cascade Build

This is the steps you will need to take to build a capricorn cascade module from scratch. This is not a common practice, however the steps will still be helpful when building from a copied module. These steps will start with building in the cascade development environment before being built in production in order to be properly tested.

# Building from Scratch

In OPUS DEV

```

_shared-orion

|__ cms
    |__ formats
        |__ components

```

1) After navigating to 'components' in 'shared_orion', click 'Add Content' located on the top page tool bar next to the site navigation dropdown. 
   - click 'Default' file icon
    - format < >
     - type: 'Velocity'
     - Velocity format file name needs to be kebab-case.
    Example file has been created named 'training test' for reference on formatting new file.

 
# Build from copied file (Suggested)

This is pretty straight forward and usually makes the most sense to do in regards to building.

1) In desired module file ( ex: OPUS DEV/_shared-orion/cms/formats/components), click to highlight the box next to the file you wish to copy.
2) An icon tool bar will appear after clicking the side box. Select the copy icon. A drawer will pop out for you to confirm by clicking the blue 'copy' button in the corner.
3) Click Confirm Copy on Copy assets pop up.
4) Locate created copy. It should have the same name as the original with an additional '1' after the name.
5) Right click the copy name.
6) Click 'More' from the pop up menu. 
7) Click 'Rename' to rename the copied file.
8) You have now created a "new" file to for with. You may go in an clean up the formatting. 

#

# Data Definitions 
 Once the module is built you will have to link it in the data definitions in order to use it.

1) Locate and click 'Manage Site' on the tool bar on the top of the page.
2) scroll to locate the 'data Definitions'  block and click ' Go to Data Definitions'.
3) Scroll down on the next page and click on 'Universal'.
4) In the 'Universal' file, click edit ( pencil icon) in top right corner. This will open up all of the data definitions.
5) Scroll down to the block labeled 'Content Row'. This is where all the main components live.
6) Just below the "Category" and "Show this content row?" wil be a series of dropdown boxes. locate the one titled under which file you built the module, in this example it would be 'Specialized Type'.
7) Click the pencil (edit) icon next to the 'Specialized Type'.
8) Scroll all the way to the bottom of the dropdown to find and click on the button 'Add Item' to add your recently created module. This is how you initiate the module to be used for building. 
9) The new item requires the Value ( the kabob-case name of the file, i.e. training-test). The Label Can be formatted as regular Capitalized text ( Training Test ).
10) Next you will add the necessary fields from the 'Show Fields' drop down.
    example: if the cascade module has a `$heading` variable, that will be 'Content Row/Heading'.
    This allows you to use the heading props and the user can add whatever they want.
11) When done adding variables (?) you will select the save button on the bottom of the data field drop down you are currently in. Do not save at this time using the Submit button on the top. It will not save the work you just did.
12) Once Saved and back on the main data definitions page you may click 'Submit' at the top of the page.
13) You can now test build with your new module in a beta file.

# Shared Fields
Shared fields are used like the variables in the data definition. The difference is that they are all contained in one group to help keep things organized. These groups are what needs to be used if you need to loop through information. 

1) Locate and click 'Manage Site' on the tool bar on the top of the page.
2) scroll to locate the 'Shared Fields' block, which should be just above the 'data definitions' block. Click ' Go to Shared Fields'.
3) To create a new shared field Click '+ Add' near the top right of the page. 
4) select 'Shared Field'
5) Choose 'group' to use all functionality available.
6) Name the shared field something human readable.
7) Select the pencil icon across from the 'group1' to edit the default name. Identifier must be kabob case and will be referenced in the module much like the data definitions. The Label can be Human readable. 
8) From hear you can add whatever you want that you would like to be grouped together.
9) Once you are done building your shared field you can save and go back over to the data definitions page.
    Manage site -> Data Definitions -> Universal -> edit
10) Once in the Universal data definition edit page, scroll down to the very bottom of the page to the last data definition.
11) Select and drag the 'group' icon that looks like a clip board, down to the bottom of the content row box. You will see a line light up. Then let go, creating a new group.
12) This we automatically pop open the 'edit' field for your newly created group.
13) At the top of the edit field there will be a box labeled ' Choose Shared Field', Click on this.
14) Choose your previously created shared field from the asset list that appears.
15) This will auto populate your shared field in the data definitions.
16) Now to attach your shared field to your module, Locate the type drop down again ( 'Specialized Type') and open the edit field. 
17) In your intended module, Locate the new group/shared field in the 'Show Field' dropdown. It will likely be at the very bottom of the list.
18) Now whe you use your module the shared field will be attached.


 