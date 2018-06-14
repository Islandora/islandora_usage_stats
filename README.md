# Islandora Usage Stats [![Build Status](https://travis-ci.org/Islandora/islandora_usage_stats.png?branch=7.x)](https://travis-ci.org/Islandora/islandora_usage_stats)

## Introduction

A module to track views and downloads of Islandora items. Features include:

* Toggle to ignore common bots, with a configurable regex bot filter
* View count uses session variables, and defaults to a 5 minute cooldown for repeated requests
* IP Exclusion list to prevent artificially inflating counts while testing/developing/administrating
* Several customizable blocks to display metrics
* Report-generating interface at __Reports > Islandora Usage Stats Reports__
* Object log views integration
* Access log for all views and downloads

Note:

* This module, and the views/blocks it generates, does **not** respect XACML or namespace restrictions.
* As this is a server-side tracking solution, a caching layer could prevent accesses from being recorded.  If this is impacting you a [solution](https://github.com/discoverygarden/islandora_ga_reports) using JavaScript may work better.

## Requirements

This module requires the following modules/libraries:

* [Tuque](https://github.com/islandora/tuque)
* [Islandora](https://github.com/islandora/islandora)
* [Islandora basic collection](https://github.com/Islandora/islandora_solution_pack_collection)
* [Views (3.x)](https://www.drupal.org/project/views)
* [Date](https://www.drupal.org/project/date)
* [Datepicker](https://www.drupal.org/project/datepicker)
* [Views Data Export](https://www.drupal.org/project/views_data_export)

## Installation

Install as usual, see [this](https://www.drupal.org/docs/7/extend/installing-modules) for further information.

## Usage

Usage stats for the children of a collection appear on the overview pages ("Manage" tab) of collections, to users who have the permission to "__View Islandora Usage Collection Overview__". A block showing the same information, __Usage Stats for Collections__, is also available under __Structure > Blocks__, which can be placed and permissioned like a normal block.

A view of all gathered stats, with the ability to generate CSV reports, is available at __Reports > Islandora Usage Stats__ (`admin/reports/islandora_usage_stats_report`) for users who have the permission "__View Islandora Usage Reports__".

This module also provides several Drupal blocks. They can be configured (e.g. number of rows to display, which PIDs to omit, ...) at __Structure > Blocks__:
* __Most Searched Terms__
* __Most Viewed Islandora Items__
* __Recently Accessed Islandora Items__
* __Recently Downloaded__


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
