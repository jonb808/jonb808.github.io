---
layout: project
type: project
image: images/pokefight.jpg
title: Simply Pokemon
permalink: projects/Pokemon
# All dates must be YYYY-MM-DD format!
date: 2017-03-01
labels:
  - Java
  - GitHub
summary: As a school project, we were tasked with making a program that runs a basic pokemon battle gameplay scenario.
---
## Pokemon the Game
Pokemon is a well known game with a relatively simple gameplay. In this game, a player has a set of 6 pokemons and battles with other pokemon. The opposing pokemon can be from other players or in the wild. The winner of the battle is dependant on attack and health points. The amount of attack points dealt also account for types to inflict more or less damage. For wild pokemon, the player is also given the option to run or catch it. 

<img class="ui medium left floated image" src="../images/Pokemonbattle.png">

For this project, we used Java to create the user interface for a pokemon battle. To do this, we had to use everything we learned during the term. I began by creating the pokemon as objects and sorting them in an array. I then created a type map to account for all the different pokemon types and how they interact against each other. For this simplified pokemon game, I then made a pokedex file to account for other pokemone that the player can encounter. We then put everything together and made a GUI for the player so that he begins with a pokemon and encounters opposing pokemon. The player is then given options that simulate the pokemon battle gameplay. This project was difficult as I was still learning, but through it, I gained experience in combining different pieces of code to make a complete project.

Another valuable part of this experience was learning to include exception handling. I previously never used exceptions much in past experiences, but it proved useful for this project. Because the pokemon code interacted with other components for the simulated gameplay, there were many rules that had to be followed which would otherwise later cause errors in other unassumming pieces of code. Below are some examples of how some of our exceptions were set.

```
   public void setName(String newName)throws PokemonException{
      this.name = newName;
   }
   public void setHp(int newHp)throws PokemonException{
      if((newHp >= 0) && (newHP <= 401)){
         this.hp = newHp;
      }
      else{
         PokemonException he = new PokemonException();
         he.setMessage("hp should be between 0 - 401");
         throw he;
      }
   }
   public void setNumber(int newNumber)throws PokemonException{
      if((newNumber >= 0) && (newNumber <151)){
         this.number = newNumber;
      }
      else{
         PokemonException ne = new PokemonException();
         ne.setMessage("Number should be a number between 1 and 151");
         throw ne;
      } 
   }
 ```
