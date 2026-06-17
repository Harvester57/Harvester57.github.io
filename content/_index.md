---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: |
        Hi, I'm Florian Stosse, just another information security engineer !

        ### Current work

        I currently work at the [European Space Agency](https://www.esa.int/), as a cybersecurity engineer for the Galileo programme, specifically for the [Galileo Mission Segment (GMS)](https://gssc.esa.int/navipedia/index.php/Galileo_Ground_Segment#Galileo_Mission_Segment_(GMS)).

        ### Experience and education summary

        I previously worked at [Safran Data Systems](https://www.safran-group.com/companies/safran-data-systems), in the Space & Communications business unit. I focused on hardening and securing our embedded Windows 7 and 10/11 platforms (Cortex family of TT&C and high data rate receivers), among other cool things :)

        I also completed a three-year apprenticeship at Bureau Veritas' R&D center in La Défense, Paris, in the RAMS department, focusing on software security (static analysis, SDLC), connected/autonomous vehicles security (ISO 21434), and industrial systems security (IEC 62443).
        
        This was done in parallel with my M.Sc in Computer Science (major in cybersecurity, minor in embedded systems) from ESIEA Paris (a top French engineering school, part of the ["Grandes écoles"](https://en.wikipedia.org/wiki/Grande_%C3%A9cole)), from which I graduated in August 2018.

        Do not hesitate to get in touch if you want to chat about these topics (or anything else, really) !
    design:
      spacing:
        # Customize the section spacing. Order is top, right, bottom, left.
        padding: ['0', '0', '40px', '0']
      css_class: dark
      background:
        # Choose colors such as from https://html-color-codes.info
        gradient_start: '#165e80ff'
        gradient_end: '#033a53ff'
        # The gradient angle from 0-360 degrees
        gradient_angle: 180
        # Text color (true=light, false=dark, or remove for the dynamic theme color).
        #text_color_light: true
  - block: resume-experience
    id: experience
    content:
      username: me
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: false
  - block: collection
    id: publication
    content:
      title: Selected publications
      text: ""
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      view: citation
  - block: collection
    id: project
    content:
      title: Personal projects
      text: Here are a selection of projects that I am currently working on (sorry for the AI-slop pictures, I'm very bad at designing cute stuff).
      count: 0
      filters:
        folders:
          - project
    design:
      view: article-grid
      columns: 4
  # - block: collection
  #   id: talks
  #   content:
  #     title: Recent & Upcoming Talks
  #     filters:
  #       folders:
  #         - event
  #   design:
  #     view: article-grid
  #     columns: 1
  # - block: collection
  #   id: news
  #   content:
  #     title: Recent News
  #     subtitle: ''
  #     text: ''
  #     # Page type to display. E.g. post, talk, publication...
  #     page_type: post
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       author: ""
  #       category: ""
  #       tag: ""
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ""
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: date-title-summary
  #     # Reduce spacing
  #     spacing:
  #       padding: [0, 0, 0, 0]
---
