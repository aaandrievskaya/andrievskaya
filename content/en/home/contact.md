---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

  # Contact details (edit or remove options as required)
  email: 1032211699@pfur.ru
  phone: +7 888 888 88 88
  address:
    street: Ordzhonikidze street, 3
    city: RUDN
    region: Moskow
    postcode: '94305'
    country: Russia
    country_code: RUS
  coordinates:
    latitude: '37.4275'
    longitude: '-122.1697'
  directions: Enter house 3 on Ordzhonikidze street, go up to the 3rd floor, turn left and go along the common corridor, then after the toilet go through the door on the left and go down to the 2nd floor. One of the cabinets is needed
  office_hours:
    - 'Monday - Saturday 9:00 to 19:00'
    - 'Sunday is a day off'

design:
  columns: '2'
---
