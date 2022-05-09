## Object-relational mapper
Deﬁne your data models entirely in Python. You get a rich, dynamic database-access API for free — but you can still write SQL if needed.
## URLs and views
A clean, elegant URL scheme is an important detail in a high-quality web application. Django encourages beautiful URL design and doesn’t put any cruft in URLs, like .php or .asp.

To design URLs for an application, you create a Python module called a URLconf. Like a table of contents for your app, it contains a simple mapping between URL patterns and your views.

## Templates
Django’s template language is designed to strike a balance between power and ease. It’s designed to feel comfortable and easy-to-learn to those used to working with HTML, like designers and front-end developers. But it is also flexible and highly extensible, allowing developers to augment the template language as needed.

## Forms
Django provides a powerful form library that handles rendering forms as HTML, validating user-submitted data, and converting that data to native Python types. Django also provides a way to generate forms from your existing models and use those forms to create and update data.

## Authentication
Django comes with a full-featured and secure authentication system. It handles user accounts, groups, permissions and cookie-based user sessions. This lets you easily build sites that allow users to create accounts and safely log in/out.

## Admin
One of the most powerful parts of Django is its automatic admin interface. It reads metadata in your models to provide a powerful and production-ready interface that content producers can immediately use to start managing content on your site. It’s easy to set up and provides many hooks for customization.


## Internationalization
Django offers full support for translating text into different languages, plus locale-specific formatting of dates, times, numbers, and time zones. It lets developers and template authors specify which parts of their apps should be translated or formatted for local languages and cultures, and it uses these hooks to localize web applications for particular users according to their preferences.


## Security
Django provides multiple protections against:

Clickjacking
Cross-site scripting
Cross Site Request Forgery (CSRF)
SQL injection
Remote code execution


#  How Django Works Behind the Scenes
Last updated: December 16, 2019

Django is a Python-based web framework used by millions of developers and billions of consumers through popular apps like Instagram. It is open source, meaning the code is available for free on Github and can be downloaded onto any developer’s computer and used alongside the official documentation. However, I find that even professional Django developers have little insight into “how” Django is actually run, both technically and legally/financially, so this post is my attempt to provide a concise overview of it all.

Django was originally developed at the Lawrence Journal-World newspaper by Adrian Holovaty, Simon Willison, and Jacob Kaplan-Moss. The code was open-sourced in 2005 and developers immediately started making contributions to the codebase. Fourteen years later, Django remains under active development, with new major releases every nine months, minor security releases almost monthly, an official issue tracker, and robust discussion on the django-developers Google group.

As with all open source projects, the two major issues that crop up are funding and control. Let’s start with funding: why does an open-source project need funding?

It turns out that while writing code is fun and developers are generally willing to contribute their time for free to do so, there are a host of decidedly less fun tasks needed to maintain and sustain an open source project. This includes handling any legal/trademark issues, triaging tickets, guiding community discussions, organizing conferences, managing releases, and so on. As a result, almost all popular open source packages have some degree of funding involved, typically in one of three forms:

1) Corporate Sponsor - A group of engineers within a larger, for-profit company decide to open-source internal code. This is how React (Facebook) and Angular (Google) emerged. Typically engineers at the company are paid, in part, to work on open source though community involvement from developers outside of the core company occurs as well. While this structure has the stability of a wealthy benefactor, there can be confusion around the licensing aspects at times.

2) Solo - An individual developer initially creates code, open sources it, and retains default control. This is the case for VueJS, Tailwind CSS, and Laravel, among others. Typically the lead developer either raises contributions directly like Evan You of VueJS, offer add-on services like Spark for Laravel, or the founders provide highly-paid consulting services.

3) Non-profit - This was Django’s approach early on, in 2008, when the Django Software Foundation was formed to promote, support, and advance Django.
