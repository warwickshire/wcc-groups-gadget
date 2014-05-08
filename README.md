WCC Group Gadget
=================

The source XML file is a Gmail sidebar gadget used to launch the WCC Group application.
This allow easy access to the Groups lookup from the sidebar.

![enter image description here][1]

The XML file consists of two sections. First the 'ModulePrefs' which contains the details of the gadget that will be displayed when it is added to Gmail. The dynamic-height is useful here so the gadget can expand vertically.

<pre>
    title="WCC Sidebar" 
    directory_title="WCC Sidebar" 
    description="Sidebar gadget for links to WCC resources" 
    author="Warwickshire County Council" 
    author_email="email_address" 
    author_affiliation="WCC" 
    author_location="UK" title_url="http://www.warwickshire.gov.uk/" 
    screenshot="https://wcc-groups-gadget.googlecode.com/git/wcc_ss.PNG" 
    thumbnail="https://wcc-groups-gadget.googlecode.com/git/wcc_thumb.PNG" 
    category="Email" 
    category2="Utilities" 
    height="100"
    Require feature="dynamic-height"    
</pre>

The second section '<Content type="html">' is for, in this case, the HTML code that will render the gadget. Be aware you are working within a strict container with limited width. Use CDATA to surround the HTML code to avoid it getting parsed as XML.

To use and deploy, follow these steps

1. Copy the XML file and host it publically accesible
2. Modify the top section details
3. Add links to the application you want to lanuch
4. Go to Gmail settings and first enable the lab 'Add any gadget by URL'
5. Go to the gadgets tab and add the path to the hosted XMl file

  [1]: https://raw.githubusercontent.com/warwickshire/wcc-groups-gadget/master/wcc_groups_gadget.png