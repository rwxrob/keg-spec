# Determining title of included content

* The **link text** of an **include link** MUST determine the expanded **heading**.
* The **link text** MUST override the **title** of an included **node**.
* The expanded **heading** MUST be disabled if **link text** begins with exclamation point.

Every **node** has a **title**. Every **include** also has a title.

Tools MUST keep the include title (discarding the node title).

All titles MUST be discarded if the **include link text** begins with a exclamation point (`!`).

* [!sample with ignored link titles](kegml-with-ignored-link-titles.md)

Note that the above sample itself is also an example of an **ignored title include link**.

    #kegmlx #kegml
