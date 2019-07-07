---
layout: post
title:      "Nerd Alert- Pokemon CLI project"
date:       2019-07-06 23:52:32 -0400
permalink:  def_gotta_catch_em_all
---

![](https://imgur.com/tVp8h2P)

I’m a true 90’s baby through and through. When given the opportunity to branch out and create a project of anything I could dream up, I turned to my childhood.

Many a hour were spent clutching a Game Boy color playing Pokemon Red version. That opening intro is classic. In the original gameplay, the game first loads with Professor Oak welcoming you and introducing you to the world of Pokemon. You choose your gender and name, eventually you’re given a choice of starter Pokemon from Charmander, Squirtle, or Bulbasaur. It’s amazing, epic and I one hundred and ten percent wanted to do this for my CLI project.

Another huge factor in choosing a topic for my project was my discovery of the Catpix Ruby gem. This gem will take a picture and print a pixelated picture to the terminal. I knew I wanted to have a project that would incorporate this gem.

I have a CLI class, a Pokemon class, a Scraper class, and a Trainer class. The CLI class runs through the script of the entire program. It has a run method that runs through the rest of the CLI methods in order needed. Scraper class takes the input link and scrapes information on 809 Pokemon (all 9 generations). As it accesses the information I was looking for, it initializes new Pokemon objects with an attr accessor of name, image link, an array of types, and a link for more info. The Trainer class stores the users name and has an attr accessor of a Pokedex that will save the starter Pokemon chosen.

A huge hurdle I hit with using my Catpix gem was getting it to allow me to pass in an image link rather than a specific location in my personal computer. Considering I was relying on the scraped image link to be passed through my Catpix gem, this was a huge problem.

After much research and some deep googling I found the MiniMagick gem. The MiniMagick gem relies on the Rmagick gem to work. The MiniMagick gem would take an image link and turn it into an object. One of the attr accessors in this MiniMagick object was path. I could then take that path and use it with my Catpix gem. I discovered this at 4 am after an incredible amount of trial and error trying to correctly install each gem I needed. I can’t begin to explain my excitement at figuring out this, if I had been holding an infant I may have shaken it... (Just kidding but that’s the level of excitement.) I basically used a gem on top of a gem on top of a gem. But hey, now that functionality was working. Score!

After running through my script, that VERY closely follows Pokemon Red Version beginning game play, Professor Oak presents the user with a Pokedex. Here is where I ventured from what really happened and what happens when you get code involved. In the normal gameplay, it’s your mission to travel and collect information on every Pokemon you come across. This information is then saved in the Pokedex. In a way a card catalogue of Pokemon. In my program, the Pokedex is already loaded with information on every Pokemon. When you load up the Pokedex you’re presented with options such as see all types of Pokemon, see all Pokemon of a specific type, look up a Pokemon by name, or see a surprise Pokemon.

All of the options in the Pokedex get their information by iterating over the list of 809 Pokemon and returning it. For instance, when the user types in ‘types’ the program will run through each Pokemon, collect all the types in an array, alphabetize the list, and return only uniq items. When user types in ‘surprise’ or a specific Pokemon’s name, a pixelated picture will print to the terminal along with information on that Pokemon. Typing ‘exit’ will exit from the program.

It was a challenge at first to adjust to not only creating code from scratch, but learning how to test my code not using TDD. I wound up running through my program many, many times until it looked how I wanted it to. I relied on Pry like a crutch and sprinkled binding.pry’s in there like I was Emeril Degasse. I learned a lot from creating this project and really boosted my own self-confidence in my knowledge and my abilities. I’ve helped some of my cohort mates with their code and enjoyed seeing the excitement when they create something and understand what they’re doing. I look forward to showing off what I’ve created and seeing what everyone else came up with.
