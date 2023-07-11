+++
title = "minitalk"
template = "project.html"
weight = 5
description = "minitalk"
+++

# Minitalk

Is an individual project about a small client-server comunication program
through UNIX signals. It's mandatory to use just SIGUSR1 and SIGUSR2 (user defined signals),
so the client program must send the text as a binary message, and the server
keeps a buffer to store the received characters until the complete message is received,
then the server prints it out.

```
void
sendchar(int pid, char c)
{
	int	i = 0;
	int	signal = 0;

	while (i < 8)
	{
		if (c & 128)
			signal = SIGUSR1;
		else
			signal = SIGUSR2;
		if (kill(pid, signal))
			exit(1);
		usleep(100);
		i++;
		c <<= 1;
	}
}
```

<div class="links">

<div>
<a target="blank" href="https://github.com/sebamiro/minitalk42/">GitHub</a>
</div>
<div>
<a target="blank" href="https://cdn.intra.42.fr/pdf/pdf/90288/en.subject.pdf">Subject</a>
</div>

</div>
