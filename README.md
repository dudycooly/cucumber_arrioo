cucumber_arrioo
===============


What?
====

Cucumber Pretty Formatter that outputs  only Scenarios,Feature file names and failing steps

Tested with Cucumber 0.10.5


Why?
====
As I felt pretty format is too verbose ;) , Lookng at [SlowHandCuke] (https://github.com/moredip/SlowHandCuke) sparked this idea



How To Install
==============

Just copy <code>arrioo_formatter</code> to <code>features/support</code>

Then add <code> -f arrioo </code>to your cucumber command-line.



License
=========

Do what you will, but give credit.

jay [dot] naveen [at] gmail.com


Sample Output
=========

(cats)jay@user-HP-Z400-Workstation:~/workspace/cats/cats/tests/test_apps/features/bizrules$ cucumber --format arrioo availability_rules.feature 
Using the default profile...
CATS server is up and running...
Feature: Business Rule Reporting -- Availability rules
                                               
  Scenario: Check OFFNET-PSTN-VOICE service availability rule returned # availability_rules.feature:12
    Then I should see the following "primary rules":                   # step_definitions/bizrules_steps.rb:196
  | rule                                                                                                                                        |
  | [OFFNET-PSTsN-VOICE] is available if [Characteristics/AvailableNetwork] with name [OFFNET-PSTN-VOICE] received in context |
  Unable to find css "li" with text "OFFNET-PSTsN-VOICE is available if Characteristics/AvailableNetwork with name OFFNET-PSTN-VOICE received in context" (Capybara::ElementNotFound)
  ./step_definitions/bizrules_steps.rb:206:in `block (3 levels) in <top (required)>'
  ./step_definitions/bizrules_steps.rb:199:in `each'
  ./step_definitions/bizrules_steps.rb:199:in `block (2 levels) in <top (required)>'
  ./step_definitions/bizrules_steps.rb:197:in `/^I should see the following "(.*?)":$/'
  availability_rules.feature:14:in `Then I should see the following "primary rules":'
                                               
  Scenario: Check ONNET-MPF-VOICE_ONNET-MPF-DATA Service Group availability rule returned # availability_rules.feature:18
                                                          
Failing Scenarios:
cucumber availability_rules.feature:12 # Scenario: Check OFFNET-PSTN-VOICE service availability rule returned

2 scenarios (1 failed, 1 passed)
10 steps (1 failed, 9 passed)
0m11.787s
