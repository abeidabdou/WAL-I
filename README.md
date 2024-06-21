![WAL-I](https://github.com/abeidabdou/WAL-I/blob/fd2be38b24b161884e3adb205112836f950f624d/DrawKit%20Vector%20Illustration%20Animal%20%26%20Pets%20(21).png)
# WAL-I

**WAL-I is a friendly Discord bot powered by AI and the Discord API, designed to assist you and your moderators by understanding and responding to commands in plain, everyday language.**

> Welcome to the shortest documentation you'll ever read!  
> Before starting, watch the video to understand more about what you will be reading.

## What Can WAL-I Do?

### Commands

Since WAL-I doesn't use any specific command to perform actions but relies on natural language, we will go through examples.

#### 1. Deleting Messages

WAL-I can delete messages based on various criteria: by user, keywords, links, attachments, time intervals, and message IDs. Deletion can also be scoped to specific channels or all channels for server owners.

**1.1 Deleting Messages by ID:**

```diff
- "message: Delete this message to ensure privacy. 32109876"
- "message: WAL-I, this message needs to be removed, 23424234, 32109876, user doesn't respect the rules"
```

**1.2 Deleting Messages by Channel:**

```diff
- "message: delete the last 30 messages in test"
- "message: delete the last 20 messages"
```
_(WAL-I assumes the current channel if none is specified)_

```diff
- "message: delete the last 20 messages sent here"
- "message: delete the last 50 messages in all channels" _(Server owner only)_
```

**1.3 Deleting Messages by Interval:**

```diff
- "message: Delete the 10 messages sent before 23423424532 in test"
- "message: delete the last 10 messages sent after 2375672242"
- "message: delete the messages sent after 2375672242 and before 23423424532 in channel test"
- "input: delete the messages sent between 2375672242 and 23423424532 in channel test"
```
_(WAL-I determines the before and after IDs automatically)_

**1.4 Deleting Messages with Attachments:**

```diff
- "message: delete all messages with link"
- "message: delete any message with an image in channel test"
```

**1.5 Deleting Messages with Specific Words or Keywords:**

```diff
- "message: Delete any message containing this emoji 🫡"
```

**1.6 Deleting Messages by Users:**

```diff
- "message: delete the last 10 messages Ali sent"
- "message: delete the last 10 messages Ali sent in test"
- "message: delete the last 10 messages I sent in channel test"
- "message: delete the last 10 messages I sent in all channels"
```
_(Server owner only)_

```diff
- "message: Delete the 20 messages Ali sent before 23423424532 in channel test"
- "message: delete messages sent by Ali after 23453534536 and before 23423424532"
- "message: delete messages with stp in channel test sent by Ali before this message 23453534536"
```

**Combining Criteria:**

```diff
- "message: Delete messages sent by Ali and Sam containing trip"
- "message: delete messages sent between 2am and 5pm"
```
_(WAL-I uses the international timezone)_

**Important Notes:**

```diff
! Specificity is key.
! Only a server owner can delete messages in all channels simultaneously.
! If no limit is provided, the default limit is 5 messages for everyone else and none for server owners.
! No limit is needed when using before and after criteria.
! Server owners can delete messages using date and time across all channels.
! Moderators cannot delete messages using date and time.
! A reason must be provided for all deletions.
```

WAL-I provides targeted message deletion capabilities with an emphasis on specificity. If it can't fulfill a request, it will notify you.

#### 2. Moderation Actions

WAL-I can ban, kick, timeout, mute, and unmute one or multiple users.

```diff
- "message: WAL-I ban Amy"
- "message: WAL-I ban Amy, Samy, and Ali"
```

#### 3. Role Permissions

WAL-I can assign role permissions in a channel (server owner only).

```diff
- "message: WAL-I let everyone send messages in test"
```
_(This grants @everyone the permission to send messages in channel test)_

### Modules

Currently, WAL-I offers a module that allows mods to delete messages, ban, kick, timeout, and mute without needing additional permissions. To create a mod:

1. Invoke the command: `WAL-I create mod`.
2. Specify the user, the number of bans, kicks, timeouts, and messages they can delete.
3. The user will be assigned a `WAL-I mod` role, granting them the ability to use WAL-I commands.
4. Adjust their limits or reset their stats as needed.

Removing a mod is as simple as removing the `WAL-I mod` role or deleting their stats message.

**Disclaimer:**

```diff
! WAL-I does not store mod stats in a database. Deleting the stats message will permanently remove the data.
! WAL-I retains request context for 5 minutes after the last request.
```

If you have more questions, join our [Discord server](#).

## Subscribe and Add WAL-I to Your Server

The subscription fee is $5.
