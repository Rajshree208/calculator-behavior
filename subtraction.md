# Subtraction

Scenario: Subtraction of two positive numbers
  
  Given The calculator is turned on

  When I type in "positive number"
       And I press "-" operator
       And I type in "positive number"
       And I press "equals/enter"
  
  Then I see the difference of the two positive numbers as the result

Scenario: Subtraction of two negative numbers
  
  Given The calculator is turned on
  
  When I type in "negative number"
       And I press "-" operator
       And I type in "negative number"
       And I press "equals/enter"
  
  Then I see the difference of the two numbers alongwith a -/+ sign depending upon the sign of the greater number as the result
  
  Scenario: Subtraction of +ve and -ve number
  
  Given The calculator is turned on
  
  When I type in "positive number"
       And I press "-" operator
       And I type in "negative number"
       And I press "equals/enter"
  
  Then I see the sum of the two numbers alongwith a -/+ sign depending upon the position of the negative number.
  
  Scenario: Subtraction of fractions
  
  Given The calculator is turned on
  
  When I type in "fraction"
       And I press "-" operator
       And I type in "fraction"
       And I press "equals/enter"
  
  Then I see the difference of the two fractional numbers as the result
  
  Scenario: Invalid Input is provided in input
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "-" operator
       And I type in "."
       And I press "equals/enter"
  
  Then I see the error "Invalid Input" as the result
  
  Scenario: Subtracting numbers where the result goes out of range
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "-" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the added number in an exponential form as the result
  
  Scenario: Typing operator more than once
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "-" operator
       And I press "-" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the error "Invalid Syntax" as the result
