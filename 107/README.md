# KEG Web

* Any **keg** MAY easily be also published as a Web site.
* A keg Web site MUST have an `index.html` page for every `README.md` file.
* Any keg MAY have additional files and directories in its root keg directory.
* A keg for KEG Web SHOULD have a `web` directory containing CSS, JavaScript, etc.
* A **keg app** for KEG Web SHOULD generate `index.html` when `README.md` updated.

The KEG Web refers to using the Web to distribute KEG content. Any Web site can easily double as a keg simply by generating an `index.html` static page every time the `README.md` file is updated. A **keg app** can easily do this as it watches for changes to any nodes because it usually also needs to automatically update the `dex` **last changes index**.

Web users benefit from KEG Web sites because the underlying source of any stylized Web page is always available as raw KEGML markup allowing the user to decide if and how to render that content in a way that is best for them, not dictated by the **content creator**. While Web browsers seek to provide "simplified views" of some sites that qualify, simply requesting the `README.md` file with any Web browser provides the simplest of views.

KEG Web sites also allow redundant copies of different rendered keg forms as well. Content creators may choose to provide a PDF or epub or KEGMLX version of the entire keg that can be easily downloaded with a single command or click allowing KEG Web site users opportunities to store and distribute the keg content in multiple ways. Whether it be a technical manual, series of articles, a text book, academic paper, or novel, KEG Web publishing affords the greatest flexibility. Moreover, publications can be easily authenticated with **content creator authentication and encryption**.
