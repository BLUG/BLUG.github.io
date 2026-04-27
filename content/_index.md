---
title: Bergen Linux User Group
type: landing

sections:
  - block: cta-image-paragraph
    id: about
    content:
      items:
        - title: Bergen Linux User Group
          image: blug_logo.png
          text: |
            BLUG er en Brukergruppe for GNU/Linux, BSD og annen fri programvare i Bergen. Her møtes folk som jobber med GNU/Linux og BSD til daglig, entusiaster og andre som har interesse for fri programvare.

            BLUG er støttet av næringslivet og privatpersoner i Bergen gjennom Organisasjonen for Fremme av Fri Programvare i Bergen og Omegn.

            BLUG har tradisjonelt hatt møter med foredrag siste torsdag i måneden, men det har vært lite aktivitet de siste årene. Vi ønsker å starte opp igjen med månedlige møter.

            Ellers møtes vi hver torsdag på Henrik for å prate om løst og fast.


  - block: collection
    id: events
    content:
      title: Foredrag og Møter
      count: 10
      filters:
        folders:
          - events
    design:
      view: date-title-summary

  - block: collection
    id: publications
    content:
      title: Siste presentasjoner
      count: 10
      filters:
        folders:
          - publication
    design:
      view: citation

  - block: collection
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
    design:
      view: card

  - block: features
    id: medlemmer
    content:
      title: Blogger og prosjekter
      text: Fra våre medlemmer
      items:
        - icon: hero/globe-alt
          description: "[bsdly.blogspot.com](https://bsdly.blogspot.com) — BSD, nettverkssikkerhet og e-postinfrastruktur. Forfatter av *The Book of PF*."
        - icon: hero/book-open
          description: "[The Book of PF](https://nostarch.com/book-of-pf-4e) — Peter N.M. Hansteens bok om PF-brannmuren, nå i 4. utgave."
        - icon: hero/globe-alt
          description: "[blog.elzapp.com](https://blog.elzapp.com)"

  - block: contact-info
    id: contact
    content:
      title: Contact
      visit_title: "Møt oss"
      email: blug@blug.linux.no
      address:
        lines:
          - "Vi møtes hver torsdag kveld (fra ca kl 19) på Henrik Øl og Vinstue for samtaler og god drikke"
      social:
        - icon: brands/mastodon
          url: https://cyberplace.social/@blug
        - icon: brands/facebook
          url: https://www.facebook.com/BergenLUG/
        - icon: brands/github
          url: https://github.com/BLUG
---
