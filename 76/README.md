# Ignored title include link

* An **include link** MUST NOT produce a **heading** if first **rune** of **link text** is an exclamation point (`!`).

* [!sample with ignored link titles](kegml-with-ignored-link-titles.md)

Note that the above sample itself is also an example of an **ignored title include link** and was included using the following KEGML markup:

```kegml
* [!sample with ignored link titles](kegml-with-ignored-link-titles.md)
```

Here's the content of `some-file.txt`:

* [!sample text file that gets included without](some-file.txt)

When **expanded** that sample produces the following KEGMLX markup:

~~~kegmlx
Include link with ignored titles below:

```txt
This is just some file.
```
~~~

Note how the suffix of the file is automatically assigned to the **fenced** **class**.

    tags: [kegml, kegmlx]
