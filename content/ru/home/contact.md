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
  email: test@example.org
  phone: 888 888 88 88
  address:
    street: 450 Serra Mall
    city: Стэнфорд
    region: CA
    postcode: '94305'
    country: США
    country_code: US
  coordinates:
    latitude: '37.4275'
    longitude: '-122.1697'
  directions: Войдите в здание 1 и поднимитесь по лестнице в офис 200 на этаже 2
  office_hours:
    - 'Понедельник с 10:00 до 13:00'
    - 'Среда с 09:00 до 10:00'
  appointment_url: 'https://calendly.com'
  contact_links:
    - icon: twitter
      icon_pack: fab
      name: DM Me
      link: 'https://twitter.com/Twitter'
    - icon: video
      icon_pack: fas
      name: Zoom Me
      link: 'https://zoom.com'

design:
  columns: '2'
---
