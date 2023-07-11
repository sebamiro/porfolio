+++
title = "minishell"
template = "project.html"
weight = 7
description = "minishell"
+++

# Minishell

Is an group project about creating a basic shell program that allows users
to execute commands, this includes running external programs, built-in commands,
and handling command-line arguments, manage processes, and handle basic shell functionalities as:
- Environment variables, allowing users to set, unset, and modify variables.
- Input/Output redirection, allowing users to redirect the standard input and
  output of commands to files or other commands.
- Pipes (| character), the output of each command in the pipeline is
  connected to the input of the next command via a pipe.

```
int
ft_echo(t_cmd **cmd)
{
	int	i = 0;
	bool n_flag = false;

	if (!(*cmd)->arg && write(1, "\n", 1))
		return (0);
	while ((*cmd)->arg[i] && is_n_flag((*cmd)->arg[i])) {
		n_flag = true;
		i++;
	}
	while ((*cmd)->arg[i]) {
		putstr((*cmd)->arg[i]);
		if ((*cmd)->arg[i])
			write(1, " ", 1);
		i++;
	}
	if (!n_flag)
		write(1, "\n", 1);
	return (0);
}
```

<div class="links">

<div>
<a target="blank" href="https://github.com/sebamiro/Minishell">GitHub</a>
</div>
<div>
<a target="blank" href="https://cdn.intra.42.fr/pdf/pdf/90309/en.subject.pdf">Subject</a>
</div>

</div>
