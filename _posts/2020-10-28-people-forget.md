---
title: Making peace with Twilio
tags: Linux
article_header:
  type:overlay
  background_color:"977169"
---

Going insane, slowly but surely

<!--more-->

## There's this guy JR

JR never turns in his reports on time. The man needs a reminder every week by text.
I'm getting tired of it.

## Automation

Restore your sanity and automate text messaging using Twilio and crontab.

### Template (almost identical to offical example):

[File](https://github.com/achillesg007/woozy/blob/master/auto-phone.py)

You need to set up a twilio account for this to work.
{:.error}

### Crontab:
```yaml
10 13 * * MON [path-to-script]/auto-phone.py
```



