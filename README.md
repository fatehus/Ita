Feature: Test scenarios for Search functionality


  Background:
    Given I prepare my environment for test execution
    Given I open search page
    And I get search result

  @search
  Scenario: User able to search items
    Then I search by name "computer"

  @search
  Scenario: User able to input letters
    Given I open search page
    Then I type name "hello"


  Scenario Outline: Test search functionality with multiple inputs
    Then I type "<search>"


    Examples: multiple words

    |search|
    |Amir  |
    |Fateh |
    |Leyla |
