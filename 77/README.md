# Node include link

* The **link target** of a **node include link** MUST be a **node ref**.
* The **link text** of a node include link MUST be a valid **title**.
* A **keg app** MUST examine link target for special codes.

Given the following **include link**:

```kegml
* [Some Lede.](/23?L)
```

And, given the following **node** **README.md** file with ID of 23:

```kegml
# This is something.

This is the first paragraph block of the node with ID 23 that has had its title replaced with "Some Lede." because of the initial star noticed at the beginning of the include link text.
```

KEGMLX expansion produces the following with a **lede span** combined with the first paragraph:

```kegmlx
***Some Lede.*** This is the first paragraph block of the node with ID 23 that has had its title replaced with "Some Lede." because of the initial star noticed at the beginning of the include link text.
```

If the content of *node* 23 was anything but a paragraph, such as the following:

```kegml
# This is something in a list.

1. One
1. Two
```

Then, the **lede span** would become its own paragraph block:

```kegmlx

***Some Lede.***

1. One
1. Two
```
