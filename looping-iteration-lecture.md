# Looping and Iteration

If we can get the students thinking of arrays and hashes as very similar data structures with minor differences, then teaching iteration becomes a lot easier.

## SWBATs
HASH - Iterate through hashes using the each, each_key, and each_value methods
ARRAY - Iterate through arrays using the each method

## Hook

When Facebook decides to changes something for every user on the site, how do you think they do it?
When a conference needs badges printed for 10,000 attendees, what's the process for creating the labels?
We're going to figure this out in this next lesson.

Now that we've learned about arrays and hashes, let's try something out. What would we have to do if we had an array of names, and we want to create another new array for our labels with "Hi my name is (name)"?

we have `names = ["Alexandra", "Anthony", "Aaron", "Alyssa"]` and want `["hi! my name is Alexandra", "hi my name is Anthony", "hi my name is Aaron", "hi my name is Alyssa"]`

Let the students try to do this manually - have them experience the pain. Can you imagine doing this with 1000 names? There has to be a better way...

## Iteration

Iteration is the process of running code on every item in an array, or on every key-value pair in a hash. We iterate over an array or a hash in order to repeat an action on each individual item.

Can you think of situations in real life when we would want to repeat code on every item in a list?

Here's how we would do the above using iteration - we use the `.each` method.

First talk it out: " create a new empty array. For each item in the names array, take the name and insert it into the string 'hi! my name is _____'. Then take that string and add it on to the new array "
Once we have a clear explanation, let's convert this into code.

```ruby
name_tags = []
names.each do |name|
  name_tags << "hi! my name is #{name}"
end
print name_tags
```
Explain that do and end are the start and end of the code that will be run on the items, and that the `|name|` variable is a placeholder for each item as it gets passed into the code.


Try a few more examples, and then have them try a few on their own in the [Array Iteration mini lab](https://github.com/upperlinecode/array-iteration-mini-lab/)

---
Hash Iteration is just the same, except that you need to pass in the key and the value as opposed to just the value:

```ruby
birthdays = { :joe => "April 21st",
              :jessica => "August 5th",
              :june => "November 13th",
              :janet => "January 12th"
}

birthdays.each do |name, birthday|
  print "#{name.to_s.capitalize}'s birthday is #{birthday}'"
end
```
(Note, we need to convert the keys into strings using `.to_s` before we can use them!)

[Hash Iteration Mini Lab](https://github.com/upperlinecode/hash-iteration-mini-lab/)

Get the students to look at a few other iteration methods:
+ `.collect` what does this do? How is it different from each?
+ `.find`
+ `.each_with_index`
+ `.each_key` and `.each_value`
