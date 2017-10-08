---
title: Get Involved
form:
    name: email-form
    fields:
        - name: honeypot
          type: honeypot
        - name: email
          label: Email
          id: email-field
          type: email
          outerclasses: white-text col s12
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
        - message: Thanks, be on the lookout for some awesome things!
---
