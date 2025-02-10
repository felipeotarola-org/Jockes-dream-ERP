# Customer Registration Feature

This file outlines the customer registration feature using Gherkin syntax.

## Gherkin Syntax

```gherkin
Feature: Customer Registration
  To manage customer information
  As a business system
  I want to allow registration of new customers with proper validation

  Scenario: Successfully register a new customer
    Given I have entered valid customer information
    When I submit the registration form
    Then the customer is added to the system
    And I see a confirmation message

  Scenario: Fail to register a new customer due to invalid email
    Given I have entered valid customer information except an invalid email
    When I submit the registration form
    Then I see an error indicating the email is invalid

  Scenario: Fail to register a new customer because of missing required fields
    Given I have not entered all required customer information
    When I submit the registration form
    Then I see an error indicating which fields are missing
```

Use this Gherkin syntax to develop and test the customer registration process.
