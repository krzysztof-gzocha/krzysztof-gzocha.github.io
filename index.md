# My projects

## Golang

### PinGOr

[![Build Status](https://travis-ci.org/krzysztof-gzocha/pingor.svg?branch=master)](https://travis-ci.org/krzysztof-gzocha/pingor)
[![Go Report Card](https://goreportcard.com/badge/github.com/krzysztof-gzocha/pingor)](https://goreportcard.com/report/github.com/krzysztof-gzocha/pingor)
[![codecov](https://codecov.io/gh/krzysztof-gzocha/pingor/branch/master/graph/badge.svg)](https://codecov.io/gh/krzysztof-gzocha/pingor)

Create logs about disconnections with Golang. Run pinGOr and see it's logs to know if your internet connection was interrupted or not. Currently pinGOr is logging all information to console and persist reconnection events to DynamoDB (if configured).

PinGOr will read provided config and try to:
- resolve provided host names to IPs,
- inspect HTTP statuses for provided URLs.

It will start checking the connection after configured minimal checking period and if the connection will be ok the period will be doubled.
When connection checks will drop below configured success rate threshold, then the connection will be marked as "dropped" and proper log will be created.

Link to [Github](https://github.com/krzysztof-gzocha/pingor)

### CurNot - Currency Rate Notifier

Small golang program capable of periodically checking different currencies exchange rates with different providers.


Implemented providers:
- [x] Name: `currencyConverter` - https://free.currencyconverterapi.com
- [x] Name: `openExchangeRates` - https://openExchangeRates.org

## PHP

### Searcher 

[![Build Status](https://travis-ci.org/krzysztof-gzocha/searcher.svg?branch=master)](https://travis-ci.org/krzysztof-gzocha/searcher) [![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/krzysztof-gzocha/searcher/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/krzysztof-gzocha/searcher/?branch=master) [![Code Coverage](https://scrutinizer-ci.com/g/krzysztof-gzocha/searcher/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/krzysztof-gzocha/searcher/?branch=master) [![Packagist](https://img.shields.io/packagist/v/krzysztof-gzocha/searcher.svg?style=plastic)](https://packagist.org/packages/krzysztof-gzocha/searcher) [![SensioLabsInsight](https://insight.sensiolabs.com/projects/2b7df098-46c6-43e1-ac94-b0eab3d46401/mini.png)](https://insight.sensiolabs.com/projects/2b7df098-46c6-43e1-ac94-b0eab3d46401)

Searcher is a framework-agnostic search query builder. Search queries are written using criterias and can be run against MySQL, MongoDB, ElasticSearch, files or whatever else you like.

Have you ever seen code responsible for searching for something based on many different criteria? It can become quite a mess!
Imagine you have a form with 20 fields and all of them have some impact on searching conditions.
It's not a great idea to pass a whole form to some service at let it parse everything in one place.
Thanks to this library you can split the responsibility of building query criteria to several smaller classes. One class per filter. One `CriteriaBuilder` per `Criteria`.
This way, inside `CriteriaBuilder` you care only about one `Criteria`, which makes it a lot more readable and maintanable.
You can later use exactly the same `Criteria` for different searches, with different `CriteriaBuilder` and even different `SearchingContext` which can use even different databases.
You can even use searcher to find **files** on your system thanks to `FinderSearchingContext`.

Full documentation can be found at [http://searcher.rtfd.io/](http://searcher.readthedocs.io/en/stable/introduction.html)

Link to [Github](https://github.com/krzysztof-gzocha/searcher)

### PayU integration

[![Build Status](https://travis-ci.org/krzysztof-gzocha/payu.svg?branch=master)](https://travis-ci.org/krzysztof-gzocha/payu)

This library written in PHP will allow easily integration with [PayU API v2.1](http://developers.payu.com/pl/restapi.html). It's a bit old, so it works with PHP version >=5.4 and HHVM.  

Link to [Github](https://github.com/krzysztof-gzocha/payu)
