+++
title = "containers"
template = "project.html"
weight = 9
description = "containers"
+++

# Containers

Is an individual project about implementing the various container
types of the C++ standard template library, in C++98.

- Stack: Container adaptor, use an encapsulated object of a specific
  container class as its underlying container, providing a set of member functions to access its elements. Last-in first-out.
- Vector: Implemented as dynamic arrays with the ability to resize itself automatically when an element is inserted or deleted,
  ith their storage being handled automatically by the container. The elements are stored contiguously, which means that can
  be accessed not only through iterators, but also using offsets to regular pointers to elements.
- Map: Is a sorted associative container that contains key-value pairs with unique keys. Keys are sorted by using the
  comparison function Compare. Search, removal, and insertion operations have logarithmic complexity. Implemented as a Red-Black tree.
- Set: Is container that store unique elements following a specific order. The value of an element also identifies it, cannot be modified once in the container
  (the elements are always const), but they can be inserted or removed from the container.

		├─ Vector
		├─ Map
		├─ Stack
		├─ Set
		├─ utility
		├─ Itreator/
		│  ├─ iterator_traits
		│  ├─ random_access_iterator
		│  └─ reverse_iterator
		├─ RedBlackTree/
		│  ├─ RBT
		│  ├─ RBT_iterator
		└  └─ node

<div class="links">

<div>
<a target="blank" href="https://github.com/sebamiro/ft_containers">GitHub</a>
</div>
<div>
<a target="blank" href="https://cdn.intra.42.fr/pdf/pdf/47323/en.subject.pdf">Subject</a>
</div>

</div>
