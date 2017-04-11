# SilverStripe MetaDescription Fallback

## Requirements

* SilverStripe 3.2 and above
* PHP 5.4 and above

## Maintainers

* michal.kleiner@chrometoaster.com

## Description

This module applies a data extension to SiteTree providing a mechanism to populate meta description header from a defined
set of content fields when the default MetaDescription is empty.

The list can use names of fields, names of methods or leverage the the dot notation to reference relations or methods,
as outlined in the configuration example below.

## Installation with [Composer](https://getcomposer.org/)

```
composer require "chrometoaster/silverstripe-metadescription-fallback"
```

### Example configuration

In your `config.yml`, define the list of fields:

```YAML
Chrometoaster\SEO\DataExtensions\MetaDescriptionFallbackSiteTreeExtension:
  fallback_fields:
   - Description
   - Introduction
   - Content.Summary
   - RelatedPages.First.MetaDescription
```

Run dev/build either via opening the url `http://<your-host>/dev/build` in a browser or
by running the dev/build task using CLI.

## Reporting Issues

Please [create an issue](http://github.com/chrometoasters/silverstripe-metadescription-fallback/issues) for any bugs you've found, or features you're missing.

## Changelog

For details of updates, bugfixes, and features, please see the [changelog](CHANGELOG.md).

## TODO

* Add unit tests for fallback mechanism.
