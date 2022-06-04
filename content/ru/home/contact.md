---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Контакты
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
    street: ул. Орджоникидзе, 3
    city: РУДН
    region: Москва
    postcode: ' '
    country: Россия
    country_code: RUS
  coordinates:
    latitude: '37.4275'
    longitude: '-122.1697'
  directions: Войдите в дом 3 по улице Орджоникидзе, поднимитесь на 3 этаж, поверните налево и пройдите по общему коридору, далее после туалета зайдите в дверь слева и спуститесь на 2 этаж. Один из кабинетов -- нужный
  office_hours:
    - 'Понедельник - Пятница с 9:00 до 19:00'
    - 'Воскресенье - выходной'
      
design:
  columns: '2'
---
