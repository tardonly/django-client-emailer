django-client-emailer:
=====================================

Introduction:
=============

django-client-emailer is used for sending mails from different clients i.e. AWS, sendgrid, mailjet etc.

Source Code is available in Repository(https://github.com/tardonly/django-client-emailer).

Modules used:

* boto3
* requests
* django


Requirements
======================

    Python  >= 3.4

Installation Procedure
======================

1. Install django-client-emailer using the following command::

        pip install django-client-emailer
    		or
        git clone git://github.com/micropyramid/django-email-gateway.git

        cd django-client-emailer

        python setup.py install


2. After installing/cloning this, add the following details in django settings file to send emails notifications ::

    MAIL_SENDER = 'AMAZON' for aws
                        or
                  'MAILGUN' for mailgun
                        or
                  'SENDGRID' for sendgrid
                        or
                  'MAILJET' for mailjet
                        or
                  None for django default mailer

   #### AWS details if mail sender amazon

    AWS_ACCESS_KEY_ID = "Your AWS Access Key"

    AWS_SECRET_ACCESS_KEY = "Your AWS Secret Key"

   #### mailgun if mail sender is mailgun

    MGUN_API_URL = 'mailgun api url'

    MGUN_API_KEY = 'mailgun api key'

   ##### mailjet if mail sender is mailjet

    MJ_APIKEY_PUBLIC = 'mailjet api key'

    MJ_APIKEY_PRIVATE = 'mailjet api secret'

validating emails
==================
Email get validated from `validate_email`

Usage:
=======

#####Sending an email:

    send_mail(subject, email_template_name, context, from_email, to_email, verified, cc_list=None, bcc_list=None)
It will process the your message content, will return the email subject, from mail, to email(abc@yourdomain.com), hashcode(abc), mail content.



