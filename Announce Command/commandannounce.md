{
  "name": "announce",
  "permissions": "NONE",
  "restriction": "1",
  "_id": "yqMNU",
  "actions": [
    {
      "comment": "DBM-GDG - Announce Command ",
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
      "comparison": "1",
      "value": "2",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "3",
      "iffalseVal": "2",
      "name": "Check Parameters"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "**Incorrect Command Input**\n\nusage: `!announce Title Message`",
      "storage": "0",
      "varName2": "",
      "iffalse": "0",
      "iffalseVal": "",
      "name": "Send Message"
    },
    {
      "name": "End Action Sequence"
    },
    {
      "info": "0",
      "infoIndex": "1",
      "storage": "1",
      "varName": "embedtitle",
      "name": "Store Command Params"
    },
    {
      "info": "1",
      "infoIndex": "2",
      "storage": "1",
      "varName": "embedmessage",
      "name": "Store Command Params"
    },
    {
      "title": "${tempVars(\"embedtitle\")}",
      "author": "",
      "color": "RANDOM",
      "url": "",
      "authorIcon": "",
      "authorUrl": "",
      "imageUrl": "",
      "thumbUrl": "",
      "timestamp": "false",
      "debug": "false",
      "text": "",
      "year": "",
      "month": "",
      "day": "",
      "hour": "",
      "minute": "",
      "second": "",
      "storage": "1",
      "varName": "embed",
      "name": "Create Embed Message"
    },
    {
      "storage": "1",
      "varName": "embed",
      "message": "${tempVars(\"embedmessage\")}",
      "name": "Set Embed Description"
    },
    {
      "storage": "1",
      "varName": "embed",
      "channel": "0",
      "varName2": "",
      "storage3": "0",
      "varName3": "yourembed",
      "iffalse": "0",
      "iffalseVal": "",
      "name": "Send Embed Message"
    },
    {
      "time": "3",
      "measurement": "1",
      "name": "Wait"
    },
    {
      "channel": "1",
      "varName": "",
      "message": "**Your announcement has been sent to ${msg.channel}**\n\n**Embed:**\n**Title:** ${tempVars(\"embedtitle\")}\n\n**Text:** ${tempVars(\"embedmessage\")}\n\n",
      "storage": "0",
      "varName2": "",
      "iffalse": "0",
      "iffalseVal": "",
      "name": "Send Message"
    }
  ]
}
