# BDD test

## Nightwatch VS Protractor

Recently, nightwatch.js+cucumber.js were pitched against protractor for behavior driven tests. Well,
it fails to compete as it could not complete a simple bdd test task:

```
# features/documentation.feature
Feature: Example feature
  As a user of aurelia.js
  I want to have documentation on aurelia
  So that I can concentrate on building awesome applications

  Scenario: Reading documentation
    Given I am on the aurelia js org web site
    When I click on "select your role."
    Then I should see "Are you a Web Dev?"
```

And what's worse, it started to report "PASS" for obviously failing tests. And it could not
even produce a screenshot to prove it is right.

Things may change but here are the things under the test:

```
  "dependencies": {
    "chromedriver": "^2.31.0",
    "cucumber": "^3.0.0",
    "geckodriver": "^1.8.1",
    "nightwatch": "^0.9.16",
    "nightwatch-cucumber": "^8.0.4",
    "phantomjs-prebuilt": "^2.1.15",
    "selenium-server": "^3.5.0"
  }
```