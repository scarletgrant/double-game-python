# double-game-python

Double Game in Python using Jupyter Notebook. 

This program has been awarded an A+ with 95% score.

## Dobble
A simple implementation of the Dobble card game has is created. Each card has eight images and each pair of cards will have exactly one image in common. The game is to be the first to spot the matching image on each pair. For the game, one card is revealed each time and compared with the last card in the game. This way, each card is involved twice. At the beginning of the game, players decide how many rounds they want to play in the game. Players can record who won with 'A' or 'B', and a draw can be recorded with a 'D' or 'd'.

### Files
An emoji package is used for this game. To install please use: pip install emoji --upgrade
This game uses a .text file (emoji_names) with 57 emoji's. The original required file had 60, but 3 names did not presented an emoji from the package and therefor they have been removed.

### Structure

**image_dictionary:** 
57 emoji's are stored in image_dictionary

**card_dictionary:** 
Generates cards with sets of image_ids and stores them in dictionary with the card number as key and the image id's (in a set) as the value.

**Class DoubleCard*:** 
A simple set blueprint for the cards. There are 57 valid cards.

**Class DobbleDeck*:** 
It holds and manages a deck of cards that are stored as DoubleCard instances ad has three methods:

    1. add_card*
    2. remove_card*
    3. play_card*

**Function generate_cards:** 
Generates cards with sets of image_ids and stores them in card_dictionary. 
For the generation of the pairs with only one matching image, some sample code has been given and edited. It works only when the number of images on the card is a primenumber plus 1, e.g. 3,4,6,8. The program is designed to be as flexible as possible for future changes and updates. Upon delivery, the function 'generate_cards' takes 8 images as requested, but this can be quickly adjusted with an argument when calling the function. The amount of available cards can vary for each image number which should be taken into account when adjusting the game.

**Function check_validity:**
A check_validity function is created that will take the deck as argument and check if the cards only match on one image. The intersection method is used here for the validation. This function is callable in two modes:
1. check_validity(deck, verbose = True)
2. check_validity(deck)
The first one produces output after validation.

**Function print_card_format:** 
Casts the image_ids to an emoji with the image_dictionary

**Function print_cards:**
Calls the print_card_format

**Function dobble_game*:**
Allows two users to play. It will present 'cards' as lists of emoji's by calling the format function. The users will decide who wins and provide the input to record the win counts.


*This class, method or function have been created by requirement 
