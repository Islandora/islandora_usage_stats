# Islandora Usage Stats [![Build Status](https://travis-ci.org/Islandora/islandora_usage_stats.png?branch=7.x)](https://travis-ci.org/Islandora/islandora_usage_stats)

## Introduction

A module that tracks views and downloads of Islandora items, as well as solr searches, in the Drupal database.

Features include:

* ability to ignore common bots, with a configurable regex bot filter
* ability to ignore repeated requests based on session variables, with a default cooldown period of 5 minutes
* ability to ignore requests from specific IP addresses for testing/developing/administration
* Views integration

Islandora Usage Stats provides the back-end framework and gathers usage data, which can be exposed through custom Views or additional modules. It also provides some built-in tools for exposing usage information.

Caution:

* This module, and the views/blocks it generates, does **not** respect XACML or namespace restrictions.
* As this is a server-side tracking solution, a caching layer can prevent usage from being accurately recorded.  If this is impacting you, a solution using JavaScript may work better for you. Community solutions include [discoverygarden's Google Analytics module](https://github.com/discoverygarden/islandora_ga_reports) and [Diego Pino's Matomo module](https://github.com/DiegoPino/islandora_piwik/). 

## Requirements

This module requires the following modules/libraries:

* [Islandora](https://github.com/islandora/islandora)
* [Islandora basic collection](https://github.com/Islandora/islandora_solution_pack_collection)
* [Views](https://www.drupal.org/project/views)
* [Views Data Export](https://www.drupal.org/project/views_data_export)
* [Date](https://www.drupal.org/project/date)
* [Datepicker](https://www.drupal.org/project/datepicker)

This module can be extended with the following Islandora community/Drupal contrib modules:

* Views UI (bundled with Views)
* [Islandora Usage Stats Callbacks](https://github.com/Islandora-Labs/islandora_usage_stats_callbacks) (in Islandora Labs)
* [Islandora Usage Stats Charts](https://github.com/mjordan/islandora_usage_stats_charts) (by Mark Jordan)


## Installation

Install as usual, see [this](https://www.drupal.org/docs/7/extend/installing-modules) for further information.

## Usage

The data collected by Islandora Usage Stats is made available to Views, so custom reports can be created. It also works with community modules such as [Islandora Usage Stats Callbacks](https://github.com/Islandora-Labs/islandora_usage_stats_callbacks) or [Islandora Usage Stats Charts](https://github.com/mjordan/islandora_usage_stats_charts) to provide more functionality. These modules are not part of Islandora's official releases.

Out of the box, Islandora usage stats can also provide:
* Views of usage stats on Collection overview pages
* A View of object page views at __Reports > Islandora Usage Stats Reports__
* Several customizable blocks to display the most popular objects
* A customizable block to show collection usage stats


## Configuration

Configuration options are available at Islandora » Islandora Utility Modules » Islandora Usage Stats Settings (admin/islandora/tools/islandora_usage_stats).

![Configuration](https://user-images.githubusercontent.com/1943338/41436826-3bab2b9a-6ff9-11e8-96f9-7819388c40ee.png)

## Documentation

Further documentation for this module is available at [our wiki](https://wiki.duraspace.org/display/ISLANDORA/Islandora+Usage+Stats).

## Troubleshooting/Issues

Having problems or solved a problem? Check out the Islandora google groups for a solution.

* [Islandora Group](https://groups.google.com/forum/?hl=en&fromgroups#!forum/islandora)
* [Islandora Dev Group](https://groups.google.com/forum/?hl=en&fromgroups#!forum/islandora-dev)

## Maintainers/Sponsors

Work based on code from https://github.com/roblib/islandora_scholar_upei and the scholar_tracking module for Drupal 6. Iterated on by Ryerson University Library and Archives (RULA) and discoverygarden inc.

Current maintainers:

* [Bryan Brown](https://github.com/bryjbrown)

Sponsors:

* [METRO](http://metro.org/)

## Development

If you would like to contribute to this module, please check out [CONTRIBUTING.md](CONTRIBUTING.md). In addition, we have helpful [Documentation for Developers](https://github.com/Islandora/islandora/wiki#wiki-documentation-for-developers) info, as well as our [Developers](http://islandora.ca/developers) section on the [Islandora.ca](http://islandora.ca) site.

## License

[GPLv3](http://www.gnu.org/licenses/gpl-3.0.txt)
