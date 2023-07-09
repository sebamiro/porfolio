+++
title = "printf"
template = "project.html"
weight = 1
description = "printf"
+++

# PRINTF

Is an individual project about recoding the famous printf C function
into its own library, to learn about variadic functions and improve algorithmic methodology
<br>
<br>
<br>
- %: (% character)
- c: char (character)
- s: char * (string)
- p: void * (pointer's address)
- u: unsigned int (unsigned decimal integer)
- x/X: unsigned int (hexadecimal)
- d/i: int (integer)

```
int
findtype(va_list ap, char c)
{
	if (c == '%')
		return (write(1, "%", 1));
	else if (c == 'c')
		return (handlechar(ap));
	else if (ft_strchr(c, "diuxX"))
		return (handlenbr(ap, c));
	else if (c == 's')
		return (handlestr(ap));
	else if (c == 'p')
		return (handleptr(ap));
	return (-1);
}

```

[GitHub](https://github.com/sebamiro/printf42/)
