---
title: Inhalte zur GitHub Pages-Website mit Jekyll hinzufügen
intro: 'Du kannst Du Deiner Jekyll-Website auf {{ site.data.variables.product.prodname_pages }} eine neue Seite oder einen neuen Beitrag hinzufügen.'
product: '{{ site.data.reusables.gated-features.pages }}'
redirect_from:
  - /articles/adding-content-to-your-github-pages-site-using-jekyll
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

Personen mit Schreibberechtigungen für ein Repository können mit Jekyll Inhalte zu einer {{ site.data.variables.product.prodname_pages }}-Website hinzufügen.

### Informationen zu Inhalten von Jekyll-Websites

Bevor Du Inhalte zu einer Jekyll-Website auf {{ site.data.variables.product.prodname_pages }} hinzufügen kannst, musst Du eine Jekyll-Website erstellen. Weitere Informationen findest Du unter „[Eine {{ site.data.variables.product.prodname_pages }}-Website mit Jekyll erstellen](/articles/creating-a-github-pages-site-with-jekyll).“

Die hauptsächlichen Arten von Inhalten für Jekyll-Websites sind Seiten und Beiträge. Eine Seite wird für eigenständige Inhalte genutzt, die nicht mit einem bestimmten Datum verknüpft sind, z. B. eine Seite mit Informationen zu Deiner Person oder Organisation. Die standardmäßige Jekyll-Website enthält eine Datei mit dem Namen `about.md`, die als Seite Deiner Website unter `YOUR-SITE-URL/about` angezeigt wird. Du kannst den Inhalt dieser Datei bearbeiten, um Deine Informationsseite zu personalisieren. Die Informationsseite kannst Du außerdem als Vorlage für neue Seiten verwenden. Weitere Informationen findest Du unter „[Pages](https://jekyllrb.com/docs/pages/)“ (Seiten) in der Jekyll-Dokumentation.

Bei einem Beitrag handelt es sich um einen Blog-Beitrag. Die standardmäßige Jekyll-Website enthält ein Verzeichnis mit dem Namen `_posts`, das eine Standard-Beitragsdatei enthält. Du kannst den Inhalt dieses Beitrags bearbeiten und den Standardbeitrag als Vorlage für neue Beiträge verwenden. Weitere Informationen findest Du unter „[Posts](https://jekyllrb.com/docs/posts/)“ (Beiträge) in der Jekyll-Dokumentation.

Dein Design umfasst standardmäßige Layouts, Includes und Stylesheets, die automatisch auf neue Seiten und Beiträge auf Deiner Website angewendet werden. Du kannst diese Standardeinstellungen aber überschreiben. Weitere Informationen findest Du unter „[Informationen zu {{ site.data.variables.product.prodname_pages }} und Jekyll](/articles/about-github-pages-and-jekyll#themes).“

{{ site.data.reusables.pages.about-front-matter }}

{{ site.data.reusables.pages.test-locally }}

### Eine neue Seite zu Deiner Website hinzufügen

{{ site.data.reusables.pages.navigate-site-repo }}
{{ site.data.reusables.pages.navigate-publishing-source }}
3. Erstelle im Root-Verzeichnis Deiner Veröffentlichungsquelle eine neue Datei für Deine Seite mit dem Namen _PAGE-NAME.md_, und ersetze dabei _PAGE-NAME_ durch einen aussagekräftigen Dateinamen für die Seite.
4. Füge den folgenden YAML-Frontmatter oben in der Datei hinzu, und ersetze dabei _PAGE TITLE_ durch den Titel der Seite und _URL-PATH_ durch den gewünschten Pfad für die URL der Seite. Wenn beispielsweise die Basis-URL Deiner Website `https://octocat.github.io` lautet und der URL-Pfad (_URL-PATH_) `/about/contact/` ist, findet sich Deine Seite unter `https://octocat.github.io/about/contact`.
  ```shell
  layout: page
  title: "<em>PAGE TITLE</em>"
  permalink: /<em>URL-PATH</em>/
  ```
5. Füge unterhalb des Frontmatter den Inhalt für Deine Seite hinzu.
{{ site.data.reusables.files.write_commit_message }}
{{ site.data.reusables.files.choose-commit-email }}
{{ site.data.reusables.files.choose_commit_branch }}
{{ site.data.reusables.files.propose_file_change }}

### Einen neuen Beitrag zu Deiner Website hinzufügen

{{ site.data.reusables.pages.navigate-site-repo }}
{{ site.data.reusables.pages.navigate-publishing-source }}
3. Navigiere zum Verzeichnis `_posts`.
4. Erstelle eine neue Datei mit dem Namen _YYYY-MM-DD-NAME-OF-POST.md_, wobei Du _YYYY-MM-DD_ durch das Datum des Beitrags und _NAME-OF-POST_ durch den Namen des Beitrags ersetzt.
4. Füge den folgenden YAML-Frontmatter oben in der Datei hinzu, und ersetze dabei _POST TITLE_ durch den Titel des Beitrags, _YYYY-MM-DD hh:mm:ss -0000_ durch das Datum und die Uhrzeit für den Beitrag und _CATEGORY-1_ und _CATEGORY-2_ durch so viele Kategorien, wie Dein Beitrag aufweisen soll.
  ```shell
  layout: page
  title: "<em>POST TITLE</em>"
  date: </em>YYYY-MM-DD hh:mm:ss -0000</em>
  categories: <em>CATEGORY-1</em> <em>CATEGORY-2</em>
  ```
5. Füge unterhalb des Frontmatters den Inhalt für Deinen Beitrag hinzu.
{{ site.data.reusables.files.write_commit_message }}
{{ site.data.reusables.files.choose-commit-email }}
{{ site.data.reusables.files.choose_commit_branch }}
{{ site.data.reusables.files.propose_file_change }}

### Nächste Schritte:

{{ site.data.reusables.pages.add-jekyll-theme }} Weitere Informationen findest Du unter „[Ein Design zu Deiner {{ site.data.variables.product.prodname_pages }}-Website mit Jekyll hinzufügen](/articles/adding-a-theme-to-your-github-pages-site-using-jekyll).“