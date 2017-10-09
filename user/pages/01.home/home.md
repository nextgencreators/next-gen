---
title: Home
form:
    name: contact
    fields:
        - name: honeypot
          type: honeypot
        - name: name
          label: Full Name
          id: name-field
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true
        - name: email
          label: Email Address
          id: email-field
          type: email
          outerclasses: col s12
          validate:
            required: true
        - name: subject
          label: Subject
          id: subject-field
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true
        - name: message
          label: Message
          id: message-field
          autocomplete: on
          type: text
          outerclasses: col s12
          validate:
            required: true
        
    buttons:
        - type: submit
          value: Submit
          classes: btn waves-effect waves-light
    process:
        - save:
            fileprefix: contact-
            dateformat: Ymd-His-u
            extension: txt
            body: "{% include 'forms/data.txt.twig' %}"
        - message: Thank you for getting in touch!
---
