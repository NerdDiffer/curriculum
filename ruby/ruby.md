# Ruby
Total Estimated Time: 100-200 hrs

## !! This section is incomplete !!

*[Top level table of contents](/README.md)*

## Table of Contents
1. Intro
2. Basic Ruby
2. Intermediate Ruby
3. Ruby and the Web
4. File I/O and Serialization
5. Testing Ruby with RSpec
6. Basic Data Structures
7. Basic Algorithms
8. Final Projects
9. Finish

## Intro

In this unit you will learn Ruby, the language designed specifically with programmer happiness in mind.  It's a healthy chunk of learning but, by the end of it all, you'll have built some pretty sweet games including Tic Tac Toe, Minesweeper, Checkers, and Chess.  You'll be able to put together a Twitter spambot (that really spams!), save and open files, test out your code, separate your spaghetti code into nice modular classes, and even reproduce some basic algorithms and data structures for solving complex problems.  Basically, you're going to start feeling a whole lot more like a real programmer and that feeling will be justified.

Some people believe you can just dive right into Rails and start firing out websites.  Rails is a framework built using Ruby and every piece of code in it is Ruby.  When (not *if*) something in your project breaks, you'd better be able to debug it.  And what happens when you want to stretch your wings and do something just a bit beyond what the vanilla tutorials show you how to do?  The amount of time you'd spend googling your error messages and staring blankly at help docs was better spent learning Ruby.

As you may gather, this is also where the real project work begins.  Some of the early material will be fairly straightforward and will rely on simple exercises to help reinforce understanding.  As we get further along and into some of the more advanced topics, we'll be learning less and doing more... just the way it should be.   Buckle up, strap in, and let's get learning!

**How this will work:**

Ruby's a big language so it's been broken up into smaller chunks to make it more digesible.  In each section, you'll first be asked to do readings, watch videos, or otherwise view content.  We'll provide a "A Brief Summary" of the material but it's not a replacement for actually doing the reading.  At the end of each section or group of sections will be programming exercises which are best done in pairs.

**Our free resources:**

