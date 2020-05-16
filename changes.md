
V 1.0.3 Bump version for npmjs update issue
v 1.0.2	fixed emits not allowing table updates to browser added emitOnlyNewValues: false on widget startup

v.1.0.1 DYNAMIC ETables are now possible.
	msg.config.options and msg.config.columns are now configurable at runtime, this means that it is now possble to change the displayed tables based on button
	clicks or editable fields....on the fly !!	

v 0.1.5 Pull request by wisniaklo to add cellEdited, so, a new parameter is now added to indicate the callback.
        If the cell has editor = true,  a message is sent with "callback : cellEdited" 
	If the cell has editor = false, a message is sent with "callback : cellClick"

v 0.1.4 Allow specifying editor "position" for "select". this should be specified as part of editorParams: editorParams.position
  values are "top"(default), "center" / "middle" or 'bottom'
  
      {
        "title": "Event Type",
        "field": "eventType",
        "editor": "select",
        "width": "5%",
        "editorParams": {
            "values": [
                "PLANNED",
                "UNPLANNED"
            ],
            "position": "top"
        }
    } 
  
v 0.1.3 Initial release
