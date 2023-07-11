+++
title = "libft"
template = "project.html"
weight = 0
description = "libft"
+++

# Libft

Is an individual project that requieres to create a C library for future projects,
it has some re-implemented standard C functions, and other non-standar functions.
We get a deeper understanding of data structures and basic algorithms. During the
cursus we are only allowed to use functions that we have programed, so we have to
keep growing this libary with anything we would find useful.

```
char*
ft_strjoin(const char *s1, const char *s2)
{
	size_t	total;
	char	*str;

	total = ft_strlen(s1) + ft_strlen(s2) + 1;
	str = ft_calloc(total, 1);
	if (!str)
		return (NULL);
	ft_strlcat(str, s1, total);
	ft_strlcat(str, s2, total);
	return (str);
}
```

<div class="links">

<div>
<a target="blank" href="https://github.com/sebamiro/libft42/">GitHub</a>
</div>
<div>
<a target="blank" href="https://cdn.intra.42.fr/pdf/pdf/90260/en.subject.pdf">Subject</a>
</div>

</div>
