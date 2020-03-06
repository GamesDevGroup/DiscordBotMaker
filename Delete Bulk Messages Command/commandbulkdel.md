{
  "name": "delmsgs",
  "permissions": "NONE",
  "restriction": "1",
  "_id": "HmpMh",
  "actions": [
    {
      "comment": "DBM-GDG - Delete Messages Command",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "storage": "0",
      "varName": "",
      "name": "Delete Message"
    },
    {
      "condition": "0",
      "comparison": "0",
      "value": "1",
      "iftrue": "3",
      "iftrueVal": "4",
      "iffalse": "0",
      "iffalseVal": "",
      "name": "Check Parameters"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "Usage: `!delmsgs [ammount]` \n**YOU CAN ONLY DELETE MESSAGES UNDER 2 WEEKS**",
      "storage": "1",
      "varName2": "usageerror",
      "iffalse": "0",
      "iffalseVal": "",
      "name": "Send Message"
    },
    {
      "time": "3",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "usageerror",
      "name": "Delete Message"
    },
    {
      "name": "End Action Sequence"
    },
    {
      "info": "0",
      "infoIndex": "1",
      "storage": "1",
      "varName": "deleteammount",
      "name": "Store Command Params"
    },
    {
      "channel": "0",
      "count": "${tempVars(\"deleteammount\")}",
      "condition": "0",
      "custom": "",
      "varName": "",
      "name": "Delete Bulk Messages"
    },
    {
      "time": "3",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "🔧 ${tempVars(\"deleteammount\")} Were Deleted By ${member} 🔧",
      "storage": "1",
      "varName2": "completemsg",
      "iffalse": "0",
      "iffalseVal": "",
      "name": "Send Message"
    },
    {
      "time": "15",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "storage": "1",
      "varName": "completemsg",
      "name": "Delete Message"
    },
    {
      "name": "End Action Sequence"
    }
  ]
}