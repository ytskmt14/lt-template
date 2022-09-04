---
# try also 'default' to start simple
theme: seriph
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# persist drawings in exports and build
drawings:
  persist: false
---

# Presentation Title

---
layout: TwoColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="Header" />

::left_column::
left column

::right_column::
right_column
<img src="slidev-logo.png"/>

---
layout: OneColWithHeader
---

::default::
<!-- ./components/ContentHeader -->
<ContentHeader text="Header" />

::content::
<!-- ./components/ContentList -->
<ContentList :items="['item A', 'item B', 'item C']" />
