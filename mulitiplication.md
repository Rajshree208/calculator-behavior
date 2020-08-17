# Multiplication

Scenario: Multiplication of two positive numbers
  
  Given The calculator is turned on

  When I type in "positive number"
       And I press "*" operator
       And I type in "positive number"
       And I press "equals/enter"
  
  Then I see the product of the two positive numbers as the result
  
  Scenario: Multiplication of two negative numbers
  
  Given The calculator is turned on
  
  When I type in "negative number"
       And I press "*" operator
       And I type in "negative number"
       And I press "equals/enter"
  
  Then I see the product of the two numbers as the result
  
  Scenario: Multiplication of +ve and -ve number
  
  Given The calculator is turned on
  
  When I type in "positive number"
       And I press "*" operator
       And I type in "negative number"
       And I press "equals/enter"
  
  Then I see the product of the two numbers alongwith a - as the result
  
  Scenario: Multiplication of fractions
  
  Given The calculator is turned on
  
  When I type in "fraction"
       And I press "*" operator
       And I type in "fraction"
       And I press "equals/enter"
  
  Then I see the product of the two fractional numbers as the result
  
  Scenario: Multiplying numbers where the result goes out of range
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "*" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the product in an exponential form as the result
  
  Scenario: Multiplying a number by 0
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "*" operator
       And I type in 0
       And I press "equals/enter"
  
  Then I see 0 as the result
  
  Scenario: Multiplying a number by 1
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "*" operator
       And I type in 1
       And I press "equals/enter"
  
  Then I see the number itself as the result
  
  Scenario: Multiplying two decimal numbers
  
  Given The calculator is turned on
  
  When I type in "decimal number"
       And I press "*" operator
       And I type in "decimal number"
       And I press "equals/enter"
  
  Then I see the product in decimal precised to what the customer requires as the result
  
  Scenario: Multiplying more than two numbers
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "*" operator
       And I type in "number"
       And I press "*" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the product of the numbers as the result
  
  Scenario: Range of operands exceed limit
  
  Given The calculator is turned on
  
  When I type in "number" where number.countDigits > 10
       And I press "*" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I give a scrollable display for users 
       And I see the product of the numbers as the result
  
  Scenario: Typing operator more than once
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "*" operator
       And I press "*" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the error "Invalid Syntax" as the result
  
  Scenario: Interleaving operators
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "*" operator
       And I press "/" operator
       And I press "+" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the product of the two numbers as the result
