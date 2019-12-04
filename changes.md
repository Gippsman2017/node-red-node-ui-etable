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
