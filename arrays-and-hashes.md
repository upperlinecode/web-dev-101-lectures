# Arrays and Hashes Lecture

Arrays and hashes are really fun to teach and can be made very accessible with student input and examples. This topic can be broken down into two lectures (a. Arrays b. Hashes) but it's good for there to be some continuity between them as array and hash syntax is so similar.

In this lecture, we're going to teach arrays and hashes together, and then teach iteration separately.

## SWBATs:

ARRAY - Explain what an array is and why it's used
ARRAY - Create an array
ARRAY - Return a specific value from an array using it's index
ARRAY - Add, delete and modify items in an array
ARRAY - Mutate arrays using methods available to all arrays
ARRAY - Iterate through arrays using the each method
ARRAY - Use .split to change a string into an array
ARRAY - Assign various an array to a variable
HASH - Explain what a hash is and why it's used
HASH - Create a hash
HASH - Return a specific value from a hash using it's key
HASH - Mutate hashes using methods available to all hashes
HASH - Add delete and modify key-value pairs in a hash
HASH - Explain what a symbol is and why it's used
HASH - Use symbols as keys in hashes
HASH - Iterate through hashes using the each, each_key, and each_value methods
HASH - Parse through nested hashes and arrays to pull out specific pieces data

## Hook

+ Ask the students about lists that they make in every day life - put these up on the board (grocery lists, bucket list, attendance list, etc). Once you've done this, read the room and choose one of these examples to build a list from on the whiteboard.
  + For example, choose to create a bucket list and ask students for their suggestions (add to board). I like to initially list things out like this:

| number  |   item                 |
|---      |---                     |
| 1  | Camp in New Zealand         |
| 2  | Eat at a 3 star restaurant  |
| 3  | Go skydiving                |
| 4  |  Compete in the Olympics    |


## Arrays

  + Tell the students that today we're going to be learning to create different types of lists in programming. These are called arrays and hashes.
  + **Think and Share:** Pause and have students think of why lists might be useful or important in programming. When are lists used in apps?
  + Before we start creating our lists in programming, let's actually modify this list that's on the board so that we use the same syntax as we would in Ruby.
    + Change "number" to "index" and start counting from 0.

| index  |   item                 |
|---      |---                     |
| 0  | Camp in New Zealand         |
| 1  | Eat at a 3 star restaurant  |
| 2  | Go skydiving                |
| 3  |  Compete in the Olympics    |

+ We call the location in the array the 'index', and arrays in Ruby (and most other languages) start at 0. Let's call this array `bucket_list` and map out our table to what this looks like in ruby:

```ruby
bucket_list = ["Camp in New Zealand","Eat at a 3 star restaurant","Go skydiving","Compete in the Olympics"]
```

+ Arrays in Ruby are shown by using square brackets, and then separating each item by commas.
+ You can create arrays with any sort of item - strings, integers, floats, or even other arrays!

+ **Pause** Have students create their own bucket_list (or other) arrays in a new ruby file called `arrays.rb.`

## Array CRUD

Ok, so we have an array, but what we really want to do is **use** it. How do we use lists in real life? (Ask)

+ Read from the list
+ Add items to the list
+ Remove items from a list
+ Change items on a list
+ Check if an items is on a list
+ See how long a list is
+ etc...

We can do all of these things, and more, using array methods. Methods are collections of code that allow us to take certain actions.

(As you walk through these, have the students follow along and practice with their own arrays)

+ **Read:** We can look at an individual item in an array by calling it using square brackets and the index. `bucket_list[1]` will return the second item in an array.
+ **Create:** You can add to an array by using the `.push()` method or `<<`. Example: `bucket_list.push("Go to Alaska")` or
`bucket_list << "Go to Alaska"` - these add to the END of the array.
+ **Update:** If we want to change an item in an array, we call it by its index (using square brackets) and then reassign it. Example: `bucket_list[4] = "Go to Iceland"`
+ **Delete:** `bucket_list.delete("Go to Iceland")` OR `bucket_list.delete_at(4)`
+ **Length:** Check the length of an array using `.count`: `bucket_list.count`

Stop here and have the students practice adding, deleting, updating, and reading from arrays. There are a few array labs to try out at this point ([the Mini-Lab on Countries](https://github.com/upperlinecode/upperline-hs-manipulating-arrays-mini-lab) is a good one).

## Hashes

We've created this table to represent our array, but we have a problem here. We don't know which item belongs to which student. We're going to introduce a new data structure called a **hash** that solves this problem for us. In a hash, we can update our two column table to look like this (on the board update the table):

| name  |   item                 |
|---      |---                     |
| Danny  | Camp in New Zealand         |
| Taylor  | Eat at a 3 star restaurant  |
| Jeff  | Go skydiving                |
| Melanie  |  Compete in the Olympics    |

Really, that's the only big difference between hashes and arrays - they're not ordered and indices we have keys. Each line is known as a key-value pair.

Now let's create this hash in ruby:

[hash documentation](https://ruby-doc.org/core-2.4.0/Hash.html)

```ruby
bucket_list = {
  :danny => "Camp in New Zealand",
  :taylor => "Eat at a 3 star restaurant",
  :jeff => "Go skydiving",
  :melanie => "Compete in the Olympics"
}
```
Highlight to the students:

+ Each key-value pair is separated by commas
+ we use :symbols for the keys so that we can make sure that each key is unique
+ Keys are always on the left, values are always on the right.
+ Accessing values from a hash is identical to arrays, except that instead of using indexes (bucket_list[0]), we use the key (bucket_list[:danny])

**Pause** Have the students build a new array by interviewing each other. The array should have student names as keys, and their birthday as values. (feel free to pick a different example to work with.)

Challenge the students to figure out how to do the same CRUD by googling and looking at the documentation:
+ How to find the length of a hash
+ How to add to a hash
+ How to delete a key-value pair
+ How to change a value for a key value pair
