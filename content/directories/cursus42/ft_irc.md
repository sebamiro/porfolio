+++
title = "irc"
template = "project.html"
weight = 9
description = "irc"
+++

# IRC

Is an group project about creating a small IRC server in C++98, that can be used with a
real IRC client to chat, create chat rooms, send private messages to one or multiple users,
via TCP connection.
<br><br>
Command list:
- PASS: Set a 'connection password'.
- NICK: Set or change user's nickname.
- USER: Set username, hostname and realname at the beginning of connection.
- MODE: Set or removes users or channels options.
- QUIT: Terminate a client session.
- JOIN: Request access to the given channel/s.
- PART: Remove user from the given channel/s.
- TOPIC: Change or view the topic of a channel.
- KICK: Request the forced removal of a user from a channel.
- PRIVMSG: Send private messages to other users or channels.

```
void
ft_irc::Server::quit(ft_irc::Client &client, const ft_irc::Parser::cmd_t *cmd)
{
	LOG_INFO("quit: " << client.getNickname() << " leaving")
	client.sendMsg("ERROR :Leaving Server");
	if (!cmd->args.empty()) {
		LOG_TRACE("quit: Reason: " << cmd->args.front())

		this->deleteClient(client.getFd(), cmd->args.front());

		return;
	}
	LOG_TRACE("quit: No reason")
	this->deleteClient(client.getFd());
}	// Server::quit
```

<div class="links">

<div>
<a target="blank" href="https://github.com/sebamiro/ft_irc">GitHub</a>
</div>
<div>
<a target="blank" href="https://cdn.intra.42.fr/pdf/pdf/84865/en.subject.pdf">Subject</a>
</div>

</div>
