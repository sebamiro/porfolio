+++
title = "get_next_line"
template = "project.html"
weight = 2
description = "get_next_line"
+++

# Get_next_line

Is an individual project about creating a function that returns the next line
from a file descriptor, without knowing its size beforehand.
One of the goal of this project is to learn a highly interesting
concept in C programming: static variables, and to gain a deeper understanding
of allocations, whether they happen on the stack memory or in the heap memory,
the manipulation and the life cycle of a buffer, the unexpected complexity implied
in the use of one or many static variables.
<br><br><br>
```
char*
get_next_line(int fd)
{
	static char	*staticbuf;
	char		*line;

	if (fd < 0 || BUFFER_SIZE <= 0 || read(fd, 0, 0) < 0)
		return (NULL);
	staticbuf = ftread(fd, staticbuf);
	if (!staticbuf)
		return (NULL);
	line = findline(staticbuf);
	staticbuf = nextline(staticbuf);
	return (line);
}
```

<div class="links">

<div>
<a target="blank" href="https://github.com/sebamiro/get_next_line42/">GitHub</a>
</div>
<div>
<a target="blank" href="https://cdn.intra.42.fr/pdf/pdf/90264/en.subject.pdf">Subject</a>
</div>

</div>
