---
title: Sponsor Form
page_title: Sponsor Us!
form:
    name: sponsor-form
    fields:
        - name: honeypot
          type: honeypot

        - name: Company
          label: Company
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true 

        - name: Contact
          label: Contact
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true

        - name: Address
          label: Address
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true

        - name: State
          label: State
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true

        - name: City
          label: City
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true

        - name: Zipcode
          label: Zipcode
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true

        - name: Phone-number
          label: Phone-number
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true
          id: name

        - name: Email
          label: Email
          type: email
          outerclasses: col s12
          validate:
            required: true
          id: email


    buttons:
        - type: submit
          value: Submit
          classes: btn waves-effect waves-light
        - type: reset
          value: Reset
          classes: btn waves-effect waves-light

    process:
        - email:
            from: "{{ config.plugins.email.from }}"
            to:
              - "{{ config.plugins.email.from }}"
              - "{{ form.value.email }}"
            subject: "[Feedback] {{ form.value.name|e }}"
            body: "{% include 'forms/data.html.twig' %}"
        - save:
            fileprefix: feedback-
            dateformat: Ymd-His-u
            extension: txt
            body: "{% include 'forms/data.txt.twig' %}"
        - message: Thank you for your feedback!
        - display: thankyou

---

