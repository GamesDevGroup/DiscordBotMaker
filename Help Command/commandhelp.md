{
  "name": "help",
  "permissions": "NONE",
  "restriction": "1",
  "_id": "QdDKC",
  "actions": [
    {
      "comment": "DBM-GDG - help Embed ",
      "color": "#ff8000",
      "name": "Comment"
    },
    {
      "condition": "0",
      "comparison": "1",
      "value": "1",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "3",
      "iffalseVal": "2",
      "name": "Check Parameters"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "**${server} Help System**\n\nusage `!help [Topic]` Ex. `!help commands`\n\n**Topics**\n\nCommands\nSupport",
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
      "varName": "topicname",
      "name": "Store Command Params"
    },
    {
      "storage": "1",
      "varName": "topicname",
      "comparison": "1",
      "value": "\"commands\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "3",
      "iffalseVal": "2",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "**Commands Help**\nThese are the commands available:\n\ncommand1: this is command 1\ncommand2: this is number 2\ncommand3: and what you know, obviously its #3",
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
      "storage": "1",
      "varName": "topicname",
      "comparison": "1",
      "value": "\"support\"",
      "iftrue": "0",
      "iftrueVal": "",
      "iffalse": "3",
      "iffalseVal": "2",
      "name": "Check Variable"
    },
    {
      "channel": "0",
      "varName": "",
      "message": "**Support Help**\nThese are the support commands available:\n\nsupportcommand1: this is command 1\nsupportcommand2: this is number 2\nsupportcommand3: and what you know, obviously its #3",
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
      "channel": "0",
      "varName": "",
      "message": "**${server} Help System**\n\nThere is no topic by that name.\n\n**Topics**\n\nCommands\nSupport",
      "storage": "0",
      "varName2": "",
      "iffalse": "0",
      "iffalseVal": "",
      "name": "Send Message"
    }
  ]
}
