Changes
=======

2.3.4 (2018-06-18)
++++++++++++++++++

- Added auto generated Django migration file

2.3.3 (2018-06-18)
++++++++++++++++++

- Updated so that if the Site table isn't available, EMAIL_CONFIRM_LA_DOMAIN is set to 'example.com'
  (assuming it's not set to anything in settings). This happens during unit tests.

2.3.2 (2018-06-12)
++++++++++++++++++

- Added 'reply_to' field to email message (required if used in conjuction with Postmark)

2.3.1 (2017-09-13)
++++++++++++++++++

- Updated code to conform to what the README says about using Site.objects.get_current().domain if EMAIL_CONFIRM_LA_DOMAIN isn't set
- Added ability to send template context data when using verify_email_for_object()
    
2.3.0 (2016-09-09)
++++++++++++++++++

- Support automatically login after email confirmation via `EMAIL_CONFIRM_LA_AUTOLOGIN` setting
- Use `uuid.uuid4()` to generate confirmation key


2.2.0 (2016-07-25)
++++++++++++++++++

- Fix migration dependencies
- New parameter ``old_email`` in `post_email_confirmation_confirm` signal


2.1.0 (2016-07-25)
++++++++++++++++++

- Reset migration
- Fix ``EmailConfirmationValidator``


2.0.0 (2016-07-22)
++++++++++++++++++

- **v2.0.0 is a BACKWARD-INCOMPATIBLE release!**
- Full refactoring
- Drop support for Django 1.4


0.2.3 (2015-03-08)
++++++++++++++++++

- Fix `#14 <https://github.com/vinta/django-email-confirm-la/issues/14>`_ Admin raises an `AttributeError` when `content_object` doesn't exist


0.2.2 (2014-11-13)
++++++++++++++++++

- New admin action: Re-send confirmation email
- New setting: ``EMAIL_CONFIRM_LA_EMAIL_BACKEND``
- Change ``EMAIL_CONFIRM_LA_DOMAIN`` default value to ``''``, fail fast
- Fix circular import


0.2.1 (2014-11-09)
++++++++++++++++++

- Django 1.6 compatibility: ``transaction.atomic``
- Django 1.4 compatibility: ``update_fields``


0.2.0 (2014-11-08)
++++++++++++++++++

- Django 1.7 compatibility: ``migrations``


0.1.0 (2014-10-31)
++++++++++++++++++

- Initial release
