---
group: security
title: Google reCAPTCHA
functional_areas:
  - Configuration
---

This extension adds the Google reCAPTCHA module to your Magento installation. Google reCAPTCHA provides a greater level of security for both the storefront and Admin UI than is available with standard CAPTCHA, and gives you the ability to:

- Verify when customers create accounts, retrieve passwords, log in to their accounts, or contact your company.
- Enhance security when Admin users log in.

Google reCAPTCHA reduces potential user error when entering a Captcha code and encourages cart conversion without adding hurdles during checkout.

At this time, Google reCAPTCHA can be installed only from the command line.

{:.bs-callout .bs-callout-info}
**Magento Community Contribution** - Magento thanks [Riccardo Tempesta](https://twitter.com/rictempesta) of [MageSpecialist](https://partners.magento.com/portal/details/partner/id/129) for contributing these features as part of the Magento Community Engineering program.

## Install Module

Install the extension using Composer for v2.1 and v2.2. Installations and upgrades of v2.3 include 2FA features.

Use the following composer command to install:

``` bash
composer require msp/recaptcha:2.0.0
```

To complete installation in an existing Magento instance, run the following commands to enable the module:

``` bash
php bin/magento module:enable --all
php bin/magento setup:upgrade
```

## Configure reCAPTCHA

See the [Magento Admin User Guide](https://docs.magento.com/m2/ce/user_guide/stores/security-google-recaptcha.html) for configuration options to the Magento Admin UI and storefront.

## Troubleshooting

The extension supports a command line option for disabling reCAPTCHA and allow backend access. Use this commands when you cannot access the Magento Admin UI.

``` bash
php bin/magento msp:security:recaptcha:disable
```