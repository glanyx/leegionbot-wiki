# LeegionBot
LeegionBot is the official Discord bot for the LeeandLie Patreon Army Discord server.

## Function Distribution
Commands for LeegionBot are divided into several subsets.

- Basic User Commands
- Special Leegion Commands
- Elevated Permission Commands
- Bot Owner Commands

All commands are prefixed with `lb!`.

## Basic User Commands
Basic User Commands are basic commands that everyone has access to. A full list of available commands can be found below.

### === About ===
**Construction**
`lb!about`

**Usage**
Returns and embedded message containing LeeandLie's biography.

### === Links ===
**Construction**
`lb!links`

**Usage**
Returns an embedded message containing several links to LeeandLie's website, merchandise store and social media sites.

### === Who ===
**Construction**
`lb!who [user]`

Where: [user] is a mentioned user.

**Usage**
Returns an embedded message containing basic information about the [user] (Example: `lb!who @Xaladon#0001`).

### === Stats ===
**Construction**
`lb!stats`

**Usage**
Returns a list of statistics related to the current server.

### === Tiers ===
**Construction**
`lb!tiers [tier]`

Where: [tier] is an available Patreon tier.

**Usage**
Returns an embedded message containing the list of available tiers on Patreon. Appending a specific [tier] will return information on that specific tier and corresponding rewards (E.G. `lb!tiers Lieutenant`).

### === Roll ===
**Construction**
`lb!roll [Optional:limit]`

Where: [limit] is any positive number.

**Usage**
Rolls a random number between 1 and 100 (default). If a [limit] has been specified, a random number between 1 and [limit] will be returned.

### === Ping ===

**Construction**
`lb!ping`

**Usage**
Checks the delay between client and server and posts the response time in milliseconds.

### === Help ===
**Construction**
`lb!help`

**Usage**
Sends a help message to requester over Direct Messages. Only the bot owner can send help information to others.

## Special Leegion Commands
Special Leegion Commands are unique in the way that they add value to a Leegion specific event or behaviour.

### === Suggestion Add ===
**Construction**
`lb!suggestion add [your suggestion]`
`lb!sg add [your suggestion]`

Where: [your suggestion] is a suggestion formed of any string of characters.

**Usage**
Create a suggestion for the server to upvote or downvote and for the moderator team to review. The suggestion will be posted in the Suggestions channel. Suggestions should be in regards to and of benefit to the Discord server or the Leegion as a whole.

### === Suggestion Edit ===
**Permissions Required**
Suggestion Author, Manage Roles or Bot Owner

**Construction**
`lb!suggestion edit [Suggestion ID] [your suggestion]`
`lb!sg edit [Suggestion ID] [your suggestion]`

Where: [Suggestion ID] is the ID assigned to your suggestion in the Suggestions channel on Discord.
Where: [your suggestion] is a suggestion formed of any string of characters.

**Usage**
Allows you to edit an existing Suggestion. You can only edit Suggestions created by yourself and only when they have not yet been processed by a moderator. Moderators can always edit any Suggestion.

### === Livechat ===
**Permissions Required**
Manage Roles or Bot Owner

**Construction**
`lb!livechat [start / end]`

**Usage**
Starts or ends the Lieutenant tier and up Livechat on Discord. Role permissions are changed to allow access to the Patreon Livechat Voice Channel and an announcement is made to the Livechat Text channel on start. With the end attribute the permissions are denied and another announcement is made to the Lieutenant channel.

All users will be forceably muted when the Livechat starts.

### === Livechat Mute ===
**Permissions Required**
Manage Roles or Bot Owner

**Construction**
`lb!livechat [mute / unmute]`

**Usage**
Mutes or Unmutes all relevant roles part of the Livechat Voice Channel.

## Elevated Permission Commands
This set of commands all require specific server rights within the Discord server. Commands in this set are generally related to server management.

### === Mute ===
**Permissions Required**
(Manage Roles and Mute Voice Users) or Bot Owner

**Construction**
`lb!mute [user]`

Where: [user] is a mentioned user.

**Usage**
Will assign the LeegionMute role to a user that prevents a them from speaking in both Text and Voice channels. If the role does not yet exist it will be created.

### === Kick ===
**Permissions Required**
Kick Users or Bot Owner

**Construction**
`lb!kick [user] [Optional:reason]`

Where: [user] is a mentioned user.

Where: [reason] is an optional string of text.

**Usage**
Will kick the mentioned user from the server using the standard Discord kick feature. If a reason is provided it will be passed along to the standard kick feature.

### === Ban ===
**Permissions Required**
Ban Users or Bot Owner

**Construction**
`lb!kick [user] [Optional:reason]`

`lb!kick [user] [Optional:deletionDays]`

`lb!kick [user] [Optional:deletionDays] [Optional:reason]`

Where: [user] is a mentioned user.

Where: [deletionDays] is the amount of days the mentioned user's messages will be deleted for.

Where: [reason] is an optional string of text.

**Usage**
All specified constructions are valid. The mentioned user will be banned from the server through the standard Discord functionality. Should a [deletionDays] be provided, this will be a temporary softban. If a reason is provided it will be passed along to the standard ban feature.

### === Nickname ===
**Permissions Required**
Manage Nicknames or Bot Owner

**Construction**
`lb!nick [user] [nickname]`

Where: [user] is a mentioned user.

Where: [nickname] is a new specified name for the mentioned user.

**Usage**
This will change the mentioned user's visible and discriminated name on the server.

### === Nickname Reset ===
**Permissions Required**
Manage Nicknames or Bot Owner

**Construction**
`lb!nickr [user]`

Where: [user] is a mentioned user.

**Usage**
This will revert any changes made to the mentioned user's name.

## Bot Owner Commands
Lastly, this set of commands is only available to the owner of the bot. These are only commands for bot control.

### === Status ===
**Permissions Required**
Bot Owner

**Construction**
`lb!status [status]`

Where: [user] is a string of text.

**Usage**
This will change the bot's playing status.

### === Test ===
**Permissions Required**
Bot Owner

**Construction**
`lb!test`

**Usage**
Checks that the bot is active and returns the current server ID.

### === Help ===
**Construction**
`lb!help [Optional:recipient]`

Where [recipient] is a mentioned user.

**Usage**
Sends a help message to requester over Direct Messages. If a [recipient] has been specified, the help message will be sent to [recipient] instead (E.G. `lb!help @Xaladon#0001`). Only the bot owner can send help information to others.
