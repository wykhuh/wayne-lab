+++
# This section displays projects from `content/projects/` which have
# `featured = true`.

widget = "featured"
headless = true
active = true
weight = 30

title = "Projects"
subtitle = ""

[content]
  # Page type to display. E.g. post, talk, or publication.
  page_type = "projects"

  # Choose how much pages you would like to display (0 = all pages)
  count = 0

  # Page order. Descending (desc) or ascending (asc) date.
  order = "desc"

  # Filter posts by a taxonomy term.
  [content.filters]
    tag = ""
    category = ""
    publication_type = ""

[design]
  # Toggle between the various page layout types.
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   4 = Citation (publication only)
  view = 3

+++
