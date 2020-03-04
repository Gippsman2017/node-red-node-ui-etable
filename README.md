# node-red-node-ui-etable
This node is based on the capabilities of the Tabulator library and allows 
the user to define complex - editable tables and constructs.

Credit must go to Kazuhito Yokoi for his inspiration. node-red-node-ui-table

This node differs from node-red-node-ui-table due to it being more native to
the Tabulator libraries, it allows very complex editable tables to be built, although this means that the configuration of the node now must follow the http://tabulator.info json format.

Eg

Options can be

{
    "movableColumns": true,
    "resizableColumns": true,
    "selectable": 5,
    "responsiveLayout": "collapse",
    "autoResize": true,
    "layout": "fitColumns",
    "pagination": "local",
    "height": "800px",
    "groupBy": "system",
    "groupStartOpen": true
}

Columns can be

[		{title:"Name", field:"name", editor:"input"},
		{title:"Task Progress", field:"progress", align:"left", formatter:"progress", editor:true},
		{title:"Gender", field:"gender", width:95, editor:"select", editorParams:{values:["male", "female"]}},
		{title:"Rating", field:"rating", formatter:"star", align:"center", width:100, editor:true},
		{title:"Color", field:"col", width:130, editor:"input"},
		{title:"Date Of Birth", field:"dob", width:130, sorter:"date", align:"center"},
		{title:"Driver", field:"car", width:90,  align:"center", formatter:"tickCross", sorter:"boolean", editor:true}
]

Pass input data in msg.payload. Note that options and columns can also be passed in via msg. 
msg = {
    payload: ...
    config: {
        options: ...
        columns: ...
    }
}

CallBacks handled are :

        If the cell has editor = true,  a message is sent with "callback : cellEdited" 
        If the cell has editor = false, a message is sent with "callback : cellClick"

