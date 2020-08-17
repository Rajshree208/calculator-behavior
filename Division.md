# Division

Scenario: Division of two positive numbers
  
  Given The calculator is turned on

  When I type in "positive number"
       And I press "/" operator
       And I type in "positive number"
       And I press "equals/enter"
  
  Then I see the quotient of the two positive numbers as the result
  
  Scenario: Division of two negative numbers
  
  Given The calculator is turned on
  
  When I type in "negative number"
       And I press "/" operator
       And I type in "negative number"
       And I press "equals/enter"
  
  Then I see the quotient of the two numbers as the result
  
  Scenario: Division of +ve and -ve number
  
  Given The calculator is turned on
  
  When I type in "positive number"
       And I press "/" operator
       And I type in "negative number"
       And I press "equals/enter"
  
  Then I see the product of the two numbers alongwith a - as the result
  
  Scenario: Dividing a number by 0
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "/" operator
       And I type in 0
       And I press "equals/enter"
  
  Then I see an error stating "Cannot divide by zero" as the result
  
  Scenario: Dividing 0 by any number
  
  Given The calculator is turned on
  
  When I type in 0
       And I press "/" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see 0 as the result
  
  Scenario: Division when both operands are 0
  
  Given The calculator is turned on
  
  When I type in 0
       And I press "/" operator
       And I type in 0
       And I press "equals/enter"
  
  Then I see an error stating "Cannot divide by zero" as the result
  
  Scenario: Dividing more than two numbers
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "/" operator
       And I type in "number"
       And I press "/" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the quotient of the numbers in an order(left->right or right->left)
  based on the customer need as the result
  
   Scenario: Typing operator more than once
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "/" operator
       And I press "/" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the error "Invalid Syntax" as the result
  
  Scenario: Interleaving operators
  
  Given The calculator is turned on
  
  When I type in "number"
       And I press "/" operator
       And I press "*" operator
       And I press "+" operator
       And I type in "number"
       And I press "equals/enter"
  
  Then I see the quotient of the two numbers as the result
  
  Scenario: Converse operation
  
  Given The calculator is turned on
  
  When I type in "num1"
       And I press "/" operator
       And I type in "num2"
       And I press "equals/enter"
  
  Then I see the result of num1/num2 is not equal to the result
  of num2/num1
