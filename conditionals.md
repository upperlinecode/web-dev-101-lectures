# Conditionals
SWBATs:
+ CONDITIONALS - Explain the use of a boolean data type.
+ CONDITIONALS - Explain what an if statement is and why it's used
+ CONDITIONALS - Implement an if statement with 1, 2, and 3+ branches
+ CONDITIONALS - Use comparison operators in a conditional statement

## Suggested Hooks

+ Have students stand up and teacher conducts a sorting of the students:
  + Over vs Under 15 - if you are over 15 do ten jumping jacks.
  + Horoscope - if you are a libra, stand up
  + etc
  + Explain that what we're doing here is using conditionals or if statements to determine if something is true or false and then do something if the condition is met.
  + If statements in code are just what they sound like - they test for the truth of a comparison, and then execute code if the comparison is true.

  ```ruby
  horoscope = "Libra"

  if horoscope == "Libra"
    puts "Stand Up Libras!"
  end
  ```

  An if statement allows us to trigger events based on specific conditions.

  **Pause and have students think of situations in technology where if statements would be useful. Have at least 3 groups share**

## Syntax

If statements are pretty straightforward:

```ruby
if comparison
  run this code
end
```

The comparison portion of an if statement checks to see if something is true or false.

+ `==` checks for equality. Show how this can be used for strings and numbers.
+ `<`, `>`, `>=`, `<=`. Show how these can be used with numbers in conditional statements.

```ruby
if 10 > 9
  puts "ten is greater than 9!"
end
```
**Pause and have the students write and test some basic if statements - encourage them to use gets.chomp to get data from the user that they can write comparisons with.**

Example:

```ruby
puts "how old are you?"
age = gets.chomp.to_i
if age > 30
  puts "WOW YOU ARE ANCIENT"
end
```

### Additional branches
What if we want to do something different if the if statement is false?

+ Show students how to add an `elsif` statement.

```ruby
puts "how old are you?"
age = gets.chomp.to_i
if age > 30
  puts "WOW YOU ARE ANCIENT"
elsif age < 30 && age > 20
  puts "Twenties are the new thirties?"
end
```

+ Show students that `else` is used as a catchall for any other situation that doesn't match the ifs and elsifs:

```ruby
puts "how old are you?"
age = gets.chomp.to_i
if age > 30
  puts "WOW YOU ARE ANCIENT"
elsif age < 30 && age > 20
  puts "Twenties are the new thirties?"
else
  puts "You are either very old, or very young..."
end
```

+ Show how comparisons can be strung together with `&&` (AND) and `||` (OR). For `&&` both comparisons must be true in order to ensure the code is run. For `||` one or the other must be true to get the code to run.
