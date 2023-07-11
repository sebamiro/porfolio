+++
title = "push_swap"
template = "project.html"
weight = 4
description = "push_swap"
+++

# Push_swap

Is an individual project about creating an algorithm that efficiently sorts
a stack of integers in ascending order using only a specific set of operations
<br><br>

There are two stacks: Stack A and Stack B, initially, all the numbers to be sorted
are in Stack A, while Stack B is empty. Operations allowed on the stacks are limited:

		sa:   swaps the 2 top elements of stack a
		sb:   swaps the 2 top elements of stack b
		ss:   both sa and sb
		pa:   moves the top element of stack b at the top of stack a
		pb:   moves the top element of stack a at the top of stack b
		ra:   shifts all elements of stack a from bottom to top
		rb:   shifts all elements of stack b from bottom to top
		rr:   both ra and rb
		rra:  shifts all elements of stack a from top to bottom
		rrb:  shifts all elements of stack b from top to bottom
		rrr:  both rra and rrb

The algorithm needs to be efficient, aiming for the smallest number of steps (operations) possible,
taking into account edge cases and error handling.

<div class="links">

<div>
<a target="blank" href="https://github.com/sebamiro/push_swap42/">GitHub</a>
</div>
<div>
<a target="blank" href="https://cdn.intra.42.fr/pdf/pdf/90284/en.subject.pdf">Subject</a>
</div>

</div>