The goal here is to provide as much of this curriculum as possible using free resources.  If you've done the prep work from Web Development 101 then you should have a good handle on the basics but these resources are important to help you really understand the material.
* The staple book: Zed Shaw's [Learn Code the Hard Way](http://ruby.learncodethehardway.org/book/), an extension of his wildly popular Learn Python the Hard Way into Ruby.
* For the crazies: Why's [Poignant Guide to Programming](http://mislav.uniqpath.com/poignant-guide/book/chapter-1.html) (check it out... if it jives with your learning style, you may have found the match you never thought you'd find)
* If there's anything you need to brush up on still: [The Ruby User's Guide](http://www.rubyist.net/~slagell/ruby/) has sections on many topics you might want to dive back into for a deeper look.

**Other good resources:**
* Peter Cooper's [Beginning Ruby](http://beginningruby.org/) is a solid introduction to Ruby that covers pretty much the breadth of the language as you need to understand it.
* Brian Marick's [Everyday Scripting with Ruby](http://pragprog.com/book/bmsft/everyday-scripting-with-ruby) takes a pragmatic approach to learning Ruby to help with the kinds of problems you might face in a variety of different real-world work scenarios.

## Basic Ruby

### Intro

Ruby shouldn't be anything new to you by now... you should have completed the preparatory readings, Ruby Monk, and the test-first exercises as part of the [Ruby 101 section of the Web Development 101 Unit](/web_development_basics/web_development_basics.md#ruby-101) that you completed prior to jumping into this.  If you haven't, go back and work on that before getting started here.  It's expected that you have a pretty good handle on the basics of the Ruby language and an idea of what you're still shakey on.

In this section on Basic Ruby, we're going to make sure you really do understand all the building blocks of the language and of programming in general.  If there's something that you still just don't quite understand, track it down via the Additional Resources section or Google for it on your own.  *How* you learn isn't as important as making sure you're comfortable with your understanding of everything that will be covered here.

### Primitive Data Types

Primitive data types are the basic building blocks of computer programs.  Understanding them and what you can do with them is like knowing your ABC's.  Get well acquainted with Numbers, Strings, Arrays, Hashes, Enumerable methods, Objects, Ranges, and Dates/Times.  You're populating your developer's toolkit.

The exercises should help you hone in on what things you understand well and which ones you need to dig deeper on.  The larger exercises towards the end will round things out a bit more wholistically.

#### Numbers and Operators and Expressions
##### Goals
This is pretty straightforward stuff.  The goal here is to familiarize yourself with all basic data types and how they interact in arithmetic expressions

##### Thought Questions
* What's the difference between `=`, `==`, and `===`?
* How do you do exponents in Ruby?

##### Do These First
* Read [Learn Ruby the Hard Way Chapters 1-5](http://ruby.learncodethehardway.org/book/ex3.html)
* Read [Learn to Program Chapter 1](http://pine.fm/LearnToProgram/?Chapter=01) (You should already have completed this)
* Read [http://rubylearning.com/satishtalim/numbers_in_ruby.html](http://rubylearning.com/satishtalim/numbers_in_ruby.html)

##### A Brief Summary

When doing mathematical operations, Ruby expects the result to be the same type as the inputs, so dividing two integers by each other will produce an integer... whether you want to or not:

    > 5 / 3
    => 1  

To fix this, you need to make one of the inputs a different data type that can handle decimals, like a *floating point* number (float): 

    > 5.0 / 3 
    => 1.6666666666666667

Because Ruby is so flexible, it lets you do some quirky things like multiplying completely different data types together in a way that you sort of think you *should* be able to but never expected to actually be able to do:

    > "hi" * 3
    => "hihihihi"

These types of operations work the same way with variables:

    > my_word = "howdy"
    => "howdy"
    > my_word * 3
    => "howdyhowdyhowdy"

For equality:
* `=` is for assignment, so it assigns a value to a variable as in `> name = "Erik"`
* `==` is for checking that two things are equal but don't have to be identical instances.  You'll use this in most cases, especially when working with conditional statements.  `> 1 + 1 == 2` returns '=> true'.  When you start creating your own classes (like an "Animal" class), you'll need to tell Ruby how to compare two animal instances by writing your own version of this method (it's easy).
* `===` can actually mean some different things (you can overwrite it easily). You will probably be sticking with `==` in most situations, but it's good to understand `===` as well.  `===` typically asks whether the thing on the right is a member or a part or a type of the thing on the left.  If the thing on the left is the range `(1..4)` and we want to know if 3 is inside there:

    > (1..4) === 3
    => true

This also works for checking whether some object is an instance of a class:

    > Integer === 3
    => true

See [http://stackoverflow.com/questions/4467538/what-does-the-operator-do-in-ruby](http://stackoverflow.com/questions/4467538/what-does-the-operator-do-in-ruby) for a more detailed explanation.

##### Exercises
* Play around in IRB and just try multiplying and dividing and equating and comparing things to each other.  Be creative until you have a good handle on things.

#### Objects and Methods
##### Intro and Goals
"Everything in Ruby is an Object" is something you'll hear rather frequently.  "Pretty much everything else is a method" could also be said.  The goal here is for you to see the Matrix... that everything in Ruby is an Object, every object has a class, and being a part of that class gives the object lots of cool methods that it can use to ask questions or do things.  Being incredibly object-oriented gives Ruby lots of power and makes your life easier.

Hopefully you've already picked most of this up from the prep-work.

##### Thought Questions
* What is an object?
* What is a class?
* What is a method?
* How can you print out an object or class's methods?
* What is inheritance?
* How many classes can a class inherit from in Ruby?
* What's the top-level ancestor class that all others inherit from in Ruby?
* What are Reflection Methods?
* What are a method's Side Effects?
* How do methods take inputs?
* Do all methods have outputs?
* What is Method Chaining and how does it work?

##### Do These First
* [Ruby Inheritance](http://rubylearning.com/satishtalim/ruby_inheritance.html)

##### A Brief Summary
  
Think of every "thing" in Ruby as a having more than meets the eye. The number `12` is more than just a number... It's an **object*** and Ruby lets you do all kinds of interesting things to it like adding and multiplying and asking it questions like `> 12.class` or `> 12+3`.

Ruby gives all objects a bunch of neat **methods**.  If you ever want to know what an object's methods are, just use the `.methods` method!  Asking `> 12345.methods` in IRB will return a whole bunch of methods that you can try out on the number 12345.  You'll also see that the basic operators like `+` and `-` and `/` are all methods too (they're included in that list).  You can call them using the dot `> 1.+2` like any other method or, luckily for you, Ruby made some special shortcuts for them so you can just use them as you have been: `> 1+2`.

Some methods ask true/false questions, and are usually named with a question mark at the end like `.is_a?`, which asks whether an object is a type of something else, e.g. `1.is_a?Integer` returns `true` while `"hihi".is_a?Integer` returns `false`.  You'll get used to that naming convention.  Methods like `.is_a?`, which tell you something about the object itself, are called **Reflection Methods** (as in, "the object quietly reflected on its nature and told me that it is indeed an Integer").  `.class` was another one we saw, where the object will tell you what class it is.

What is a method? A method is just a function or a black box.  You put the thing on the left in, and it spits something out on the right.  *Every method returns something*, even if it's just `nil`.  Some methods are more useful for their **Side Effects** than the thing they actually return, like `puts`.  That's why when you say `> puts "hi"` in IRB, you'll see a little `=> nil` down below... the method prints out your string as a "side effect" and then returns `nil` after it's done.  When you write your own methods, if you forget to think about the return statement, sometimes you'll get some wierd behavior so always think about what's going in and what's coming out of a method.

Methods can take **inputs** too, which are included in parentheses to the right of the method name (though they can be omitted, as you do with `> puts("hi")` becoming `> puts "hi"`... it's okay to be lazy, as long as you know what you're doing).  Going back to the addition example, `> 1+2==3` is asking whether 1+2 will equal 3 (it returns `=> true`), but it can more explicitly be written `> 1.+(2).==(3)`.  So, in this case, you can see there's more going on than meets the eye at first.  

That example also shows **Method Chaining**, which is when you stick a bunch of methods onto each other.  It behaves like you'd expect -- evaluate the thing on the left first, pass whatever it returns to the method on the right and keep going.  So `> 1+2==3` first evaluates `1+2` to be `3` and then evaluates `3==3` which is `true`.  This is great because it lets you take what would normally be many lines of code and combine them into one elegant expression.

**Bang Methods** are finished with an exclamation point `!` like `.sort!`, and they actually modify the original object.  Remember, when you run a normal method in IRB, it will output whatever the method returns but it will preserve the original object.  Bang methods save over the original object:

    > my_numbers = [1,5,3,2]
    => [1, 5, 3, 2]
    > my_numbers.sort
    => [1, 2, 3, 5]
    > my_numbers
    => [1, 5, 3, 2]          # still unsorted
    > my_numbers.sort!
    => [1, 2, 3, 5]
    > my_numbers
    => [1, 2, 3, 5]          # overwrote the original my_numbers object!

Let's answer the question, "Where did all those methods come from?" **Classes** are like umbrellas that let us give an object general behaviors just based on what it is.  An object is an instance of a class -- you (yes, you) are an instance of the `Person` class.  There are lots of behaviors (methods) that you can do just by virtue of being a `Person`... `.laugh`, `.jump`, `.speak("hello")`.  This is really useful in programming because you often need to create lots of instances of something and it's silly to have to rewrite all the methods you want all of them to have anyway, so you write them at the class level and all the instances get to use them.

Instances of a class get to **inherit** the behaviors of that class.  Inheritance works for classes too!  Your class `Person` has lots of methods but many of them are inherited just by virtue of you also being a `Mammal` or even just a `LivingThing`.  You get to use all the methods of your ancestor classes

An interesting exercise to try in Ruby is to use the method `.superclass` to ask a class what its parent is.  If you just keep on going and going, you'll see that everything eventually inherits from `BasicObject`, which originates most of the methods you have access to in the original object:

    > 1.class.superclass.superclass.superclass
    => BasicObject
    > BasicObject.methods
    => # giant list of methods

Random Note: Running the `.methods` method on a class only returns the class methods, whereas `.instance_methods` will return all methods available to any instance of that class (so `String.methods` will return a list of class methods, while `"hello".methods` will return a longer list that is the same as `String.instance_methods`).

Other Random Note: Use `.object_id` to see an object's id, and this can be useful if you're running into odd errors where you thought you were modifying and object but it's not changing.  If you debug and look at the id's along the way, you may find that you're actually only modifying a COPY of that object.

##### Exercises
##### Additional Resources

#### Strings
##### Intro and Goals
Strings are a huge part of web programming and you'll run into them everywhere from variable names to user input to giant gobs of HTML text to handling big dictionary files.  They're actually pretty simple at the core but, for being just a jumble of characters, strings have some pretty cool properties in Ruby and you can do a whole lot to manipulate them.  

This section should give you an appreciation for the ways you can mess with strings and some of the handy methods that Ruby gives you along the way to make your life easier.

##### Thought Questions
* What's the difference between single and double quotes?
* What is string interpolation?
* What are escape characters?
* What are line breaks?
* How do you make other things into strings?
* How do you concatenate strings?
* How do you access a specific character or substring?
* How do you split up strings into arrays?
* How are strings an arrays similar?
* How do you get and clean up user input on the command line?
* What does it mean that strings are "mutable" and why care?
* What is a symbol?
* How is a symbol different from a string?
* What is a Regular Expression (RegEx)?

##### Check these out First
* [Chris Pine on Strings](http://pine.fm/LearnToProgram/?Chapter=02) (was part of the prep work)
* A list of [Escape Characters](http://www.java2s.com/Code/Ruby/String/EscapeCharacterslist.htm) in Ruby
* Read through (and watch the video) for this [Regular Expressions in Ruby](http://net.tutsplus.com/tutorials/ruby/ruby-for-newbies-regular-expressions/) explanation.
* A great little [Regex Tutorial](http://regexone.com/) and the example problems (should only take an hour or so) 

##### A Brief Summary
Strings are just made up of individual characters and denoted with quotes.  `> I confuse Ruby and probably throw an error` but `> "I do not because I have quotes"`.  

**Double Quotes** are often interchangeable with **Single Quotes**... there's almost no difference and you're free to use either.  Two cases make the distinction important:

A) When you want to show quotes inside a string:

    > my_long_string = "And she said, 'Cool program!'"
    => "And she said, 'Cool program!'"

Note that you can accomplish the same type of thing by escaping the quote characters (see below).

B) When you want to use string interpolation and when you want to show quotes within a string.

**String Interpolation** occurs when you want to plug something else into a string, like a variable.  You'll find yourself using this a lot, for instance, when you make websites with dynamic text content that needs to change depending on who is logged in.  Simply use the pound symbol and curly braces `#{}` to do so, and the output of whatever is within those curly braces will be converted to a string and, presto! You've got a new string:

    > my_name = "Tiny Tim"
    => "Tiny Tim"
    > my_string = "My name is #{my_name}!"
    => "My name is Tiny Tim!"

The key point here, though, is that interpolation *only works inside DOUBLE quotes*.  Keep the interpolated stuff brief or your code won't be very legible.  Single quotes will simply escape every special character in the string and treat it like a normal letter (so the pound-curly-braces has no special meaning):

    > my_name = "Neo"
    => "Neo"
    > my_string = 'My name is #{my_name}!'
    => "My name is \#{my_name}!"  # Hey! That's not what we wanted!

**Escaping** characters just means telling the output program to not treat them specially at all (like the pound symbol, which has special meaning before the curly braces).  You do so with a back slash `\` before whatever you want to escape.  Sometimes you'll see what looks like a strange jumble of characters in your output, with lots of those '\' floating around, and you'll know that you've got some escaping going on.

    > now = "RIGHT NOW"
    => "RIGHT NOW"
    > puts "interpolating #{now} but not \#{now}"
    "interpolating RIGHT NOW but not #{now}"
    => nil            # Remember, puts returns nil!

IRB shows you the backslashes, but they'll be hidden in your `puts` output.

As you can imagine, this could get pretty tedious if you're trying to output a blog post or some other long batch of text that contains lots of mixed characters and don't want to manually or programmatically replace special characters, so later we'll see some simple convenience methods to use to take care of those issues for you.

There are some special characters that are actually denoted using the backslash and you'll want to know the key ones, which will probably pop up again and again:  
* `\n` will output a new line
* `\r` is a newline too (carriage return)
* `\t` will output a tab

    > puts "let's put a bunch of newlines between this\n\n\nand this."



    and this.
    => nil

**`to_s`** is a method that will try to convert anything into a string.  

    > 12345.to_s
    => "12345"

This method gets called a LOT behind the scenes later on... basically anytime Ruby or especially Rails is outputting or rendering something (like a variable), it will call `to_s` on it to make it a nice friendly string first.  

Fun fact: If you've created your own object, you may need to write your own `to_s` method for it to display properly in some settings (e.g. looking ahead, if you've got a Person object and want to display its first name only whenever you tried to `puts` it, you'd want to write the `to_s` method to do so).

**Combining Strings** without using interpolation can be done using "concatenation", or basically just adding them together:

    > my_name = "Billy Bob"
    > "hello" + " world" + ", say I, the great " + my_name + "!"
    # => "hello world, say I, the great Billy Bob!"

Instead of adding them with a plus `+`, you can also use the friendly shovel operator `<<` to append to a string (just like with arrays...):

    > "howdy " << "fella!"
    => "howdy fella!"

To **Access a Specific Character or Substring** of a string, just treat it like an array!  A string acts like a zero-indexed array that ends at -1, so use `[0]` to access the first letter, `[-1]` to access the last letter, and `[n..m]` to pluck a substring:

    > s = "hello"
    => "hello"
    > s[0]
    => "h"
    > s[-1]
    => "o"
    > s[-2]
    => "l"
    > s[2..4]
    => "llo"
    > s[1..-2]
    => "ell"

**Break a String into Pieces** using `.split`, which creates an array of substrings that are broken up based on whatever character you passed in:

    > list = "eggs, milk, cheese and crackers"
    => "eggs, milk, cheese and crackers"
    > list.split(", ")
    => ["eggs", "milk", "cheese and crackers"]
    > list.split(" ")
    => ["eggs,", "milk,", "cheese", "and", "crackers"]

You can also split based on individual characters by passing either a blank string or a blank regular expression (denoted by `//`):

    > list.split("")      # or also list.split(//)
    => ["e", "g", "g", "s", ",", " ", "m", "i", "l", "k", ",", " ", "c", "h", "e", "e", "s", "e", " ", "a", "n", "d", " ", "c", "r", "a", "c", "k", "e", "r", "s"] 

When you write your Ruby programs, you'll probably want to ask for **User Input**... which is easy with `gets`, which then waits for the user to type something.  You'll want to store whatever the user types into a variable and be sure to trim off the extra line break (from when the user hit the `enter` key) using `.chomp`:

    > player1 = gets    
    Erik                # this was typed in manually
    => "Erik\n"         # woah, let's get rid of that \n
    > player1 = gets.chomp
    Erik
    => "Erik"           # better.

`.chomp` will cut off a space or newline at the END of the string (and can take an optional input so you can specify what exactly to chomp off). `.strip` will remove ALL spaces and newlines from both the beginning and end of the string:

    > " dude \n".chomp
    => " dude "         # still have the extra spaces
    > " dude \n".strip
    => "dude"           # clean as a whistle.

Of course, it's up to you to figure out if your user has entered something illegal or harmful, but at least you have an easy job removing extraneous spaces and returns.

**Other Helpful String Methods** include:
* `.length` to get the length of the string
* `.downcase` to convert `"ALL THIS"`` to `"all this"`
* `.upcase` to convert `"all this"` back to `"ALL THIS"`
* `.reverse` to convert `"hello"` to `"olleh"`

Fun fact: Strings made with the backtick characters `` ` `` (which is usually located on the same key as the tilde `~`) are actually interpolated and run by your operating system, so in IRB if you type ``> puts `ls` `` on a mac, it will actually output your directory contents!

What about all the times you may want to **Search For or Replace Within Strings**?  For that, you need to begin understanding **Regular Expressions**, or "RegEx"'s.  There's a handy method for strings called `.gsub(pattern, replace_with_this)`, which finds any occurrances of that pattern and replaces it with whatever you want:

    > "hello".gsub("l","r")
    => "herro"

But what if you want to go looking for more advanced patterns than just simple letters?  Pretty much anytime you've got a function that needs to go mucking through a string looking for patterns, you can employ a Regular Expression.  

Regular Expressions are really just a special syntax that is used to find things (and not just in Ruby, they're used all over the place).  It's beyond the scope of this summary for sure, but I hope you've tried them out at [RegexOne](http://regexone.com/).  Once you know how to match stuff, you'll feel ready to take on any big dictionary files or big batches of questionable user input that needs to be standardized.  But be careful, it can be too tempting to go hog-wild with your expressions. It's something you should at least know the basics of but probably will not be applying all that often "in the wild".  

The last thing to cover is **Symbols**, which start creeping up all over the place when you get into Rails and even Hashes.  Symbols are denoted with the colon before the name, e.g. `:my_symbol` instead of `"my_string"`.  A symbol is basically like a string without any depth... string lite, if you will.  A string is **Mutable**, meaning it can be added to, reversed, and generally messed with in a hundred different ways.  Whenever you have text that you want to play around with or use as, well, text, just stick with strings.

But sometimes all you want is a name, like when you're using a hash key.  In that case, it makes sense to use symbols.  Symbols are immutable, so they don't change.  They are also only stored in memory in one place, wherease strings have a new place in memory each time you declare one:

    > "hello".object_id
    => 70196107337380
    > "hello".object_id
    => 70196107320960       # different
    > :hello.object_id
    => 461128
    > :hello.object_id
    => 461128               # same!

While you're learning, just stick with strings until you see the examples using symbols, which will mostly be with hash keys.

##### Exercises
See Below

#### Arrays
##### Intro and Goals
We saw how strings are a lot like arrays... so it's probably a good time to dive into what arrays are and how flexible they are in Ruby.  Arrays are almost as ubiquitous as strings.  You'll be working with them all the time to help store data for you, everything from the names of all your users to coordinates on a game board.  An array is an all-purpose bucket into which you can put pretty much anything.

Here, you'll learn the basics of creating arrays, how to manipulate them in a dozen different ways, and some best practices for working with arrays.  Note that we'll be learning even more about how to dig around inside of arrays in the future section on iterators, so if you're excitedly waiting to better understand .each, .map and others like them, we're almost there!  If not... you will be.

##### Thought Questions
* What are three ways to create an array?
* How do you prepopulate the array with default data?
* How do you access items in an array?
* How do you modify the items in an array?
* How do you combine arrays? 
* How do you find the values in one array that aren't in another?
* How do you find values in both arrays?
* What is the difference between `push`/`pop` and `shift`/`unshift`?
* What is the shovel operator?
* How is `> arr.pop` different from `> arr[-1]`?
* How is `push`ing or `<<`ing another array into your array different from just adding them together?
* How do you delete items in an array?
* Why should you be careful deleting items in an array?
* How can you convert arrays to strings?
* How can you figure out if an array contains a particular value?
* What are the naming conventions for arrays?
* What should you store in arrays?

##### Check these out First
* Do [Codecademy's section on arrays](http://www.codecademy.com/courses/ruby-beginner-en-F3loB/0/1) for some practice with them


##### A Brief Summary

Arrays begin life as empty containers waiting to be filled with objects or data.  As items are added, they stay in whatever spot you put them, which is good because then you know exactly where to find them later.  You can put anything in an array!  Numbers, strings, objects, symbols, haikus...

**Creating an Array** can happen in many different ways.  You can either create it empty, specify how many spaces it should have (still empty), or even **fill it with default values**:

    > a = Array.new     # 1
    => []               # see, it's empty
    > b = []
    => []               # still empty
    > c = Array[]       
    => []
    > empty_a = Array.new(5)
    => [nil, nil, nil, nil, nil]
    > full_a = Array.new(3, "hi")
    => ["hi", "hi", "hi"]

And remember, you can store pretty much anything in there, even other arrays:

    > full_b = [1, 4, 8, "hello", a]
    => [1, 4, 8, "hello", []]  # Cool, arrays inside arrays!

... *but don't do that!*  It's best to keep only ONE type of thing in your arrays or you'll have many headaches down the road because you'll almost always assume that there's only one type of thing in there.  Forget that you ever learned that arrays can hold different values.

**Accessing Items** is super easy, just start from `0` like you did with strings.  Just like with strings, you can start from the end of the array using negative numbers from `-1` and you can even grab ranges of values (which are themselves arrays!):

    > arr = [1, 3, 5, 7, 2]   # favorite way to declare an array
    => [1, 3 ,5 ,7 ,2]
    > arr[0]
    => 1
    > arr[-1]
    => 2
    > arr[1..3]
    => [3, 5, 7]          # this returned an array!
    > arr[1..200000]      
    => [3, 5, 7, 2]       # no error... silently cuts off at the end

**Modifying Items** is as simple as accessing them is... just set them equal to a value:

    > arr[0] = 42
    => 42
    > arr
    => [42, 3, 5, 2]      # changed it!
    > arr[0..2] = 99
    => 99
    > arr
    => [99, 2]            # wiped out several values, oops...

**Adding Arrays** is also done similarly to strings, by just mashing one onto the end of the other:

    > first = [1,2,300]
    => [1,2,300]
    > second = [7,8,9]
    => [7,8,9]
    > combined = first + second
    => [1,2,300,7,8,9]      # this is a NEW array

**Subtracting Arrays** is a bit different... think of the minus sign as saying "take away any and all values that are in the right array from the left array". The only values remaining will be those from the left that were not included in the right side at all:

    > [1,2,3] - [2,3,4]
    => [1]                # the 4 did nothing
    > [2,2,2,2,2,3,4] - [2, 5, 7]
    => [3,4]              # it killed ALL the 2's

You'll find yourself adding arrays a lot more frequently than subtracting them but it's good to know both.

If you want to find values in **Both** arrays, check their union using the ampersand `&`:

    > [1,2,3]&[2,4,5]
    => [2]

What if you only want to add or subtract one single value?  That's a very common operation with arrays, and Ruby has provided four handy methods that let you either pluck away or add onto the front or back of the array.  First, the more common is to add or remove stuff from the END of the array, using **`.push` or `.pop`**:

    > my_arr = [1,2,3]
    => [1,2,3]
    > my_arr.push(747)
    => [1, 2, 3, 747]
    > my_arr
    => [1, 2, 3, 747]     # warning: we modified my_arr!!!
    > my_arr.pop
    => 747
    > my_arr.pop
    => 3
    > my_arr
    => [1, 2]          # warning: pop also modified my_arr

What if you want to take the item off the FRONT of the array?  This is less common.  For that, use the similar `.shift` and `.unshift` methods:

    > my_arr = [1,2,3]
    => [1,2,3]
    > my_arr.shift
    => 1
    > my_arr
    => [2,3]          # warning: shift also modified my_arr!
    > my_arr.unshift(999)
    => [999, 2, 3]
    > my_arr
    => [999, 2, 3]    # warning: unshift... yep, modified my_arr.

So the `push`/`pop`/`shift`/`unshift` methods should take you wherever you realistically need to go.  Although there's another handy method you should be aware of, the **Shovel Operator**, aka `<<`.  This method is *almost* identical to push, since it just jams whatever's to its right into the array:

    > my_arr = [1,2,3]
    => [1,2,3]
    > my_arr << 3
    => [1, 2, 3, 3]
    > my_arr << [4,5]
    => [1, 2, 3, 4, [4, 5]]   # Array within array alert!

For now, just think of it as the cool way of pushing onto an array.  But note that `<<` is often overridden (like in Rails), and so it pays to be mindful of exactly what flavor of `push`ing you're doing.

**Deleting Items** from an array should be done carefully because, if you're deleting items inside a loop or something like that, it will change the index of the other items and you'll need to anticipate this or live to regret it.  Delete an item at a specific index using `.delete_at`, which is sort of like `pop`ing but from anywhere you want:

    > my_arr = [1,2,3]
    => [1, 2, 3]
    > my_arr.delete_at(1)
    => 2
    > my_arr
    => [1,3]

See if an array **includes an item** AT ALL by using `.include?`, which, as you should see from the `?` at the end, returns true or false:

    > my_arr.include?(3)
    => true
    > my_arr.include?(132)
    => false

To find WHERE a specific item lives in the array, use `.index` but note that it only returns the FIRST instance of this (and then gives up. Lazy method.):

    > my_arr.index(3)
    => 2
    > [1,2,3,4,5,6,7,3,3,3,3,3].index(3)
    => 2                  # Just the index of the FIRST match
    > my_arr.index(132)
    => nil                # Not an error, just nil

**A few useful and commonly used methods:**
* `.shuffle` will mess up your whole array
* `.sort` will clean it up again for you.  Though `.sort` is pretty self-explanatory in the simple case, it can actually take parameters to let you decide if you want to sort things using a different (or reverse) methodology.
* `.sample` picks out a totally random value from the array... good for gambling games!
* `.first` gives you the first item (but doesn't remove it, so it's same as `[0]`) but can be more descriptive of your code's intent.
* `.last` is same as `[-1]`

Do as I say and not as I do: name your arrays with the plural form (because it has a bunch of things in it, like `colorful_bugs` instead of `colorful_bug`) and be descriptive.  No one likes to try and figure out what `array1` or `a` contains... stick with `colorful_bugs`.  I just kept them short here because they're tiny examples.  Someone should rename them all.

Strings are a lot like arrays... but how do we **Convert an Array into a String**? Just use `.join` and tell it what, if anything, you want in between each element (the "separator"):

    > ["he", "llo"].join
    => "hello"
    > colorful_bugs = ["caterpillar", "butterfly", "ladybug"]
    => ["caterpillar", "butterfly", "ladybug"]
    > "I found a #{colorful_bugs.join(' and a ')} in the yard!"
    => "I found a caterpillar and a butterfly and a ladybug in the yard!" 

Advanced stuff:
Remember how we could create a new array and fill it up with stuff using `Array.new(5, "thing")`?  `Array.new` also takes an optional argument that is a block and it will run it every time it needs to populate a new element.  Woah! We got a bit ahead of ourselves, but it's a cool feature to have floating in the back of your head.

    > Array.new(5){|item_index| item_index ** 2}
    => [0, 1, 4, 9, 16]    # It squared each index to populate the array!

##### Exercises

#### Hashes
##### Intro and Goals

Hashes may be a bit intimidating at first but they're actually pretty similar to arrays.  They're basically just containers for data, like arrays, but instead of storing data based on a numeric indices, you use "keys" which can be strings or symbols.  This makes hashes more appropriate for storing data with a bit more depth to it.

##### Thought Questions
* What is a hash?
* What are keys and values?
* How is a hash similar to an Array?
* How is a hash different from an Array?
* What are 3 ways to create a hash?
* What is the hash rocket?
* How do you access data in a hash?
* How do you change data in a hash?
* How do you add hashes together?
* How do you list out all the keys or values?
* How do you see if the hash contains a key or value?
* What is a set?


##### Check these out First
* [Treehouse's intro to Hashes video](http://www.youtube.com/watch?v=NvXeDtKkXq8), and don't worry about the awesome_print gem, it's not required.
* [Codecademy's section on Hashes](http://www.codecademy.com/courses/ruby-beginner-en-F3loB/1/1) for the basics.
* [Codecademy's hashes and symbols section](http://www.codecademy.com/courses/ruby-beginner-en-Qn7Qw) to bring together what we talked about in the strings section.
* Go back and do [Ruby Monk's Hashes section](http://rubymonk.com/learning/books/1/chapters/10-hashes-in-ruby/lessons/46-introduction-to-ruby-hashes) if you didn't do it during the Web Dev 101 section.  Shame on you for not doing it before >:o

##### A Brief Summary

A *Hash* is just a container for data where each piece of data is mapped to a *Key*.  The data is called the *Value*.  Keys can be either strings or symbols. Values can be anything, just like with arrays.  A hash looks almost like an array, but with squiggly braces `{}` instead of hard ones `[]`.  There's no order to a hash (unlike an array)... you're accessing your data using strings anyway so it doesn't matter which order they're in.

Make a new hash using several methods:

    > my_hash = Hash.new
    => {}
    > my_hash = {}        # easier way
    => {}

You store data in a hash by matching a key with a value.  Use the **Hash Rocket** `=>` (not to be confused with the same symbol in our IRB examples which denotes the IRB output) if you're creating the hash, or just index into it like an array using hard brackets `[]`.

    > favorite_colors = { "eyes" => "blue", "hair" => "blonde"}
    => {"eyes"=>"blue", "hair"=>"blonde"}
    > favorite_colors["eyes"]
    => "blue"

**Change Data** in a hash just like an array, by indexing into it and assigning a new value.  Unlike an array, to create a new data item, just pretend it already exists and assign it a value:

    > favorite_colors["eyes"] = "green"
    => "green"
    > favorite_colors
    => {"eyes"=>"green", "hair"=>"blonde"}
    > favorite_colors["skin"] = "suburned"
    => "sunburned"
    > favorite_colors
    => {"eyes"=>"blue", "hair"=>"blonde", "skin"=>"sunburned"}

Hashes are useful for lots of reasons behind the scenes, but it should be immediately obvious that you can handle more nuanced data than you can with arrays.  How about a dictionary of words?  Just store the words as keys and the meanings as values, if you so choose.  You see hashes all the time in Rails, including as a way of passing options to a method (since they can store all kinds of different things and be variable sized).

If you recall our discussion from Strings, we use symbols as keys for hashes more often than not.

    > favorite_smells = { :flower => "daffodile", :cooking => "bacon" }
    => { :flower => "daffodile", :cooking => "bacon" }

**Delete** from a hash by just setting the value to `nil` or by calling the `.delete` method:

    > favorite_smells[:flower] = nil
    => nil
    > favorite_smells
    => {:cooking => "bacon" }             # one deleted...
    > favorite_smells.delete(:cooking)
    => "bacon"
    > favorite_smells
    => {}                                 # ...and the other.

That's all pretty straightforward.  What if we want to **add two hashes together**?  Just use `.merge`.  If there are any conflicts, the incoming hash (on the right) overrides the hash actually calling the method.

    > favorite_beers = { :pilsner => "Peroni" }
    => { :pilsner => "Peroni" }
    > favorite_colors.merge(favorite_beers)
    => {"eyes"=>"blue", "hair"=>"blonde", "skin"=>"sunburned", :pilsner => "Peroni"}       # okay, that's getting silly now...

If you want to know what **All the Keys** are (more common) or **All the Values*** are (less common) in a hash, just use the aptly named `.keys` and `.values` methods to spit them out as an array:

    > favorite_colors.keys
    => ["eyes", "hair", "skin", :pilsner]  
    > favorite_colors.values
    => ["blue", "blonde", "sunburned", "Peroni"]

A simpler kind of hash is called a **Set**, and it's just a hash where all the values are either True or False.  It's useful because your computer can search more quickly through this than an array trying to store the same information due to the way it's set up behind the scenes.  You'll encounter them in some of the exercises later.

##### Exercises

#### Numbers, Strings and Arrays and Hashes Exercises (Paired)
* sort
* reverse
* 
* towers of hanoi
* 

#### Enumerable
##### Intro and Goals
##### Thought Questions
##### Check these out First
* [Codecademy's section on iterating over Arrays and Hashes](http://www.codecademy.com/courses/ruby-beginner-en-F3loB/2/1)
##### A Brief Summary
##### Exercises

#### Ranges
##### Intro and Goals
##### Thought Questions
* How is two periods `(1..5)` different from three `(1...5)`?
##### Check these out First
##### A Brief Summary
##### Exercises

#### Dates and Times
##### Intro and Goals
##### Thought Questions
##### Check these out First
##### A Brief Summary
##### Exercises

#### Advanced Issues
##### Intro and Goals
Puts vs p
.to_s
.inspect
falsy values, nil

##### Thought Questions
##### Check these out First
##### A Brief Summary
##### Exercises

#### Tutorial

#### Exercises (Paired) >> PUT LATER AFTER METHODS / BLOCKS!
* Rewrite the following methods from Enumerable.  You may not use the real method... which should be obvious.  You MAY use #each in the following methods once you've created it yourself the first time:
    * #each
    * #each_with_index
    * #map
    * #select
    * 

### Conditionals and Flow Control

So now you've got an understanding of what tools you can use and it's time to start thinking about how the program moves through your code.

CODECADEMY http://www.codecademy.com/tracks/ruby

#### If/Else

##### The Ternary Operator

##### Until

#### Case Statements

#### Exercises

### Methods

You have the power to assemble the building blocks and control how your program steps through them.  You may have been told that "everything in Ruby is a method."  So what are methods anyways?

#### Everything is an Object

#### Inputs

Symbols, hashes, options hashes, default values

#### Return Statements

#### Side Effects

#### Method Chaining

#### KISS

### Blocks... Huh?

One of the most confusing parts of learning basic Ruby is understanding what blocks are and how they work.  It shouldn't be, because they're actually pretty simple.

[Procs, Lambdas and Closures in Ruby by Peter Cooper (video)](http://www.youtube.com/watch?v=VBC-G6hahWA)

http://www.rubytapas.com/episodes/36-Blocks-Procs-and-Lambdas 
> Blocks vs procs vs lambdas free screencast.  Need to know call though.

http://www.robertsosinski.com/2008/12/21/understanding-ruby-blocks-procs-and-lambdas/

Blocks explained by Alex Chaffee (video) (http://codelikethis.com/lessons/ruby_blocks/blocks)

CODECADEMY http://www.codecademy.com/tracks/ruby

#### Blocks are Very Ruby-ish

#### Ways to declare a Block

#### Block Return Statements

#### Where Blocks are Used

#### Examples

#### Procs

#### Examples

#### Exercises

### Iteration

CODECADEMY http://www.codecademy.com/tracks/ruby

You can assemble code, tell the program which parts of it to execute, and wrap it all up in a method.  There's still something missing... what if you want to make something happen a whole bunch of times?  You certainly don't just run the method again and again.  Luckily we've got several standard ways of iterating through a piece of code until we tell the program to stop.

### Projects

### Style
https://github.com/bbatsov/ruby-style-guide

## Intermediate Ruby

Classes, inheritance (use .methods), OO design, refactoring, naming, recursion, scope, regex, Modules, metaprogramming (reflection?)
http://www.codecademy.com/tracks/ruby for oop

## Ruby and the Web

## File I/O and Serialization

## Testing with RSpec and Test Driven Development
http://guides.rubyonrails.org/testing.html
## Basic Data Structures

## Basic Algorithms

## Final Projects

## Finish






