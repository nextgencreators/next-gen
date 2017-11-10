---
featured_subtext: 'We have some exciting events coming up and we''d love to meet you there!'
other_ways_subtext: 'I told you all this before, when you have a swimming pool, do not use chlorine, use salt water, the healing, salt water is the healing. Watch your back, but more importantly when you get out the shower, dry your back, it’s a cold world out there.'
other_ways:
    -
        name: Volunteer
        description: 'It’s important to use cocoa butter. It’s the key to more success, why not live smooth? Why live rough? We don’t see them, we will never see them. I’m giving you cloth talk, cloth. Special cloth alert, cut from a special cloth. Every chance I get, I water the plants, Lion!'
        url_bottom: /next-gen/get_involved
    -
        name: Join
        description: 'They key is to have every key, the key to open every door. In life you have to take the trash out, if you have trash in your life, take it out, throw it away, get rid of it, major key. The ladies always say Khaled you smell good, I use no cologne. Cocoa butter is the key.'
        url_bottom: /next-gen/get_involved
    -
        name: Subscribe
        description: 'Watch your back, but more importantly when you get out the shower, dry your back, it’s a cold world out there. They will try to close the door on you, just open it. I told you all this before, when you have a swimming pool, do not use chlorine, use salt water, the healing, salt water is the healing. Hammock talk come soon.'
        url_bottom: /next-gen/get_involved
title: 'Get Involved'
form:
    name: email-form
    fields:
        -
            name: honeypot
            type: honeypot
        -
            name: email
            label: Email
            id: email-field
            type: email
            outerclasses: 'white-text col s12'
            validate:
                required: true
    buttons:
        -
            type: submit
            value: Submit
            classes: 'btn waves-effect waves-light'
    process:
        -
            save:
                fileprefix: contact-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            message: 'Thanks, be on the lookout for some awesome things!'
---

